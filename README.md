# 🎓 AICTE Oasis Infobyte Internship Program

## 📊 Task 3: Cleaning Data — Employee Dataset

**Domain:** Data Analytics  
**Project Type:** Data Cleaning and Preprocessing  
**Tools:** Python, Pandas, NumPy, Jupyter Notebook  
**Dataset:** Messy Employee Dataset

---

## 📌 Project Overview

This project was completed as part of the **AICTE Oasis Infobyte Internship Program**.

The objective was to transform a deliberately messy employee dataset into a clean, structured, and analysis-ready dataset using Python and its data analysis libraries.

The project focuses on identifying data quality issues, handling missing values, validating phone numbers, removing duplicate records where necessary, standardising inconsistent values, detecting numerical outliers, correcting data types, and documenting the cleaning process.

The project also includes a data quality report and a before-and-after comparison to evaluate the effectiveness of the cleaning process.

## 🎯 Objectives

- Inspect the original dataset and identify data quality issues.
- Generate a data quality report covering missing values, duplicates, data types, and numerical ranges.
- Apply appropriate missing-value handling strategies.
- Identify and remove duplicate rows where present.
- Standardise text values and date formats.
- Validate phone numbers and handle invalid entries.
- Detect numerical outliers using the Interquartile Range (IQR) method.
- Correct column data types.
- Compare dataset quality before and after cleaning.
- Export the cleaned dataset to a new CSV file.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Data cleaning and preprocessing |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical operations |
| Jupyter Notebook | Interactive coding and documentation |
| CSV | Dataset input and output |
| GitHub | Project documentation and version control |

## 📂 Project Directory Structure
|----|-----|
AICTE-Oasis-Infobyte-Task-3-Data-Cleaning/
│
├── Data/
│   └── cleaned_employee_data_final.csv
│
├── notebook/
│   └── 01_data_cleaning.ipynb
│
├── reports/
│   ├── data_quality_report.csv
│   └── before_after_summary.csv
│
└── README.md

**Folder description:**

Data/ — Contains the final cleaned employee dataset in CSV format.

notebook/ — Contains the Jupyter Notebook with the complete data cleaning workflow and documentation.

reports/ — Contains the data quality report and before-and-after comparison summary.

README.md — Documents the project objective, methodology, technologies, and results.

## 📊 Dataset Information

The original dataset was named `Messy_Employee_dataset.csv`.

| Attribute | Initial finding |
|---|---|
| Total rows | 1,020 |
| Total columns | 12 |
| Missing Age values | 211 |
| Missing Salary values | 24 |
| Exact duplicate rows | 0 |
| Phone numbers | Negative and invalid values identified |
| Date field | `Join_Date` required datetime conversion |
| Employee identifier | `Employee_ID` required string formatting |

These figures describe the initial dataset inspection. Final values should be taken from the exported reports after the notebook has been executed successfully.

## 🔍 Data Cleaning Methodology

### 1. Data Loading and Initial Inspection

- Imported Pandas and NumPy.
- Loaded the original CSV dataset.
- Inspected the dataset shape, column names, data types, and sample records.
- Created a working copy to preserve the original data.

### 2. Data Quality Assessment

- Counted missing values in each column.
- Checked for duplicate rows.
- Examined data types and unique values.
- Inspected minimum and maximum values in numerical columns.
- Identified suspicious and invalid phone number entries.

### 3. Missing Data Handling

- Examined missing values in `Age` and `Salary`.
- Used median imputation where appropriate, considering the numerical distributions and potential outliers.
- Evaluated missing and invalid values in other columns according to their meaning.
- Verified missing-value counts after applying the selected strategies.

### 4. Duplicate Removal

- Identified exact duplicate rows using Pandas.
- The initial dataset contained zero exact duplicate rows.
- Verified the duplicate count after cleaning.

### 5. Data Standardisation

- Removed unnecessary leading and trailing whitespace from text fields.
- Standardised applicable categorical values.
- Converted `Join_Date` to a datetime data type.
- Normalised employee identifiers to string format.

### 6. Phone Number Validation

- Investigated negative and invalid phone number values.
- Validated phone entries against the expected 10-digit Indian mobile number format.
- Identified valid and invalid phone records.
- Applied the documented handling strategy and checked the resulting column.

Invalid phone numbers should not be treated as valid simply because they are numeric. Any missing or unresolved phone values must be reported accurately in the final quality report.

### 7. Outlier Detection

Used the **Interquartile Range (IQR)** method to identify potential outliers in applicable numerical columns.

The calculation uses:

- Q1: First quartile
- Q3: Third quartile
- IQR: Q3 − Q1
- Lower bound: Q1 − 1.5 × IQR
- Upper bound: Q3 + 1.5 × IQR

Flagged values were evaluated before deciding whether to retain, correct, cap, or remove them. Unusual values were not automatically assumed to be errors.

### 8. Data Type Correction

- Converted `Employee_ID` to a string type.
- Converted `Join_Date` to datetime.
- Ensured numerical columns used appropriate numeric types.
- Checked text, categorical, and Boolean columns where applicable.

### 9. Before-and-After Comparison

Prepared a summary to compare the dataset before and after cleaning, covering:

- Row count and column count
- Total missing values
- Duplicate row count
- Columns containing missing values
- Column data types

The comparison helps demonstrate the changes made during the cleaning process.

### 10. Exporting the Results

Saved the final cleaned dataset separately from the original dataset.

Expected output files:

- `cleaned_dataset.csv`
- `data_quality_report.csv`
- `before_after_summary.csv`

The output files should be regenerated from the final notebook run so that the reported results match the submitted dataset.

## 📈 Expected Outcomes

The project demonstrates the ability to:

- Assess data quality systematically.
- Handle missing and invalid values using appropriate strategies.
- Standardise inconsistent text and dates.
- Detect duplicates and numerical outliers.
- Validate data types and business rules.
- Document cleaning decisions.
- Produce reusable data quality reports.
- Prepare structured datasets for further analysis and visualisation.

## 💼 Business Relevance

Employee data quality is important for reliable HR reporting and workforce analytics.

Incorrect dates, invalid phone numbers, missing salary values, and inconsistent identifiers can affect employee records, reporting accuracy, and downstream analysis.

This project demonstrates a structured approach to improving data reliability before using the dataset for business intelligence or analytics.

## ▶️ How to Run the Project

1. Install Python and Jupyter Notebook.
2. Install the required libraries:

   ```bash
   pip install pandas numpy jupyter
   ```

3. Place the original dataset in `data/raw/`.
4. Open `notebooks/01_data_cleaning.ipynb`.
5. Update the input and output paths if necessary.
6. Run all notebook cells in sequence.
7. Review the quality report, cleaning decisions, and validation results.
8. Verify that the cleaned CSV and comparison reports have been saved.

## 📚 Key Learnings

- Data quality assessment using Pandas.
- Missing-value analysis and imputation.
- Duplicate detection and validation.
- Text and date standardisation.
- Phone number validation.
- IQR-based outlier detection.
- Data type conversion and validation.
- Reproducible data cleaning workflows.
- Technical documentation and GitHub project organisation.

## 👩‍💻 Author

**Golla Bhumika**

Aspiring Data Analyst | Python | SQL | Excel | Power BI

## 🏁 Conclusion

This project demonstrates a systematic data cleaning workflow as part of the AICTE Oasis Infobyte Internship Program. It emphasises data quality assessment, documented decisions, validation, and reproducibility to prepare employee data for reliable downstream analysis.

**Internship:** AICTE Oasis Infobyte Internship Program  
**Task:** Task 3 — Cleaning Data
