# Promise Dataset README

This README provides an overview and details about the `Promise.csv` dataset. This dataset is commonly used in software engineering research, particularly for studies related to software requirements and their classification.

## Dataset Overview

The `Promise.csv` file contains a collection of software requirements, each categorized by a specific type. It is a valuable resource for tasks such as requirements classification, natural language processing (NLP) on software requirements, and empirical studies in software engineering.

## Dataset Structure

The dataset is provided in a CSV (Comma Separated Values) format with the following columns:

- **S.No**: Serial Number, a unique identifier for each record.
- **File**: An identifier that might represent the source file or project from which the requirement was extracted.
- **Requirement**: The actual text of the software requirement.
- **Type**: The classification or category of the requirement.




## Detailed Analysis

Based on the analysis of `Promise.csv`, the dataset contains 969 entries with no missing values across any of the columns. This indicates a clean dataset ready for immediate use.

### Data Types and Non-Null Counts

```
--- DataFrame Info ---
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 969 entries, 0 to 968
Data columns (total 4 columns):
 #   Column       Non-Null Count  Dtype 
---  ------       --------------  ----- 
 0   S.No         969 non-null    int64 
 1   File         969 non-null    int64 
 2   Requirement  969 non-null    object
 3   Type         969 non-null    object
dtypes: int64(2), object(2)
memory usage: 30.4+ KB
```

### Missing Values

No missing values were found in any of the columns:

```
--- Missing Values ---
S.No           0
File           0
Requirement    0
Type           0
dtype: int64
```

### Unique Requirement Types and Counts

The `Type` column categorizes the requirements into several distinct types. The distribution of these types is as follows:

```
--- Unique Types and Counts ---
Type
F     444
SE    125
US     85
O      77
PE     67
LF     49
A      31
MN     24
SC     22
FT     18
L      15
PO     12
Name: count, dtype: int64
```

### Requirement Length Description

The length of the `Requirement` text varies, providing a diverse set of textual data. The descriptive statistics for the length of requirements are:

```
--- Requirement Length Description ---
count    969.000000
mean     109.248710
std       61.104732
min       28.000000
25%       70.000000
50%       94.000000
75%      128.000000
max      546.000000
```

## Usage

This dataset can be used for various purposes, including:

- **Text Classification**: Training models to classify software requirements into predefined categories.
- **Natural Language Processing (NLP)**: Analyzing the linguistic patterns and characteristics of software requirements.
- **Software Engineering Research**: Conducting empirical studies on requirement quality, traceability, or evolution.

### Example Usage (Python with Pandas)

```python
import pandas as pd

# Load the dataset
df = pd.read_csv("Promise.csv")

# Display the first few rows
print(df.head())

# Get basic information about the dataset
df.info()

# Count occurrences of each requirement type
print(df["Type"].value_counts())
```


