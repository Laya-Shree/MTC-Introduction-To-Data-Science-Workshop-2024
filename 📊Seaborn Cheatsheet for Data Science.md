# 📊Seaborn Cheatsheet for Data Science

## Importing Seaborn

```python
import seaborn as sns
```

## Basic Plotting

```python
# Load built-in dataset
data = sns.load_dataset('iris')

# Simple scatter plot
sns.scatterplot(data=data, x='sepal_length', y='sepal_width')
plt.show()

# Simple line plot
sns.lineplot(data=data, x='sepal_length', y='sepal_width', hue='species')
plt.show()
```

## Creating Different Plots

```python
# Histogram
sns.histplot(data=data, x='sepal_length', bins=20)
plt.show()

# Box plot
sns.boxplot(data=data, x='species', y='sepal_length')
plt.show()

# Violin plot
sns.violinplot(data=data, x='species', y='sepal_length')
plt.show()

# Pair plot
sns.pairplot(data=data, hue='species')
plt.show()

# Heatmap
corr = data.corr()
sns.heatmap(corr, annot=True, cmap='coolwarm')
plt.show()
```

## Customizing Plots

```python
# Customizing scatter plot
sns.scatterplot(data=data, x='sepal_length', y='sepal_width', hue='species', style='species', palette='Set1')
plt.title('Custom Scatter Plot')
plt.show()

# Adding grid and style
sns.set(style='whitegrid')
sns.barplot(data=data, x='species', y='sepal_length')
plt.title('Bar Plot with White Grid Style')
plt.show()
```

## FacetGrid and PairGrid

```python
# FacetGrid
g = sns.FacetGrid(data, col='species')
g.map(sns.scatterplot, 'sepal_length', 'sepal_width')
plt.show()

# PairGrid
g = sns.PairGrid(data, hue='species')
g.map_lower(sns.scatterplot)
g.map_diag(sns.histplot)
plt.show()
```

## Regression Plots

```python
# Regression plot
sns.regplot(data=data, x='sepal_length', y='sepal_width')
plt.show()

# Residual plot
sns.residplot(data=data, x='sepal_length', y='sepal_width')
plt.show()
```

## Plotting with DataFrames

```python
import pandas as pd

# Create a DataFrame
df = pd.DataFrame({
    'x': [1, 2, 3, 4],
    'y': [10, 20, 25, 30],
    'category': ['A', 'B', 'A', 'B']
})

# Plot DataFrame
sns.barplot(data=df, x='x', y='y', hue='category')
plt.title('Bar Plot from DataFrame')
plt.show()
```

## Saving Figures

```python
# Save plot to file
sns.scatterplot(data=data, x='sepal_length', y='sepal_width')
plt.title('Scatter Plot')
plt.savefig('seaborn_plot.png')
```
