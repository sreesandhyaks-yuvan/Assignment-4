# Assignment-4
Power BI_Data Transformation &amp; Data Modeling
Power Query Syntax for Data Transformation
Open Power BI Desktop → Home → Transform data → Power Query Editor.
Keep only the first 500 rows-  Menu: Home → Keep Rows → Keep Top Rows → 500
Change Order Date to Date type – Click on the left corner of the tab and select the Date function
Change Amount and Target to Fixed Decimal Number- Click on the left corner of the tab and select the Fixed decimal number function
Convert CustomerName to proper case- In Power BI query -Select CustomerName → Transform → Format → Capitalize Each Word & Also Trim and Clean
 Merge State and City into Location- In Add Column → Custom Column – Column name changed as” Location” and applied syntax =[City] & ", " & [State]
Created a new column as Profit Margin
In Add Column → Custom Column – Column name changed as” Profit margin” and applied syntax =profit/Amount and then click on the left corner of the tab and select the percentage function
Create Profit Status- In Add Column → Custom Column – Column name changed as” Profit Status” and applied syntax as;
=if [Profit] < 0 then "Loss"
else if [Profit] = 0 then "Break-Even"
else "Profit"
 Merge Orders Tables Using Order ID from List of Orders and Order Details tables into a new table renamed as Orders Data.
Select List of Orders.
Choose Home → Merge Queries → Merge Queries as New.
Select Order Details as the second table.
Select Order ID in both tables.
Choose Left Outer join to retain all rows from List of Orders.
Name the new query Orders Data.
Expand the merged column and select the columns required.
Handle Missing Values- select a table → View → Column quality. Check Valid, Error and Empty percentages. Filter individual columns to find null or blank values, then choose a suitable strategy.
Remove Duplicate Rows- Select the table and the columns that define a duplicate record → Home → Remove Rows → Remove Duplicates.
Grouping and Aggregating Data- Count rows for each Order ID- Power Query: Home → Group By → group by Order ID → new column Order Count → operation Count Rows. 
Total Amount by Sub-Category - Power Query: Home → Group By → group by Order ID → new column Order Count → operation sum – column Target.
Data Modeling — Relationships-
Relationship 1: List of Orders[Order ID] ↔ Order Details[Order ID]. 
Relationship 2: Order Details[Category] ↔ Sales Target[Category]. 
