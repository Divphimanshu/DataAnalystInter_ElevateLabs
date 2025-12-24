# 🏅 Olympic Games Data Analysis Project

## 🎯 Project Goal

The primary goal of this project is to analyze the historical Olympic Games dataset to answer specific questions related to medal counts and athlete demographics using SQL queries executed in MySQL Workbench.

---

## 💾 Dataset Description

This project utilizes two primary datasets related to the Olympic Games history:

### 1. `athlete_events` Table (Source: `athlete_events.csv`)

This table contains detailed records of all athletes and events from 1896 to 2016.

| Field | Description | Data Type (MySQL) |
| :--- | :--- | :--- |
| **ID** | Unique number for each athlete | `INT` |
| **Name** | Athlete's name | `VARCHAR` |
| **Sex** | Male (M) or Female (F) | `VARCHAR` |
| **Age** | Age of the athlete in that event | `INT` |
| **NOC** | National Olympic Committee 3-letter code (Key) | `VARCHAR` |
| **Year** | Year of the Games | `INT` |
| **Season** | Summer or Winter | `VARCHAR` |
| **Sport** | Sport played | `VARCHAR` |
| **Medal** | Gold, Silver, Bronze, or 'NA' (No Medal) | `VARCHAR` |

### 2. `regions` Table (Source: `country_definitions.csv`)

This table provides definitions for the NOC codes, mapping them to regions.

| Field | Description | Data Type (MySQL) |
| :--- | :--- | :--- |
| **NOC** | National Olympic Committee 3-letter code (Key) | `VARCHAR` |
| **region** | Country name used for geospatial mapping | `VARCHAR` |
| **notes** | Real country name if 'region' isn't an exact match | `VARCHAR` |

---

## 💻 Setup and Execution

### Prerequisites

1.  **MySQL Server:** A running instance of a MySQL database.
2.  **MySQL Workbench:** Used for database connection and query execution.
3.  **Data Files:** The provided CSV files (`athlete_events.csv` and `country_definitions.csv`).

### Steps Executed

1.  A new schema named `olympics_data` was created in MySQL Workbench.
2.  The provided CSV files were imported into the `olympics_data` schema using the **Table Data Import Wizard**, creating the tables `athlete_events` and `regions`.
3.  The following SQL tasks were executed in the `olympics_data` schema.

---


ORDER BY
    Total_Medals DESC
LIMIT 5;
