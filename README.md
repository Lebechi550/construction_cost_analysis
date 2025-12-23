# construction_cost_analysis


### Project Overview

This project analyzes construction cost data to identify key spending patterns, major cost drivers, and supplier contributions. The goal is to support better cost control and supplier management decisions using interactive Power BI dashboards.

### Data Sources:
construction_cost: The primary dataset used for this analysis is a Microsoft Excel Comma separated values file which contains records as listed below:

- Category
- Sub-category
- Date
- Supplier
- Document
- Sales_amount
- year

### Tools
- Power BI for:
  - Data cleaning
  - Data analysis
  - Creating report/dashboard 

### Data Cleaning & Preparation

####  Data cleaning was performed using Power Query in Power BI. The following steps were taken:

After importing the raw dataset into Power Query, I removed columns containing only 'null' or irrelavant data pionts

Created Category column using Conditional logic, then on this same column, replace errors with null, fill down values and moved the column to the beginning.

Created Sub_category column using text-length: Add Column - Extract then extract the text-length and remove the column

Used IF Conditional logic to apply the text-length and then created the column - Sub_category

Corrected the data type for each column and applied changes

While on Power BI Table view' I created 'year' column- calculated column using (year = YEAR('Report'[Date]) )

### Data Analysis

####  Key performance indicators were created using DAX to track business performance:

Average Sale:  Average_Sales = AVERAGE(Report[Sales_amount])

Total Revenue: Total_Sales = SUM(Report[Sales_amount])

Total_Suppliers = COUNTA(Report[Supplier])

These KPIs provide a high-level overview of cost distribution and supplier activity.


### Dashboard Insights

#### The dashboard highlights:

Revenue distribution by category and sub-category

Cost trends over time

Top contributing suppliers

Overall cost performance using KPIs

These insights help identify high-cost areas and opportunities for cost optimization.


This analysis provides a clear understanding of construction spending behavior and supports data-driven decision-making for cost management and supplier evaluation.


Analyzed by: Ugwu Leeechi Juliet
