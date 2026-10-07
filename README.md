# Power-BI-Data-Transformation-and-Data-Modeling

**E-Commerce Sales Analysis using Power BI**

**Project Overview**

This project focuses on **E-Commerce Sales Analysis using Microsoft Power BI**. The project demonstrates the process of importing, transforming, cleaning, merging, aggregating, and modeling sales data using **Power Query and Power BI**.

The objective is to prepare the data for analysis by performing data transformation and data modeling operations and creating a structured dataset that can be used for further business analysis.

**Objectives**

The main objectives of this project are:

* Import multiple CSV datasets into Power BI.
* Perform data transformation using Power Query.
* Handle missing and duplicate data.
* Create calculated and conditional columns.
* Merge related datasets using `Order ID`.
* Sort and filter sales data.
* Perform grouping and aggregation.
* Establish relationships between tables.
* Prepare a structured data model for further analysis.

**Dataset**

The project uses three datasets and it contain information related to orders, customers, products/categories, sales amounts, profit, and sales targets.

1. List of Orders
 
2. Order Details

3. Sales Target

**Data Transformation**

The following transformations were performed using Power Query.

1. Restricting Rows

The `List of Orders` table was restricted to the **first 500 rows**.

2. Data Type Conversion

Appropriate data types were assigned to important columns:

* `Order Date` → Date
  
* `Amount` → Fixed Decimal Number
  
* `Target` → Fixed Decimal Number

3. Customer Name Formatting

The `CustomerName` column was converted to **Proper Case** to maintain consistent capitalization.

4. Creating Location

The `City` and `State` columns were combined into a new column named `Location` by using the merge function.

5. Profit Margin

A custom column named `Profit Margin` was created using the required formula.
The resulting column was formatted as a percentage.

6. Profit Status

A conditional column named `Profit Status` was created and specified conditions were given.

**Data Cleaning**

Missing Values

The datasets were checked for missing/null values using Power Query.

Duplicate Data

Duplicate records were checked in both the `List of Orders` and `Order Details` tables.

Repeated `Order ID` values were not automatically considered duplicates because a single order can contain multiple order-detail records.

Only exact duplicate rows were considered for removal.

**Data Merging**

The `List of Orders` and `Order Details` tables were merged and a new table Orders data was created.

**Sorting & Filtering**

The `Orders Data` table was used for sorting and filtering.

Sorting

Orders were sorted by:

Order Date → Descending

This helps identify the most recent orders.

Filtering

The data can be filtered by fields such as:

* State
  
* Order Date

* Category

For regional analysis, a state such as **Tamil Nadu** can be selected.

**Grouping & Aggregation**

The `Order Details` table was duplicated to perform aggregation tasks using **Group By**.

1. Count of Order ID

Orders were grouped by `Order ID` and the number of records for each order was calculated.

Group By → Order ID

Operation → Count Rows

2. Average Profit by Category

The data was grouped by `Category` and average profit was calculated.

Group By → Category

Operation → Average

Column → Profit

3. Total Amount by Sub-Category

The data was grouped by `Sub-Category` and total amount was calculated.

Group By → Sub-Category

Operation → Sum

Column → Amount

**Sales Target Aggregation**

The `Sales Target` table was duplicated and used for aggregation.

The total target amount was calculated based on the **Month of Order Date**.

This allows monthly sales targets to be compared during further analysis.

**Data Modeling**

Relationships were established between the tables.

The relationship between `Order Details` and `Sales Target` was checked through **Manage Relationships** and kept active.

**Project Outcome**

The project resulted in a structured and transformed e-commerce dataset ready for further analysis in Power BI.

The workflow demonstrates how raw sales data can be transformed into a cleaner and more organized data model using **Power Query and Power BI**.

