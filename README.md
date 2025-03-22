# 📊 ETL for Simple Dimension Tables – Project

## 📌 Overview
This project demonstrates a complete ETL (Extract, Transform, Load) pipeline using **SQL Server Integration Services (SSIS)**. The pipeline populates a `Date Dimension` table in the **AdventureWorks** data warehouse by importing and transforming a CSV file.

## 🛠️ Technologies Used
- SQL Server Integration Services (SSIS)
- SQL Server
- Flat File Source (CSV)

## 🔄 ETL Flow Summary

### 1. Extract
- Source data is read from a CSV file.
- Includes `DateKey` and other raw date-related attributes.

### 2. Transform
- Convert `DateKey` from string to integer.
- Extract and format:
  - `Year`, `Month`, `Day`
  - `FullDate` (concatenated and casted to date)
- Derive additional attributes:
  - `Quarter`
  - `EnglishMonthName`
  - `EnglishDayName`
  - `DayOfWeek`
  - Placeholder for `IsHoliday` (currently NULL)

### 3. Load
- Transformed data is loaded into the `DimDate` table in the data warehouse.

## 📸 SSIS Workflow Screenshots

1. **Control Flow**  
   Displays the high-level ETL sequence for:
   - `DimDate`
   - `DimSalesPerson`
   - `Fact Table`

2. **Data Flow – Part 1**  
   - Extract from CSV  
   - Convert `DateKey` and extract date components

3. **Data Flow – Part 2**  
   - Format `FullDate`, derive names and other attributes  
   - Final transformation before loading

4. **SQL Output**  
   - Preview of inserted rows in the `DimDate` table  
   - Includes all computed fields

## 📂 Output
Download the full PDF summary with visuals here:  
📄 [ETL_Project_Summary.pdf](./ETL_Project_Summary.pdf)

---

Feel free to clone, reuse, or modify this ETL workflow for your own data warehouse needs!
