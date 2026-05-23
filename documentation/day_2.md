# Day 2 — Advanced Pandas & Real Dataset Analysis

## Objective

The objective of Day 2 was to move beyond basic DataFrames and begin working with more realistic datasets professionally.

The session focused on:
- messy data,
- transaction analytics,
- datetime handling,
- missing values,
- grouping,
- aggregations,
- fraud analytics,
- and business intelligence thinking.

---

# Topics Covered

## 1. Realistic Transaction Dataset Creation

Created a banking-style transaction dataset containing:
- transaction IDs,
- customer names,
- branches,
- transaction amounts,
- transaction dates.

Important observations:
- customers repeated,
- branches repeated,
- missing values existed,
- dates became critical for analysis.

---

## 2. Data Inspection

Used:

```python
df.info()
df.describe()
```

Learned:
- dataset structure,
- datatypes,
- missing values,
- transaction statistics,
- variability of data.

Key realization:
Professionals never trust raw datasets immediately.

---

# 3. Missing Value Analysis

Investigated missing transaction amounts using:

```python
df[df["transaction_amount"].isnull()]
```

Learned:
- missing data must be investigated before cleaning,
- imputation strategies depend on business context.

Compared:
- mean imputation,
- median imputation.

Important insight:
Median is often safer when extreme outliers exist.

---

# 4. Datetime Engineering

Converted dates properly using:

```python
pd.to_datetime()
```

Extracted:
- month,
- year,
- day name,
- weekend indicators.

Created features:
- month,
- day_name,
- is_weekend.

Business understanding:
Datetime intelligence powers:
- fraud detection,
- customer behavior analysis,
- seasonality analysis,
- operational reporting.

---

# 5. Feature Engineering

Created transaction segmentation logic:

```python
High Value
Medium Value
Low Value
```

Using a custom function with:

```python
apply()
```

Learned:
Feature engineering transforms raw data into intelligent business signals.

---

# 6. Duplicate Handling

Learned:
- duplicate records distort analytics,
- duplicates affect reporting accuracy,
- duplicates can create operational inconsistencies.

Practiced:
- detecting duplicates,
- creating duplicates intentionally,
- removing duplicates.

Functions used:

```python
duplicated()
drop_duplicates()
```

---

# 7. GroupBy & Aggregations

Performed branch transaction analysis using:

```python
groupby()
agg()
```

Generated:
- total transactions,
- average transactions,
- highest transaction,
- lowest transaction,
- transaction count.

Key insight:
GroupBy operations are foundational for:
- business intelligence,
- SQL thinking,
- dashboard analytics,
- operational reporting.

---

# 8. Fraud Detection Thinking

Created fraud review logic using:

```python
np.where()
```

Logic:
Transactions above 100000 were flagged for investigation.

Created:
- review_flag column.

Business understanding:
Real fraud systems often begin with:
- rules,
- thresholds,
- behavioral patterns,
before Machine Learning models are introduced.

---

# 9. Data Visualization

Created bar chart visualizations for:
- total transactions by branch.

Learned:
Visualization is business storytelling.

Charts help organizations:
- detect trends,
- compare branches,
- identify anomalies,
- support decision-making.

---

# Important Concepts Learned

## Data Cleaning
Real-world data is messy and requires preprocessing before analysis.

## Datetime Intelligence
Time-based features are critical in banking and analytics systems.

## Feature Engineering
Creating intelligent columns improves analytics and future ML models.

## Aggregation
Businesses rely heavily on summarized metrics and KPIs.

## Fraud Analytics
Risk systems often begin with rule-based logic.

## Data Storytelling
Analytics is valuable only when insights can be communicated clearly.

---

# Challenges Faced

## 1. Path Management
Learned the difference between:
- Python installation path,
- current working directory.

Solved export issues using:
```python
../datasets/
```

---

## 2. Column Name Errors

Encountered:
```python
KeyError
```

Cause:
A renamed column was referenced using its old name.

Solution:
Used:
```python
df.columns
```

to inspect available columns before plotting.

---

# Key Realizations

- Data Science is not only about Machine Learning.
- Most professional work involves:
  - cleaning,
  - structuring,
  - validating,
  - and understanding data.

- Pandas is deeply connected to:
  - SQL,
  - BI,
  - ML,
  - Data Engineering,
  - and analytics systems.

- Business understanding is just as important as coding.

---

# Deliverables Completed

## Notebook
```text
day_2_advanced_pandas.ipynb
```

## Dataset Export
```text
day_2_transactions.csv
```

## Branch Analytics Dashboard
Created branch-level transaction summaries and visualizations.

## Fraud Review Logic
Implemented rule-based transaction review flags.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook
- Git & GitHub

---

# Next Session Preview (Day 3)

Planned topics:
- dataset merging,
- joins,
- concatenation,
- advanced transformations,
- lambda functions,
- exploratory data analysis,
- correlations,
- multi-dataset workflows.

Goal:
Begin thinking more like a real analytics engineer and data systems builder.