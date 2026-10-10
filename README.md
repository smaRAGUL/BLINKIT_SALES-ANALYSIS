# BLINKIT_SALES-ANALYSIS
An interactive Power BI dashboard that analyses sales, ratings, item visibility and outlet performance for Blinkit, India's quick-commerce grocery app. It turns 8,523 item-level records from an Excel dataset into clear KPIs and visuals that show which outlet types, locations, sizes and product categories drive revenue.

Table of Contents:
Project Objective
Dataset
Tools and Skills Used
Dashboard Features
Key KPIs
Key Insights
Data Preparation Steps
Repository Structure
How to Use
Future Improvements
Author

Project Objective:
Help a business or category manager answer questions such as:

How much total revenue do the outlets generate, and what is the average sale per item?
Which outlet location tier, outlet size and outlet type contribute most to sales?
How do fat content (Low Fat vs Regular) and item type relate to sales and customer ratings?
How has the number of outlets established changed over the years?
Which outlet types have better or worse item visibility?

Dataset:
Source: Blinkit Grocery dataset Kaggle
Format: Excel (.xlsx)
Size: 8,523 rows
Main fields (verify against your file): Item Identifier, Item Type, Item Fat Content, Item Visibility, Item Weight, Outlet Identifier, Outlet Establishment Year, Outlet Size, Outlet Location Type, Outlet Type, Sales, Rating

Tools and Skills Used:
Area	Details
Data source	Microsoft Excel
Data cleaning and modelling	Power Query, Power BI data model
Calculations	DAX measures (SUM, AVERAGE, COUNT, DISTINCTCOUNT)
Visualization	Power BI Desktop: cards, donut charts, area chart, bar charts, funnel, table, slicers, bookmarks
Concepts	KPI design, data storytelling, interactive filtering, dashboard layout

Dashboard Features:
KPI cards: Total Sales, Average Sale, Number of Items, Average Rating
Slicers (filters): Outlet Location Type, Outlet Size, Item Type, which update every visual on the page
Metric switch buttons: Toggle the charts between Total Sales, Average Sale, No. of Items and Average Rating
Outlet Establishment: Area chart of the metric by outlet establishment year (2010 to 2020+)
Outlet Size: Donut chart showing the split between High, Medium and Small outlets
Outlet Location: Funnel chart comparing Tier 1, Tier 2 and Tier 3 cities
Fat Content and Fat by Outlet: Low Fat vs Regular, overall and by location tier
Item Type: Bar chart across 16 product categories (Meat, Dairy, Snack Foods, Fruits and Vegetables, Soft Drinks, Breads and more)
Outlet Type table: Total Sales, No. of Items, Average Sale, Average Rating and Average Item Visibility for each outlet type, with a Total row

Key KPIs:
KPI	Value
Total Sales	1.20M
Average Sale	141
Number of Items	8,523 (~9K)
Average Rating	4
Average Item Visibility	0.07

Key Insights:
Tier 3 cities lead in revenue. Tier 3 contributes about 472K (~39%), followed by Tier 2 at about 393K (~33%) and Tier 1 at about 336K (~28%).
Medium-sized outlets generate the most sales. Medium outlets bring in about 508K (~42%), Small about 445K (~37%) and High about 249K (~21%).
Customer ratings are consistent. The average rating stays around 4 across item types, fat content and outlet types, which shows stable customer satisfaction.
Grocery Stores show the highest item visibility (0.10) compared with Supermarket Type 2 and Type 3 (0.06 each), yet the average sale per item stays close to 140 across all outlet types.
Outlet establishment peaked in the late 2010s. The area chart shows a sharp rise to about 205K before returning to around 130K.
Sales are spread evenly across item categories. No single product category dominates the rating metric, so product mix decisions should rely on sales and visibility rather than ratings alone.

Note: Insights are based on the dashboard values at default filters (all outlets, all items).

Data Preparation Steps:
Imported the Excel file into Power BI using Power Query.
Standardised inconsistent labels in Item Fat Content (for example, "LF", "low fat" and "Low Fat" merged into Low Fat; "reg" merged into Regular).
Checked and handled missing values (for example, in Item Weight and Outlet Size).
Corrected data types for sales, ratings and years.
Created DAX measures for the KPI cards and chart metrics.
Designed the layout, slicers and metric-switch buttons, then applied a consistent yellow and green Blinkit-style theme.

DAX:
Total Sales = SUM(BlinkitData[Sales])
Average Sale = AVERAGE(BlinkitData[Sales])
No of Items = COUNT(BlinkitData[Item Identifier])
Average Rating = AVERAGE(BlinkitData[Rating])
Average Item Visibility = AVERAGE(BlinkitData[Item Visibility])

Repository Structure:
blinkit-powerbi-dashboard/
│
├── data/
│   └── BlinkIT_Grocery_Data.xlsx
├── powerbi/
│   └── Blinkit_Dashboard.pbix
├── images/
│   └── blinkit_dashboard.png
└── README.md

How to Use:
Clone or download this repository.
Open powerbi/Blinkit_Dashboard.pbix in Power BI Desktop.
If the data source path breaks, go to Transform data > Data source settings and point it to data/BlinkIT_Grocery_Data.xlsx.
Use the slicers and metric buttons to explore the dashboard.

Future Improvements:
Add year-over-year and month-over-month trend analysis
Add a Top N products view and drill-through pages for each outlet
Build predictive sales forecasting
Connect to a live database (SQL) instead of a static Excel file

Author:
RAGUL.R Aspiring Data Analyst | Power BI | SQL | Excel | Python
LinkedIn:ragul-rajapathy-15rk10
GitHub:smaRAGUL
Email:rragulr43@gmail.com
