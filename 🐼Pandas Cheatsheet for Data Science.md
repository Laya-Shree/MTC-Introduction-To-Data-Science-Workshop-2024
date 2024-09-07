# 🐼Pandas Cheatsheet for Data Science

## Installing pandas

```python
pip install pandas
```

## Importing Pandas

```python
import pandas as pd
```

## Creating Dataframe

```python
# From a dictionary
df = pd.DataFrame({
    'column1': [1, 2, 3],
    'column2': ['A', 'B', 'C']
})

# From a CSV file
df = pd.read_csv('file.csv')

# From an Excel file
df = pd.read_excel('file.xlsx')
```

## Basic Operations

You can replace `'column1'` with the actual name of the column you want to analyze.

```python
# View the first 5 rows
df.head(5)
```

```python
# View the last 5 rows
df.tail(5)
```

```python
# Get DataFrame info
df.info()
```

```python
# Get basic statistics
df.describe()
```

```python
# Display the column names
df.columns
```

```python
# Display unique values of a specific column
df['column1'].unique()
```

```python
# Display the number of unique values in a specific column
df['column1'].nunique()
```

```python
# Display column name, unique value, and its count
df['column1'].value_counts()
```

```python
# Display unique value count for all columns
df.nunique()
```

### Selecting Data

```python
# Select a single column
df['column1']
```

```python
# Select multiple columns
df[['column1', 'column2']]
```

```python
# Select rows by index
df.iloc[0]          # Single row by index
df.iloc[0:5]        # Rows by range
```

```python
# Select rows by label
df.loc[0]           # Single row by label
df.loc[0:5]         # Rows by range
```

```python
# Conditional selection
df[df['column1'] > 1]
```

### Data Cleaning

```python
#check repeated rows
df.duplicated().sum()
```

```python
# Remove duplicates
df.drop_duplicates()
```

```python
# Drop rows with missing values
df.dropna()
```

```python
# Fill missing values
df.fillna(value='fill_value')
```

```python
# Rename columns
df.rename(columns={'old_name': 'new_name'})
```

### Data Manipulation

```python
# Add a new column
df['new_column'] = df['column1'] * 2
```

```python
# Drop a column
df = df.drop(columns=['column1'])
```

```python
# Sort by a column
df_sort = df.sort_values(by='column2')
```

```python
# Group by and aggregate
df_group = df.groupby('column2').agg({'column1': 'sum'})
```

### Merging and Joining

```python
# Merge DataFrames on a common column
df_merged = pd.merge(df1, df2, on='common_column')
```

```python
# Concatenate DataFrames
df_concat = pd.concat([df1, df2])
```

```python
# Join DataFrames (similar to SQL joins)
df_joined = df1.join(df2, on='key_column')
```

### Saving Data

```python
# Save to CSV
df.to_csv('file.csv', index=False)
```

```python
# Save to Excel
df.to_excel('file.xlsx', index=False)---
```
