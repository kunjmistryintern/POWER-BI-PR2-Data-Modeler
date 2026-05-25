# POWER-BI-PR2-Data-Modeler

## 📌 Project Overview

This project demonstrates the design and implementation of a professional **Star Schema Data Model** in Microsoft Power BI using multiple Excel datasets.

The project focuses on:

- Data Modeling
- Relationship Building
- Power Query ETL Process
- Cardinality Management
- Hierarchies
- Filter Flow Handling
- Data Verification using Matrix Tables

The objective of this project was to understand and implement industry-standard Power BI data modeling practices without using advanced DAX calculations or dashboard visualizations.

---

# 🛠 Tools & Technologies

- Microsoft Power BI
- Power Query Editor
- Excel Dataset Files
- Data Modeling Techniques

---

# 📂 Project Structure

```bash
POWER-BI-PR2-Data-Modeler/
│
├── Dataset/
│   ├── Sales_Fact.xlsx
│   ├── Customer_Dim.xlsx
│   ├── Product_Dim.xlsx
│   ├── Region_Dim.xlsx
│   ├── Date_Dim.xlsx
│   └── Returns_Fact.xlsx
│
├── Screenshot/
│   ├── 01_PowerQuery.png
│   ├── 02_StarSchema.png
│   ├── 03_Hierarchies.png
│   ├── 04_VerificationMatrix.png
│   └── 05_InactiveRelationship.png
│
├── Data_Modeler_Project.pbix
├── Power_BI_Data_Model_Summary.pdf
└── README.md
```

---

# 🧩 Data Model Design

## ⭐ Schema Type

A **Star Schema** was implemented using:

### Fact Tables
- `Sales_Fact`
- `Returns_Fact`

### Dimension Tables
- `Customer_Dim`
- `Product_Dim`
- `Region_Dim`
- `Date_Dim`

`Sales_Fact` was used as the primary central fact table connected with all dimension tables.

`Returns_Fact` was implemented as a secondary fact table for return analysis and inactive relationship scenarios.

---

# 🔗 Relationships Created

| From Table | To Table | Relationship Type |
|---|---|---|
| Sales_Fact | Customer_Dim | Many-to-One |
| Sales_Fact | Product_Dim | Many-to-One |
| Sales_Fact | Region_Dim | Many-to-One |
| Sales_Fact | Date_Dim | Many-to-One |
| Returns_Fact | Sales_Fact | Many-to-One |
| Returns_Fact | Date_Dim | Inactive Relationship |

### Relationship Configuration
- Single-direction cross filtering was used
- Active and inactive relationships were implemented
- Ambiguous filter paths were avoided using proper relationship management

---

# ⚙️ ETL & Data Transformation

The following ETL operations were performed using Power Query:

- Imported all Excel source files
- Removed blank rows and unnecessary records
- Applied correct data types
- Cleaned inconsistent values
- Renamed columns for better readability
- Created MonthNumber column for proper month sorting
- Performed basic data transformation and formatting

---

# 📊 Hierarchies Created

## 📅 Date Hierarchy
```text
Year → Quarter → Month → Date
```

## 🌍 Region Hierarchy
```text
Country → State → City
```

## 📦 Product Hierarchy
```text
Category → Subcategory → ProductName
```

These hierarchies were created to enable structured drill-down analysis.

---

# ✅ Data Verification

Matrix tables were used to verify relationships and filter propagation across the data model.

## Verification Matrices

### 1. Sales by Product Category and Region
- Verified Product and Region relationships
- Validated aggregation logic

### 2. Return Reasons by Fiscal Year
- Verified inactive relationship behavior
- Validated return analysis structure

### 3. Revenue by Customer Segment
- Verified Customer dimension relationship
- Confirmed revenue aggregation functionality

---

# 📷 Project Screenshots

The project includes screenshots for:

- Power Query Transformations
- Star Schema Model View
- Relationship Configuration
- Hierarchies
- Matrix Verification Tables
- Inactive Relationship Example

---

# 📁 Deliverables

The following files are included in this project:

- `.pbix` Power BI Project File
- Deliverables Summary PDF
- Dataset Files
- Project Screenshots
- README Documentation

---

# 🚀 Learning Outcomes

This project helped in understanding:

- Star Schema Modeling
- Fact and Dimension Tables
- Relationship Cardinality
- Cross Filter Direction
- Active vs Inactive Relationships
- Data Cleaning using Power Query
- Hierarchy Design
- ETL Process in Power BI
- Matrix-Based Relationship Verification

---

# 📌 Key Features

- Professional Star Schema Design
- Proper Relationship Handling
- Inactive Relationship Implementation
- Hierarchical Data Structure
- Clean ETL Workflow
- Verification using Matrix Tables
- Optimized Data Model Layout

---

# 👨‍💻 Author

## Kunj Mistry
Power BI ETL & Data Modeling Project

---

# 📜 Conclusion

This project successfully demonstrates ETL processing, Power BI data modeling, relationship management, hierarchy creation, and professional Star Schema implementation using Power Query and Model View in Microsoft Power BI.
