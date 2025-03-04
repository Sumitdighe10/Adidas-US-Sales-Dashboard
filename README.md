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

--
VAR TotalSales = SUM('Sales Data'[Total Sales])
VAR Profit = SUM('Sales Data'[Operating Profit])
VAR ProfitMargin = DIVIDE(Profit, TotalSales, 0)

--


