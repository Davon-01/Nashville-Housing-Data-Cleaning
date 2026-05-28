# Nashville Housing - Data Cleaning Portfolio Project (SQL)

## 📌 Project Overview
This project focuses on the data preparation and preprocessing phases of data analysis using **Microsoft SQL Server**. Raw housing data containing over 56,000 rows was systematically cleaned and modified to transform it from a raw, unorganized state into a structured format optimized for analysis and business intelligence reporting.

## 🛠️ Technical Skills Demonstrated
* **Data Standardization:** Converted inconsistent date-time fields into clean, uniform historical date formats using `CONVERT()`.
* **Handling Missing Values:** Implemented self-joins and conditional logic (`ISNULL()`) to populate missing property addresses by referencing matching duplicate records.
* **String Manipulation & Parsing:** Utilized advanced string functions (`SUBSTRING`, `CHARINDEX`, `REPLACE`, and `PARSENAME`) to break down combined address strings into separate, atomic columns for Address, City, and State.
* **Data Categorization Consistency:** Standardized messy categorical data fields by using `CASE WHEN` statements to clean up entry discrepancies (converting single characters like 'Y' and 'N' into full 'Yes' and 'No' values).
* **Database Optimization & De-duplication:** Wrote Common Table Expressions (CTEs) combined with window functions (`ROW_NUMBER() OVER(PARTITION BY...)`) to isolate and permanently remove duplicate rows from the database.
* **Schema Refinement:** Altered existing database metadata tables to create structured columns, concluding the pipeline by safely dropping redundant legacy attributes to optimize storage space.

## 💾 Dataset Source
The dataset utilized in this project is the **Nashville Housing Dataset**, which contains historical real estate records from the region.
* [Link to Raw Dataset](https://github.com/AlexTheAnalyst/PortfolioProjects/blob/main/Nashville%20Housing%20Data%20for%20Data%20Cleaning.xlsx)

## 🚀 How to Execute the Project
1. Download the raw `.xlsx` file from the data link above.
2. Import the raw dataset into your local instance of SQL Server using the SQL Server Import and Export Wizard.
3. Open the `Nashville_Housing_Data_Cleaning.sql` script in SQL Server Management Studio (SSMS).
4. Run the queries sequentially. Note that because the final step permanently drops the unparsed legacy columns to clean up the schema, the script is optimized to run exactly once on the raw data.
