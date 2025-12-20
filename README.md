# construction_cost_analysis


### Project Overview

This project analyzes costruction cost data to identify spending patterns, top cost drivers, and supplier contributions using Power BI.

### Data Source
The dataset contains construction cost records such as Category, Sub_category, suppliers, document, sales_amount and dates.

### Data Cleaning Process

After importing the raw dataset into Power Query, the first step was removing columns containing only 'null' or irrelavant datapionts

Useing 'Conditional Formating' create a new column (Category), then on this same column, replace errors with null, fill down values and move the column to the beginning.

Create a new column; 'Add Column' - 'Extract' then extract the text-length and remove the column

Use 'If Condition' to apply the text-length and then create a new column - Sub_category

Correct the data type for each column then close and apply changes.

While on Power BI Table view' I created 'year' column- calculated column using (year = YEAR('Report'[Date]) )

Creating KPI - from click 'Enter Data' type 'KPIs' and click Load.

Create and store the calculated measures inside the KPI table-data: click to highlight the 'KPIs'  at the top-right of the screen

Click new measure and type: Average_Sales = AVERAGE(Report[Sales_amount])

Repeat the last 2 steps to create the Total Revenue and Total Suppliers respectively: Total_Sales = SUM(Report[Sales_amount]) and Total_Suppliers = COUNTA(Report[Supplier])
