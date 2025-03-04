🎽 Adidas Sales Analysis - Power BI Dashboard

📌 Overview

This Power BI dashboard provides an interactive Adidas sales analysis across different regions and retailers in the United States. It visualizes key financial metrics, sales performance, profit margins, and regional sales trends.

The dashboard's background was designed using PowerPoint with a Glassmorphism effect and then imported into Power BI to enhance aesthetic appeal and user experience.

📸 Dashboard Preview

![Dashboard](Dashboard%20image.png)

🎨 Background Design & Aesthetics

How It Was Created

The dashboard background was designed in PowerPoint, leveraging Glassmorphism effects to enhance aesthetics.

🔹 Key Design Elements:

Glassmorphism Concept: Translucent cards with a blur effect to create a modern look.

Gradient Background: Soft color blending to make data stand out.

Transparency & Shadows: Gives a frosted glass effect.

Adidas Logo & Sneaker Images: Incorporated branding elements.

Rounded Containers: Ensures smooth UI experience.

🔹 Steps:

Created a blank PowerPoint slide and removed default placeholders.

Added a color gradient background using soft pastel tones.

Drew rounded rectangles with transparency for the Glassmorphism effect.

Imported Adidas logos & sneaker images for branding.

Saved as a PNG image and imported into Power BI as a canvas background.

![Powerpoint](Powerpoint%20image.png)

📂 Dataset Used

The dataset includes key information on sales, profit, regional distribution, and retailer performance. Data was cleaned and structured to ensure accuracy in calculations and visualizations.

📝 DAX Measures & Calculations

📂 Key Performance Indicators (KPIs)

🔷 1️⃣ Total Sales, Profit & Profit Margin Calculation

Calculates Total Revenue, Operating Profit, and Profit Margin percentage.

```
VAR TotalSales = SUM('Cleaned_Adidas_Sales_Data'[Total Sales])
VAR Profit = SUM('Cleaned_Adidas_Sales_Data'[Operating Profit])
VAR ProfitMargin = DIVIDE(Profit, TotalSales, 0)

```
Computes Total Sales & Operating Profit.
Calculates Profit Margin as a percentage of Total Sales.

2️⃣ Identifying the Best Performing Retailer

```
VAR TopRetailer =
    TOPN(1,
        SUMMARIZE(
            'Sales Data',
            'Sales Data'[Retailer],
            "RetailerSales", SUM('Sales Data'[Total Sales])
        ),
        [RetailerSales], DESC
    )
```
Extracts the retailer with the highest sales.
Uses TOPN(1, …) to return only the top-selling retailer.
Provides insights into which retailer contributes the most to total sales.

3️⃣ Finding the Most Profitable Region

```
VAR TopRegion =
    TOPN(1,
        SUMMARIZE(
            'Sales Data',
            'Sales Data'[Region],
            "RegionSales", SUM('Sales Data'[Total Sales])
        ),
        [RegionSales], DESC
    )
```
Identifies the region with the highest sales.
Helps in understanding regional sales distribution.
Assists businesses in allocating resources effectively.

4️⃣ Sales & Profit Comparison Across Retailers

```
VAR RetailerComparison =
    SUMMARIZE(
        'Sales Data',
        'Sales Data'[Retailer],
        "Total Sales", SUM('Sales Data'[Total Sales]),
        "Operating Profit", SUM('Sales Data'[Operating Profit])
    )
```
Summarizes total sales and profits for each retailer.
Allows for easy comparison of profitability across multiple retailers.
Provides key insights into which retailers are most profitable.

![Dax](https://github.com/Sumitdighe10/Adidas-US-Sales-Dashboard/blob/main/DAX%20formula%20for%20Dynamic%20Summary.png)

📊 Power BI Visualizations & Insights
📌 Key Visualizations Used:

1️⃣ KPI Cards

Displays Total Sales, Operating Profit, Profit Margin.
Provides a quick overview of financial performance.

2️⃣ Sales & Profit by Retailer (Bar Chart)

Compares total sales & operational profit across different retailers.
Helps identify which retailers perform the best.

3️⃣ Regional Sales Distribution (Map)

Visualizes sales spread across different U.S. regions.
Shows areas with highest and lowest demand.

4️⃣ Unit Sales by Region (Stacked Area Chart)

Displays sales volume trends across different regions.
Helps track which regions sell the most products.

5️⃣ Operating Profit vs. Total Sales vs Retailer ID (Scatter Plot)

Plots total sales against operating profit.
Helps analyze the correlation between sales & profit.

6️⃣ Year-over-Year Sales Comparison (Line Chart)

Compares total sales for different years.
Helps track growth and trends over time.



📊 Live Power BI Dashboard
👉 Access the interactive Power BI Dashboard here:

https://app.powerbi.com/groups/me/reports/1b2ad26b-4da6-4059-89c3-3e798e6a078a/01a50f350a01576953ee?experience=power-bi


👤 Author
🔹 Sumit Dighe




