# construction_cost_analysis


### Project Overview

This project analyzes construction cost data to identify key spending patterns, major cost drivers, and supplier contributions. The goal is to support better cost control and supplier management decisions using interactive Power BI dashboards.

### The dataset contains construction cost records as listed below:

Category

Sub-category

Date

Supplier

Document

Sales_amount

year

### Data Cleaning & Preparation

####  Data cleaning was performed using Power Query in Power BI. The following steps were applied:

After importing the raw dataset into Power Query, the first step was removing columns containing only 'null' or irrelavant data pionts

Using 'Conditional Formatting' create a new column (Category), then on this same column, replace errors with null, fill down values and move the column to the beginning.

Create a new column; 'Add Column' - 'Extract' then extract the text-length and remove the column

Use 'If Condition' to apply the text-length and then create a new column - Sub_category

Correct the data type for each column then close and apply changes.

While on Power BI Table view' I created 'year' column- calculated column using (year = YEAR('Report'[Date]) )

### Measures & KPIs

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

### Tools Used

Power BI

Power Query

DAX

This analysis provides a clear understanding of construction spending behavior and supports data-driven decision-making for cost management and supplier evaluation.


Analyzed by: Ugwu Leeechi Juliet
