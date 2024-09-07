# 📈Matplotlib Cheatsheet for Data Science

## Importing Matplotlib

```python
import matplotlib.pyplot as plt
```

## Basic Plotting

```python
# Simple line plot
plt.plot([1, 2, 3], [4, 5, 6])
plt.show()

# Plot with labels
plt.plot([1, 2, 3], [4, 5, 6])
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Simple Line Plot')
plt.show()
```

## Creating Different Plots

```python
# Scatter plot
plt.scatter([1, 2, 3], [4, 5, 6])
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Scatter Plot')
plt.show()

# Bar plot
plt.bar(['A', 'B', 'C'], [4, 5, 6])
plt.xlabel('Categories')
plt.ylabel('Values')
plt.title('Bar Plot')
plt.show()

# Histogram
plt.hist([1, 2, 1, 2, 3, 4, 4, 4, 5], bins=5)
plt.xlabel('Bins')
plt.ylabel('Frequency')
plt.title('Histogram')
plt.show()

# Pie chart
plt.pie([10, 20, 30], labels=['A', 'B', 'C'], autopct='%1.1f%%')
plt.title('Pie Chart')
plt.show()
```

## Customizing Plots

```python
# Plot with different line styles and colors
plt.plot([1, 2, 3], [4, 5, 6], linestyle='--', color='r', marker='o')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Customized Line Plot')
plt.show()

# Adding grid
plt.plot([1, 2, 3], [4, 5, 6])
plt.grid(True)
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Line Plot with Grid')
plt.show()
```

## Subplots

```python
# Creating multiple subplots
fig, axs = plt.subplots(2, 2)
axs[0, 0].plot([1, 2, 3], [4, 5, 6])
axs[0, 1].scatter([1, 2, 3], [4, 5, 6])
axs[1, 0].bar(['A', 'B', 'C'], [4, 5, 6])
axs[1, 1].hist([1, 2, 1, 2, 3, 4, 4, 4, 5], bins=5)
plt.tight_layout()
plt.show()
```

## Saving Figures

```python
# Save plot to file
plt.plot([1, 2, 3], [4, 5, 6])
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Line Plot')
plt.savefig('plot.png')
```

## Using Styles

```python
# Set a style
plt.style.use('ggplot')

# Plot with style
plt.plot([1, 2, 3], [4, 5, 6])
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Styled Line Plot')
plt.show()
```

## Plotting with DataFrames

```python
import pandas as pd

# Create a DataFrame
df = pd.DataFrame({
    'x': [1, 2, 3],
    'y': [4, 5, 6]
})

# Plot DataFrame
df.plot(x='x', y='y', kind='line')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Line Plot from DataFrame')
plt.show()
```
