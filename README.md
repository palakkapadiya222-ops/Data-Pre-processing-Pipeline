# Data-Pre-processing and Transformation-Pipeline

Multi-Source Data Preprocessing & Transformation Pipeline

A Python data pipeline designed to clean, transform, and merge environmental metrics with global employee data sourced from Kaggle.

## 📊 Overview
This repository contains a modular preprocessing pipeline built using **Pandas** and **NumPy**. It processes two primary datasets:
1. **Global AQI Dataset**: Regional air quality indices, pollutant levels, and country mappings.
2. **Employee Records & Salary Dataset**: Multi-national workforce data containing attributes like Name, Age, and Salary across various countries.

The pipeline cleans the raw data, applies advanced transformations, and combines them into ready-to-use files for analysis.

---

## ✅ Key Features & Pipeline Steps

### 1. Data Cleaning & Type Casting
* **String Standardization**: Cleans spaces and fixes capitalisation for names and countries.
* **Handling Duplicates**: Removes repetitive records from employee logs.
* **Data Type Coercion**: Fixes data types (e.g., changes text to numbers for age and salary).

### 2. Feature Engineering & Transformations
* **Mathematical Operations**: Computes custom scales and new mathematical metrics.
* **Aggregations & Groupby**: Groups data by country to calculate averages.
* **Schema Evolution**: Renames columns to make them easy to understand.

### 3. Advanced Reshaping & Merging
* **Data Concatenation**: Stacks separate data logs into a single historical sheet.
* **Pivoting Tables**: Reshapes tables to see salary bands across different countries.
* **Relational Merging**: Merges employee data with country AQI records based on location.

### 4. Basic Data Visualization
* Generates exploratory charts to inspect data distributions and outliers.

---

## 🔎 Repository Structure
```text
├── data/
│   ├── raw/                  # Downloaded raw CSVs from Kaggle
│   └── processed/            # Cleaned, merged, and pivoted outputs
├── notebooks/                # Experimental EDA & transformation notebooks
├── src/
│   ├── clean.py              # String handling, deduplication, and type casting
│   ├── transform.py          # Math scaling, groupby, merge, pivot, and concat
│   └── visualize.py          # Plotting scripts for data distribution
├── main.py                   # Central pipeline execution script
└── README.md
```

---

## 🛠 Getting Started

### Prerequisites
Make sure you have Python installed along with the required libraries:
```bash
pip install pandas numpy matplotlib seaborn
```

### Running the Pipeline
Place your Kaggle CSV files into the `data/raw/` folder and run:
```bash
python main.py
```
