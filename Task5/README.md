# 🚢 Titanic Survival Prediction: Exploratory Data Analysis (EDA)

This repository contains the Exploratory Data Analysis (EDA) performed on the Titanic dataset (`train.csv`) to understand the factors influencing survival and prepare the data for a machine learning model.

---

## 🎯 Objective

The primary goal of this analysis is to:
1.  **Understand the data** and its characteristics.
2.  **Identify patterns** and correlations, especially with the target variable, **`Survived`**.
3.  **Clean and prepare** the data by handling missing values and engineering new, more informative features.

---

## 💾 Dataset Overview

The analysis uses the classic **Titanic survival dataset** (`train.csv`). Key columns include:

| Feature | Description |
| :--- | :--- |
| **`Survived`** | Target variable (0 = No, 1 = Yes) |
| **`Pclass`** | Passenger Class (1st, 2nd, 3rd) |
| **`Sex`** | Passenger gender |
| **`Age`** | Passenger age |
| **`SibSp`** | # of siblings/spouses aboard |
| **`Parch`** | # of parents/children aboard |
| **`Fare`** | Passenger fare |
| **`Cabin`** | Cabin number |
| **`Embarked`** | Port of Embarkation (C, Q, S) |

---

## ✨ Key Analysis Steps & Feature Engineering

The `EDA.ipynb` notebook covers the following core steps:

### 1. Data Cleaning and Imputation
* **Missing Value Handling:**
    * **`Age`**: Imputed missing values using the **median age** specific to the passenger's **`Sex`** and **`Pclass`**.
    * **`Embarked`**: Imputed missing values with the **mode** (most frequent value).
    * **`Fare`**: Imputed the single missing value with the **median fare**.
    * **`Cabin`**: The column has a high percentage of missing values and was mostly dropped or used to extract the **Cabin Deck**.

### 2. Feature Engineering
* **`FamilySize`**: Created by summing **`SibSp`** and **`Parch`**, plus one (for the passenger themselves).
* **`Family_Group`**: Categorized passengers into survival groups based on `FamilySize`: **Alone**, **Small**, **Medium**, and **Large**.
* **`Title`**: Extracted the **title** (e.g., 'Mr.', 'Miss.', 'Master.', 'Mrs.') from the **`Name`** column for better grouping and imputation.
* **`Deck`**: Extracted the **first letter** of the **`Cabin`** to represent the deck level.

### 3. Visual Analysis
* Survival rates were analyzed against key features: **`Sex`**, **`Pclass`**, **`Family_Group`**, **`Age`** bins, and **`Fare`** distribution.

---

## 📈 Key Findings (Conclusions)

* **Gender:** **Females** had a significantly higher survival rate than males (following the "Women and children first" protocol).
* **Class:** **First-class** passengers had the highest survival rate, and third-class had the lowest, indicating a strong correlation with wealth/status.
* **Family Size:** Passengers traveling in **Small** or **Medium** family groups had the best survival chances, while those traveling **Alone** or in **Large** groups fared worse.
* **Title:** The Title feature provides strong predictive power, especially for children ('Master' / 'Miss') and married women ('Mrs.').

---

## 🛠️ Requirements

The analysis was performed using standard Python libraries, including:
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
