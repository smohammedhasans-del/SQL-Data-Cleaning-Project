# SQL Data Cleaning & Exploratory Data Analysis

## 📌 Project Overview

This project focuses on cleaning and analyzing a **layoffs dataset** using SQL.

The main objective is to transform raw and inconsistent data into a clean, structured dataset that can be used for further analysis and reporting.

The project demonstrates practical SQL skills including data cleaning, duplicate removal, handling NULL values, standardization, data transformation, and exploratory data analysis.

---

## 🎯 Objectives

* Clean and prepare raw layoffs data
* Remove duplicate records
* Identify and handle NULL and blank values
* Standardize inconsistent data
* Create a staging table for data cleaning
* Transform date fields into a usable format
* Prepare a cleaned dataset for analysis
* Perform exploratory analysis using SQL

---

## 🗂️ Dataset

The project uses a layoffs dataset containing information about companies and employee layoffs.

### Key Columns

* `company`
* `location`
* `industry`
* `total_laid_off`
* `percentage_laid_off`
* `date`
* `stage`
* `country`
* `funds_raised_millions`

---

## 🧹 Data Cleaning Process

The raw dataset was processed through the following steps:

### 1. Create Staging Table

A staging table was created to preserve the original dataset while performing cleaning operations.

```sql
CREATE TABLE layoffs_staging
LIKE layoffs;
```

### 2. Insert Raw Data

The raw data was copied into the staging table for cleaning.

```sql
INSERT INTO layoffs_staging
SELECT *
FROM layoffs;
```

### 3. Remove Duplicate Records

Duplicate records were identified and removed to improve data quality.

### 4. Standardize Data

Inconsistent values were standardized to maintain consistency across the dataset.

Examples include:

* Company names
* Industry values
* Country names
* Text formatting

### 5. Handle NULL and Blank Values

Missing and blank values were identified and handled based on the available information.

### 6. Clean Date Values

Date fields were converted into a consistent date format for analysis.

### 7. Remove Unnecessary Data

Columns or records that were not useful for the analysis were removed where appropriate.

---

## 📊 Exploratory Data Analysis

After cleaning the data, SQL queries were used to explore the dataset.

The analysis includes:

* Maximum total layoffs
* Maximum percentage of layoffs
* Companies with the highest layoffs
* Companies with 100% layoffs
* Total layoffs by company
* Date range of the dataset
* Layoff trends and company-level analysis

Example:

```sql
SELECT company, SUM(total_laid_off)
FROM layoffs_staging2
GROUP BY company
ORDER BY 2 DESC;
```

---

## 🛠️ Tools & Technologies

* **SQL**
* **MySQL**
* **GitHub**
* **CSV Dataset**

### SQL Concepts Used

* `CREATE TABLE`
* `INSERT INTO`
* `SELECT`
* `UPDATE`
* `DELETE`
* `CASE`
* `GROUP BY`
* `ORDER BY`
* Aggregate Functions
* Window Functions
* CTEs
* Data Cleaning
* Data Transformation

---

## 📁 Project Structure

```text
SQL-Data-Cleaning-Project/
│
├── layoffs.csv
├── Data Cleaning.sql
├── Exploratory Date Analysis.sql
├── README.md
└── LICENSE
```

---

## 💡 Key Learning Outcomes

Through this project, I practiced:

* Working with real-world messy datasets
* Writing SQL queries for data cleaning
* Handling duplicates and missing values
* Standardizing inconsistent data
* Creating staging tables
* Performing exploratory data analysis
* Using SQL to prepare data for business analysis

---

## 👨‍💻 Author

**S. Mohammed Hasan**

B.Com Student | Aspiring Data Analyst

GitHub:
https://github.com/smohammedhasans-del
