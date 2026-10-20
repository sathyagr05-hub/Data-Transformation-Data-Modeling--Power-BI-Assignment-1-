# Power BI Data Cleaning, Transformation & Data Modeling

## 📌 Project Overview

This project focuses on data import, data cleaning, data transformation, data aggregation, and data modeling using **Microsoft Power BI and Power Query Editor**.

As an aspiring Data Analyst, I created this project to develop practical skills in preparing raw datasets for analysis. The assignment covers data type conversion, text formatting, calculated columns, conditional columns, table merging, missing value handling, duplicate detection, sorting, filtering, grouping, aggregation, and relationship management.

The project uses three datasets: **List of Orders, Order Details, and Sales Target**.

## 🎯 Project Objectives

- Import CSV datasets into Power BI.
- Clean and transform data using Power Query Editor.
- Restrict rows and assign appropriate data types.
- Standardize customer names using Proper Case.
- Create calculated and conditional columns.
- Merge tables using common keys.
- Identify and handle missing values and duplicate records.
- Sort and filter order data.
- Group and aggregate data for analysis.
- Establish and validate relationships between tables.

## 🛠️ Tools & Technologies

- **Microsoft Power BI Desktop** — Data preparation and data modeling
- **Power Query Editor** — Data cleaning and transformation
- **CSV Files** — Source datasets
- **GitHub** — Project documentation and portfolio

## 📂 Datasets Used

### 1. List of Orders
Contains order-level information, including Order ID, Order Date, CustomerName, City, and State.

### 2. Order Details
Contains order-detail information, including Order ID and the available product, category, amount, and profit fields.

### 3. Sales Target
Contains sales target information, including Category and Target.

## 🔄 Project Workflow

### 1. Data Import

- Imported `List of Orders.csv` into Power BI.
- Opened Power Query Editor using **Home → Transform Data**.
- Imported `Order Details.csv` and `Sales Target.csv`.

### 2. Row Limiting & Data Types

- Restricted the List of Orders table to the first 500 rows.
- Changed `Order Date` to the Date data type.
- Changed `Amount` and `Target` to Fixed Decimal Number.

### 3. Text Formatting

- Converted the `CustomerName` column to Proper Case to maintain consistent capitalization.

### 4. Column Creation

**Location**

Merged the City and State columns to create a new column named `Location`, using the format:

`City, State`

**Profit Margin**

Created a custom column using the formula:

```text
Profit Margin = Profit / Amount
```

Formatted the resulting values as a percentage. Rows with zero or missing Amount values should be handled to avoid invalid calculations.

### 5. Conditional Column

Created a conditional column named `Profit Status` using the following business rules:

| Condition | Profit Status |
|---|---|
| Profit < 0 | Loss |
| Profit = 0 | Break-Even |
| Profit > 0 | Profit |

### 6. Merging Data

- Merged the List of Orders and Order Details tables using `Order ID`.
- Named the merged output table `Orders Data`.
- Expanded the required columns from the merged table.

### 7. Handling Missing Data & Duplicate Data

- Checked the tables for missing and null values.
- Evaluated appropriate strategies, including:
  - Replacing missing values when a valid replacement was justified.
  - Removing invalid records when necessary.
  - Retaining null values when the original information could not be verified.
- Checked for duplicate rows.
- Applied duplicate-handling decisions based on business logic.
- Preserved valid order-detail records when repeated Order IDs represented different products or line items.

### 8. Sorting & Filtering Data

- Sorted the `Orders Data` table by `Order Date` in descending order.
- Applied a State filter to analyze orders from Tamil Nadu.

### 9. Grouping & Aggregating Data

Duplicated the Order Details table and performed the following aggregations:

**Count of Order ID**
- Grouped records by Order ID.
- Counted the detail rows associated with each order.

**Average Profit by Category**
- Grouped records by Category.
- Calculated the average Profit for each category.

**Total Amount by Sub-Category**
- Grouped records by Sub-Category.
- Calculated the sum of Amount for each sub-category.

Duplicated the Sales Target table and aggregated total Target by month of Order Date using the relevant date field or relationship, where required.

### 10. Data Modeling

Established and checked relationships between the tables:

| Primary table | Related table | Relationship column |
|---|---|---|
| List of Orders | Order Details | Order ID |
| Order Details | Sales Target | Category |

Used **Manage Relationships** to verify relationship status, cardinality, and active relationships.

## 📊 Skills Demonstrated

- Data import and preparation
- Data cleaning and quality checks
- Missing value and duplicate handling
- Data type conversion
- Text transformation
- Custom and conditional columns
- Table merging and joins
- Sorting and filtering
- Grouping and aggregation
- Data modeling and relationship management
- Technical documentation

## 📁 Repository Structure

```text
Power-BI-Data-Cleaning-and-Transformation/
│
├── README.md
├── Dataset/
│   ├── List of Orders.csv
│   ├── Order Details.csv
│   └── Sales Target.csv
├── Screenshots/
│   ├── Data_Import.png
│   ├── Data_Cleaning.png
│   ├── Orders_Data_Merge.png
│   ├── Grouping_Aggregation.png
│   └── Data_Model.png
└── PowerBI/
    └── Power_Query_Assignment.pbix
```

*This is a suggested structure. Include only the folders and files you actually upload to GitHub.*

## 📈 Learning Outcomes

Through this project, I gained practical experience using Power BI and Power Query Editor to prepare raw data for analysis, apply data-cleaning techniques, create calculated columns, merge datasets, aggregate business information, and establish relationships between tables.

This assignment is part of my journey toward becoming a **Data Analyst** and building a portfolio of practical data analytics projects.

## 👤 About Me

I am an aspiring Data Analyst developing practical skills in data cleaning, data transformation, data visualization, and business intelligence using tools such as Microsoft Excel, Power BI, and SQL.

I use hands-on projects to strengthen my analytical thinking and demonstrate my learning through my GitHub portfolio.

## ⭐ Acknowledgment

This project was completed as a hands-on Power BI data import, transformation, and modeling assignment for learning and portfolio development.
