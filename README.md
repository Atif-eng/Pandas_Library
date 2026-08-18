# Pandas for Data Manipulation

**Pandas** is a powerful open-source Python library for data analysis and manipulation.  
It provides fast, flexible, and expressive data structures designed to work with structured and time-series data.

## Key Features

- **Read Data**: Load data from CSV, Excel, SQL, JSON, Parquet and more
- **Filter Data**: Select, slice, and filter rows and columns with boolean indexing
- **Preprocess Dataset**: Handle missing values, duplicates, data types, and feature engineering
- **Merge Datasets**: Join, concatenate, and merge multiple DataFrames
- **Window Functions**: Rolling, expanding, and time-based window operations
- **Aggregate Data**: GroupBy, pivot tables, and summary statistics

pandas-examples/
├── data/
│   └── dataset.csv
├── notebooks/
│   └── data_cleaning.ipynb
├── src/
│   └── utils.py
└── README.md

## Installation

```bash
pip install pandas


import pandas as pd

# 1. Read data
df = pd.read_csv('dataset.csv')

# 2. Filter data
filtered_df = df[df['Age'] > 30]

# 3. Preprocess dataset
df['Salary'].fillna(df['Salary'].mean(), inplace=True)
df.drop_duplicates(inplace=True)

# 4. Merge two datasets
merged_df = pd.merge(df1, df2, on='ID', how='inner')

# 5. Window function
df['Rolling_Avg'] = df['Sales'].rolling(window=7).mean()

# 6. Aggregate data
summary = df.groupby('Department')['Salary'].agg(['mean', 'sum', 'count'])


