## 🧹 Data Cleaning and Preprocessing: Netflix Content Analysis (Task 1)

This repository contains the methodology and final product for **Task 1: Data Cleaning and Preprocessing** for the **Netflix Movies and TV Shows** dataset. The goal was to clean, structure, and prepare the raw data for subsequent analysis or modeling.

### 🎯 Objective

To apply essential data cleaning techniques—including handling missing values, standardizing column names, removing duplicates, and correcting data types—to the provided raw dataset.

### 📂 Files

| File Name | Description |
| :--- | :--- |
| `BeforeClean.xlsx` | **Original Raw Dataset** (The data before cleaning). |
| `AfterClean.xlsx` | **Final Cleaned Dataset** (The data after processing). |
| `README.md` | This document, explaining the methodology. |

---

### 🔍 Summary of Cleaning Steps

The cleaning process ensured the data is structured and consistent, using the following transformations:

1.  **Column Standardization:** All column headers were standardized to **snake\_case** (e.g., `date_added`).
2.  **Duplicate Handling:** Checked for and confirmed **no exact duplicate rows** were present.
3.  **Missing Values (Imputation):** Null values in **`director`**, **`cast`**, and **`country`** were filled with the string **'Unknown'**.
4.  **Missing Values (Deletion):** Rows missing data in the critical fields **`date_added`** or **`rating`** (approx. 17 rows) were removed.
5.  **Feature Standardization:**
    * The original **`duration`** column (e.g., '93 min', '4 Seasons') was split into two new, clean columns: **`duration_int`** (numerical value) and **`duration_unit`** (unit type).
    * The **`date_added`** column was converted to a consistent datetime format.

---
