# 🚀 **Introduction to Data Science Workshop**

Welcome to the **Introduction to Data Science Workshop**! In this 60-minute session, we will explore the exciting world of data science, covering essential concepts and popular Python libraries like `Numpy`, `Pandas`, `Matplotlib`, and `Seaborn` along with hands on practice.

---

## 🗺️ **Workshop Roadmap**

1. **Introduction to Data Science and Career Roadmap**
2. **Python and Its Role in Data Science**
3. **Introduction to Numpy**
4. **Introduction to Pandas**
5. **Introduction to Matplotlib and Seaborn**
6. **Q&A and Hands-on Practice**

---

## 📊 **1. Introduction to Data Science and Career Roadmap**

**What is Data Science?**

- Data Science is the study of data to extract meaningful insights.
- Involves statistics, machine learning, and data analysis.

![Introduction To Data Science What is Data Science?  by Rashal Ismath   Analytics Vidhya  Medium](https://miro.medium.com/v2/resize:fit:730/0*POjH5vv_7t8s8loG)

![](file:///C:/Users/layas/AppData/Roaming/marktext/images/2024-09-05-23-02-52-image.png?msec=1725693126262)

### Fields of Data Science:

| Field | Description |
| --- | --- |
| **Data Analysis** | Analyzing datasets to summarize main features |
| **Machine Learning** | Algorithms that learn from and make predictions |
| **Artificial Intelligence** | Simulating human intelligence in machines |

### Skills Required:

- **Programming**: Python, R
- **Data Manipulation**: Pandas, Numpy
- **Visualization**: Matplotlib, Seaborn
- **Statistics & Probability**

---

## 🐍 **2. Python and Its Role in Data Science**

Python is the leading programming language in data science due to its simplicity, vast libraries, and versatility.

### Popular Python Libraries:

| Library | Usage |
| --- | --- |
| 📐**Numpy** | Numerical computations |
| 🧮**Pandas** | Data manipulation and analysis |
| 📈**Matplotlib** | Data visualization |
| 📊**Seaborn** | Statistical data visualization |

```python
# Installing Libraries
pip install pandas
pip install seaborn
pip install scikit-learn
```

```python
# Importing Libraries
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```
---
## ✨Data Preprocessing

This documentation provides a step-by-step guide for handling common data preprocessing tasks, including handling missing values, feature encoding, and normalization. These are essential steps for preparing data for machine learning models.

---

### Step 1: Handling Missing Values

Missing data can negatively affect the performance of machine learning models. In this step, we identify and handle missing values using different strategies.

#### Check for Missing Values

The first step is to check for missing values in the dataset:

```python
# Check for missing values in each column
missing_values = df_train.isnull().sum()

# Display columns with missing values
print(missing_values[missing_values > 0])
```

This code checks each column in `df_train` for missing values and prints the columns where missing values are found.

#### Method 1: Deleting Rows or Columns with Missing Values

If missing values are sparse or unimportant, they can be removed by deleting rows or columns:

```python
# Drop rows with any missing values
df_dropped_rows = df.dropna()
```

This removes any row that contains at least one missing value. Alternatively, you can specify a column to drop rows where that particular column has missing values:

```python
# Drop rows with missing values in a specific column (e.g., 'col1')
df_dropped_rows_specific = df.dropna(subset=['col1'])
```

If you prefer to remove columns with missing values, use the following command:

```python
# Drop columns with any missing values
df_dropped_columns = df.dropna(axis=1)
```

This drops columns where any value is missing. This approach is useful when entire columns are unreliable due to missing data.

#### Method 2: Replacing Missing Values with Mean, Median, or Mode

A more common approach is to replace missing values with statistical measures like the mean, median, or mode:

```python
# Fill NaN with the mean of the column
df['col1'] = df['col1'].fillna(df['col1'].mean())
```

This code replaces all missing values in `col1` with the column’s mean. Similarly, you can use the median or mode:

```python
# Fill NaN with the median of the column
df['col2'] = df['col2'].fillna(df['col2'].median())
```

```python
# Fill NaN with the mode of the column
df['col3'] = df['col3'].fillna(df['col3'].mode()[0])
```

This is particularly useful when the dataset has numerical data where you do not want to remove rows or columns.

---

### Step 2: Feature Encoding

Categorical features need to be converted into numerical formats for most machine learning algorithms. There are two main methods for this: One-Hot Encoding and Label Encoding.

#### Select Categorical and Numerical Columns

Before encoding, you should identify which columns are categorical and which are numerical:

```python
# Select all categorical columns
categorical_columns = df.select_dtypes(include=['object', 'category'])

# Select and print all numerical columns
numerical_columns = df.select_dtypes(include=['number'])
```

This helps you separate categorical and numerical features for further processing.

#### Method 1: One-Hot Encoding

One-Hot Encoding converts each unique category into a new binary column:

```python
df_encoded = pd.get_dummies(df, columns=['column1'], drop_first=True)
```

This creates binary columns for every category in `column1`. The `drop_first=True` argument removes the original column.

#### Method 2: Label Encoding

Label Encoding assigns a unique integer to each category:

```python
# Import, Initialize, and fit LabelEncoder
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
df['column1'] = le.fit_transform(df['column1'])
```

Alternatively, you can manually map categories to integers:

```python
# OR do manually
column1_map = {'value1': 0, 'value2': 1, 'value3': 2}
df['column1'] = df['column1'].map(column1_map)
```

This method is typically used when there is an ordinal relationship between the categories (e.g., low, medium, high).

---

### Step 3: Normalization

Normalization standardizes the range of independent features.

#### Standardization using StandardScaler

```python
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()

# Fit and transform all columns except the target column
x_scaled = scaler.fit_transform(df.drop(['Target_column'], axis=1))
```

This scales the features so that they have a mean of 0 and a standard deviation of 1, which improves the performance of machine learning models by normalizing the range of data.



With these steps, you'll be able to handle missing values, encode categorical data, and normalize your features effectively, preparing your data for machine learning models.

---

## 📚 **Cheat Sheet and Glossary**

Here are some key terms and commands you'll use throughout your data science journey.
### 📝 **Cheat Sheet:**

- [🐼 Pandas Cheatsheet for Data Science](./🐼Pandas%20Cheatsheet%20for%20Data%20Science.md)
- [📐 NumPy Cheatsheet for Data Science](./📐NumPy%20Cheatsheet%20for%20Data%20Science.md)
- [📈 Matplotlib Cheatsheet for Data Science](./📈Matplotlib%20Cheatsheet%20for%20Data%20Science.md)
- [📊 Seaborn Cheatsheet for Data Science](./📊Seaborn%20Cheatsheet%20for%20Data%20Science.md)

## 🔑 **Glossary of Terms**

1. **Array**: A data structure that stores elements of the same type in a fixed size.  
2. **DataFrame**: A 2D labeled data structure with rows and columns, used for data manipulation in pandas.  
3. **Data Cleaning**: The process of correcting or removing inaccurate data points to ensure data quality.  
4. **Missing Data**: Absence of a data value for a variable in a dataset, handled through deletion or imputation.  
5. **Data Preprocessing**: Transforming raw data into a clean and usable format for analysis or modeling.  
6. **Features**: The measurable properties or characteristics of data used as input in machine learning models.  
7. **Feature Selection**: The process of selecting the most important variables to use in model building.  
8. **Feature Encoding**: Converting categorical variables into numerical form for machine learning models.  
9. **One-Hot Encoding**: A method to convert categorical variables into binary vectors for each unique category.  
10. **Label Encoding**: Assigning numerical values to categorical labels in a dataset.  
11. **Normalization**: Scaling data to ensure consistency across the feature's range of values.  
12. **StandardScaler**: A tool to standardize features by removing the mean and scaling to unit variance.  
13. **Outliers**: Data points that deviate significantly from other observations in the dataset.  
14. **Exploratory Analysis**: Analyzing data sets to summarize their main characteristics, often using visualizations.  
15. **Target**: The variable or outcome that a model aims to predict, also called the dependent variable.
---

## 🎉 **Hands-on Practice**

To get started with today's hands-on session, open your Google Colab notebook and follow the instructions provided in the comments of each code cell. Use the cheat sheets provided to guide you through writing and executing the code. This practice will help you solidify your understanding of data preprocessing, feature selection, encoding, and other key concepts. Dive in and start coding! 🚀

---

## 🙋 **Q&A**

Feel free to ask any questions or clarify any doubts during this session!
