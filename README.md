# Power BI Sales Dashboard Project

This project demonstrates my creation of a comprehensive Power BI Sales Dashboard to provide insightful visualizations and analyses of sales performance. The dashboard enables users to understand key metrics such as total sales, profit, orders, and profit margins, while also allowing comparisons across different periods and categories.

## Objective

The objective of this project is to analyze and present comprehensive insights into sales data. The dashboard aims to:

- Calculate and display total sales.
- Calculate and visualize total profit.
- Analyze the number of orders placed.
- Calculate and visualize profit margin percentages.
- Compare sales by product and month with the previous year.
- Display the top 5 cities based on sales.
- Compare profit by sales channel with the previous year.
- Analyze sales by customer and compare with the previous year.
- Enable dynamic filtering through slicers for dates, cities, products, and channels.

## Steps to Follow for Creating the Power BI Sales Dashboard

### 1. Gather Data

I gathered the necessary data from various sources such as databases, spreadsheets, or web services, ensuring that the data is accurate and relevant to the project's objectives.

### 2. Power Query – Data Extract, Transform & Load (ETL)

I used Power Query Editor in Power BI to clean and transform the data. This involved:

- Removing duplicates
- Handling missing values
- Merging datasets
- Creating calculated columns

### 3. Create a Date Table

I created a date table in Power BI to utilize DAX time intelligence functions. I ensured that the Auto Date/Time option is turned off in Power BI settings for better performance.

### 4. Create Data Model in Power BI Desktop

I designed a data model to represent relationships between different tables. I established proper relationships, defined keys, and created hierarchies if needed. This step ensures accurate analysis and visualization.

### 5. Develop Reports in Power BI Desktop

I used Power BI Desktop to develop reports based on the data model. I added visualizations such as charts, tables, and maps to effectively represent the data. I applied filters, slicers, and drill-through functionalities to enable user interaction with the data.

#### Visuals Created:

1. **Sales By Product**: Compared sales with last year’s sales.
2. **Sales By Month**: Compared sales with last year’s sales.
3. **Sales of Top 5 Cities**: Visualized the top 5 cities based on sales.
4. **Compare Profit by Channel**: Compared profit with the previous year’s profit.
5. **Sales By Customer**: Compared sales with last year’s sales.
6. **Create Cards**: Displayed metrics for sales, profit, profit margin, and products sold.

### 6. Implementing DAX Calculations

I used Data Analysis Expressions (DAX) to create calculated columns, measures, and calculated tables for performing complex calculations and aggregations. DAX is a powerful formula language that allows manipulation of data within Power BI.

#### Example DAX Measures:

- **Total Sales**:
    ```DAX
    Sales = SUM(Sales_Data[Sales])
    ```
- **Previous Year Total Sales**:
    ```DAX
    Sales PY = CALCULATE([Sales], SAMEPERIODLASTYEAR(DateTable[Date]))
    ```
- **Difference Between Current Year Sales & Previous Year Sales**:
    ```DAX
    Sales vs PY = [Sales] - [Sales PY]
    ```
- **Percentage Increase or Decrease in Sales Year-on-Year (YOY%)**:
    ```DAX
    Sales vs py % = DIVIDE([Sales vs PY], [Sales], 0)
    ```
- **Products Sold**:
    ```DAX
    Products Sold = SUM(Sales_Data[Order Quantity])
    ```
- **Profit**:
    ```DAX
    Profit = SUM(Sales_Data[Profit])
    ```
- **Previous Year Profit**:
    ```DAX
    Profit LY = CALCULATE([Profit], SAMEPERIODLASTYEAR(DateTable[Date]))
    ```
- **Profit Difference with Previous Year**:
    ```DAX
    Profit Vs LY = [Profit] - [Profit LY]
    ```
- **Profit Percentage Difference with Previous Year**:
    ```DAX
    Profit vs LY % = DIVIDE([Profit Vs LY], [Profit], 0)
    ```
- **Profit Margin**:
    ```DAX
    Profit Margin = DIVIDE([Profit], [Sales], 0)
    ```
- **Total Cost**:
    ```DAX
    Total Cost = SUM(Sales_Data[Total Cost])
    ```

## Conclusion

The Power BI Sales Dashboard provides a robust and insightful view of sales data, enabling my organization to make data-driven decisions. With dynamic filtering, interactive reports, and advanced calculations, this dashboard helps optimize sales strategies and drive business success. Users can gain valuable insights into key sales metrics, trends, and comparisons across different dimensions and time periods.
