# Car Sales Dashboard
# Dashboard Link: https://app.powerbi.com/groups/me/reports/eb79039c-3528-4fc0-96ba-9a4d2ac9f2ba/f576220cbf783842114d?ctid=0369dfc8-6c8b-49ee-a447-83cfd92cdc23&experience=power-bi

## Overview
This Power BI dashboard provides detailed insights into car sales, covering various aspects like total sales, average prices, and sales distribution by car types and colors. It also presents dealer and company-wise sales trends to enable business decision-making.

## Steps to Create the Dashboard

- Step 1: Import the car sales dataset into Power BI and clean the data using Power Query.

- Step 2: Establish relationships between the relevant tables for accurate data modeling.

- Step 3: Create the "Total Sales" measure using DAX SUM on the sales column.

- Step 4: Create the "YTD Total Sales" and "MTD Sales" measures using TOTALYTD and TOTALMTD functions, respectively.

- Step 5: Develop a measure for "Average Price" using DAX AVERAGE on the price column.

- Step 6: Create measures for "YTD Cars Sold" and "MTD Cars Sold" using COUNT.

- Step 7: Design the dashboard layout with two main pages: Overview and Details.

- Step 8: Add KPI cards for Total Sales, Average Price, Cars Sold, and other key metrics on the Overview page.

- Step 9: Create a line chart for displaying weekly YTD sales trends.

- Step 10: Add visualizations like pie and bar charts for showing sales by car type, body style, and region.

- Step 11: Apply slicers for filtering the data based on criteria such as Body Style, Dealer Name, and Transmission.

- Step 12: Publish the dashboard to Power BI service and enable sharing with appropriate permissions.


## DAX Formulas for KPIs:

1. **Total Sales:**

        Total Sales = SUM('Sales'[Total_Sales])

2. **YTD Total Sales:**

        YTD Total Sales = TOTALYTD([Total Sales], 'Calendar'[Date])

3. **MTD Sales:**

        MTD Sales = TOTALMTD([Total Sales], 'Calendar'[Date])

4. **Average Price:**

        Average Price = AVERAGE('Sales'[Price])

5. **YTD Cars Sold:**

        YTD Cars Sold = COUNT('Sales'[Car_ID])

6. **MTD Cars Sold:**

        MTD Cars Sold = COUNTX(FILTER('Sales', MONTH('Sales'[Date]) = MONTH(TODAY())), 'Sales'[Car_ID])

7. **Sales Growth %:**

        Sales Growth % = DIVIDE([YTD Total Sales] - [MTD Sales], [MTD Sales], 0)

8. **% Total Sales by Dealer Region:**

        % Sales by Region = DIVIDE([Total Sales], CALCULATE([Total Sales], ALL('Sales'[Region])))


## Key Findings

**Top Sales Performers:** Chevrolet and Cadillac lead in total sales across various regions.

**Price Trends:** The average car price has shown a slight decline in the current year. Regular monitoring is required to optimize pricing strategy.

**Color Preferences:** Pale white cars dominate the market, contributing to the highest sales volume.

**Body Style:** SUVs and Hatchback are the most popular car types, significantly driving sales in the overall market.

**Dealer Insights:** Austin and Janesville regions have the highest dealer sales, indicating strong market demand in those areas.

## Key Features:
- Sales performance by region and model
- Monthly revenue trends
- Top-performing sales agents
- Customer demographics and preferences
- Interactive filters for detailed analysis

## Conclusion
This dashboard effectively summarizes car sales performance metrics for data-driven decision-making. Using the dashboard, businesses can optimize strategies based on sales patterns, popular car types, and dealer performance.

## Dasboard Snapshot: ![Image](https://github.com/user-attachments/assets/7ce432e0-cc69-4034-ac05-382509c92f4f)
