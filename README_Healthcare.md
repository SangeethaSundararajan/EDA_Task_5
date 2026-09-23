# Healthcare Data Analysis

## Project Overview

This project analyzes a healthcare dataset using Python and Pandas. The notebook performs basic data loading, inspection, data cleaning, date conversion, descriptive statistics, and exploratory analysis of patient and billing information.

## Dataset

The project uses the file:

`healthcare_raw.csv`

The dataset contains **500 rows and 9 columns**.

### Columns

- `Patient_ID` – Unique patient identifier
- `Gender` – Patient gender
- `Age` – Patient age
- `Medical_Condition` – Recorded medical condition
- `Admission_Date` – Patient admission date
- `Admission_Type` – Type of admission such as Routine, Urgent, or Emergency
- `Medical_Code` – Medical/ICD10 code
- `Billing_Amount` – Patient billing amount
- `Discharge_Date` – Patient discharge date

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab / Jupyter Notebook

## Project Workflow

### 1. Import Libraries

The project uses NumPy, Pandas, Matplotlib, and Seaborn for data processing and visualization.

### 2. Load the Dataset

The healthcare CSV file is loaded into a Pandas DataFrame.

```python
df = pd.read_csv("/content/healthcare_raw.csv")
```

### 3. Explore the Dataset

The notebook checks:

- Number of rows and columns
- Column names
- Dataset contents
- Data types
- Descriptive statistics

The dataset contains 500 records and 9 attributes.

### 4. Missing Value Handling

The `Medical_Code` column is checked for missing values. Missing values, if present, are replaced with:

```python
df["Medical_Code"] = df["Medical_Code"].fillna("Unknown")
```

The notebook then verifies that no missing values remain in this column.

### 5. Date Conversion

`Admission_Date` and `Discharge_Date` are converted from text values into Pandas datetime format for easier date-based analysis.

```python
df["Admission_Date"] = pd.to_datetime(df["Admission_Date"])
df["Discharge_Date"] = pd.to_datetime(df["Discharge_Date"])
```

### 6. Statistical Analysis

Descriptive statistics are generated for numerical columns such as:

- Age
- Billing_Amount

The dataset shows an average age of approximately **50.11 years** and an average billing amount of approximately **7249.00**.

## Key Dataset Information

| Attribute | Value |
|---|---:|
| Number of records | 500 |
| Number of columns | 9 |
| Average age | 50.11 |
| Minimum age | 22 |
| Maximum age | 78 |
| Average billing amount | 7249.00 |
| Minimum billing amount | 2300.00 |
| Maximum billing amount | 14200.00 |

## Purpose of the Project

The main purpose of this project is to practice healthcare data analysis using Python. It demonstrates how to load a dataset, understand its structure, check and handle missing values, convert date columns, and perform basic statistical analysis.

## How to Run

1. Open `Health_Care.ipynb` in Google Colab or Jupyter Notebook.
2. Upload `healthcare_raw.csv` to the working environment.
3. Run the notebook cells from top to bottom.
4. Review the data inspection, cleaning, and analysis outputs.

## Project Files

```text
Healthcare-Data-Analysis/
│
├── Health_Care.ipynb
├── healthcare_raw.csv
└── README.md
```

## Conclusion

This project provides a basic workflow for analyzing healthcare records with Python. It focuses on data understanding, cleaning, date handling, and descriptive statistics and can be extended with additional visualizations and deeper healthcare analysis.
