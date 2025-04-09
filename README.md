# BMW-Sales
![intro](https://github.com/Abhishekshaw2002/BMW-Sales/blob/73f657b048a6312dec87340c57e46b88f53b7345/Img%20used/BMW.svg.png)

# Problem Statement:
The automotive industry generates vast amounts of sales data, which, if analyzed effectively, can provide valuable insights into sales performance, customer preferences, and market trends. However, the data is often scattered across multiple files and lacks a centralized system for analysis. This project aims to address the challenge of consolidating and visualizing BMW car sales data from Excel files to provide actionable insights for decision-making.

# Objective:
The primary objectives of this project are:

To consolidate BMW car sales data from multiple Excel files into a single Power BI dashboard.
To create interactive visualizations that provide insights into sales performance, Top selling Models, Most expensive ones and Country & Channel wise sales.
To enable stakeholders to make data-driven decisions by providing a clear and intuitive dashboard.

# Technology Used in the Project:

Power BI Desktop: For data modeling, visualization, and report creation.
Microsoft Excel: For storing and managing raw data in three Excel files.
Power Query: For data transformation and cleaning.
DAX (Data Analysis Expressions): For creating calculated columns and measures.
Power BI Service: For publishing and sharing the report online.

# Scope of the Project:

Consolidate data from three Excel files: Sales Data, Car Data, and Country Data.
Create a relational data model to link the tables.
Develop interactive visualizations to analyze sales trends, country wise performance, and customer demographics.
Publish the report to Power BI Service for stakeholder access.


# Requirement Gathering for Visualization:
The following requirements were identified for the visualization:
Sales Performance: Total sales, sales by region, and sales by car model.
Product Analysis: Most Expensive sold car models and their profitability.
Time-Based Analysis: Weekdays, Monthly and yearly sales trends.

# Model Development:
Data Model:
Three tables were imported from Excel:
1. Sales Data: Contains transaction details (e.g., Sale ID, Date, Country ID, Model ID, Quantity, Revenue).
2. Country Data: Contains country details (e.g., Country Name, Region, Qty Sold, Cost, Revenue).
3. Car Data: Contains car model details (e.g., Model Name, Category, Price).
Relationships were established between the tables using Country ID and Model ID as keys.

Data Cleaning:
Removed duplicates and null values using Power Query.
Standardized data formats (e.g., date formats, currency).

7. DAX Queries used and Execution Results:

Avg Price DIVIDE ([Revenue], [Qty Sold]) 
(This query shows the average price of model}

Qty Sold SUM (factTable [Quantity Sold])
{This query shows the Quantity sold current year}

Qty Sold PY CALCULATE ([Qty Sold], DATEADD('Calendar' [Date], -1, YEAR)) 
{This query shows the Quantity sold in previous year}

Revenue SUM (factTable [Total]) 
{This query shows the Profit earned by specified model in current year}

Revenue PY CALCULATE ([Revenue], DATEADD('Calendar' [Date], -1, YEAR)) 
{This query shows the Profit earned by specified model in current year}

Revenue Growth DIVIDE ([Revenue Variance], [Revenue PY]) 
{This query shows the Revenue variance in Current year w.r.t Previous Year)

# Data Refresh and Schedule Refresh:
Data Refresh: The Excel files were refreshed manually in Power BI Desktop to ensure the latest data was used.
Schedule Refresh: After publishing the report to Power BI Service, a scheduled refresh was set up to update the data daily.

# Publish Report and Access Control:
The report was published to Power BI Service.
Access control was implemented to restrict access to authorized stakeholders.
Dashboards were shared with specific users and groups.

# Challenges Faced in the Project:
Data Inconsistency: Some records in the Excel files had missing or inconsistent data, which required cleaning.
Complex Relationships: Establishing relationships between multiple tables was initially challenging.
Performance Issues: Large datasets caused slow loading times, which were resolved by optimizing the data model.

# Future Improvement Scope:
Add more filters (e.g., by dealership, salesperson).
Incorporate predictive analytics to forecast future sales trends.
Enhance the dashboard with advanced visualizations (e.g., heatmaps, drill-throughs).

# Conclusion:
This Power BI project successfully consolidated and analyzed BMW car sales data from multiple Excel files, providing actionable insights through interactive visualizations. The dashboard enables stakeholders to make data-driven decisions, improving sales performance and customer satisfaction. With future enhancements, the project can further streamline sales analysis and forecasting.

# Screenshot: 
Include screenshot of the Power Bi dashboard ,data model and visualiZations. 
![intro](https://github.com/Abhishekshaw2002/BMW-Sales/blob/73f657b048a6312dec87340c57e46b88f53b7345/Img%20used/BMW%20dashboard.png)
![intro](https://github.com/Abhishekshaw2002/BMW-Sales/blob/73f657b048a6312dec87340c57e46b88f53b7345/Img%20used/bmw%20dasboard%202.png)

