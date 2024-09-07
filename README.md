🚀 **Introduction to Data Science Workshop**

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
| **Numpy** | Numerical computations |
| **Pandas** | Data manipulation and analysis |
| **Matplotlib** | Data visualization |
| **Seaborn** | Statistical data visualization |

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

## 📐 **3. Introduction to Numpy**

`Numpy` is the foundation for numerical operations in Python.

### Key Concepts:

- **Numpy Arrays**: Efficient arrays for storing numerical data.
- **Operations**: Mathematical operations like sum, mean, reshape, and indexing.

#### Example Code:

```python
import numpy as np

# Creating a Numpy Array
arr = np.array([1, 2, 3, 4, 5])
print("Array:", arr)

# Reshaping an Array
reshaped_arr = arr.reshape((1, 5))
print("Reshaped Array:", reshaped_arr)
```

---

## 🧮 **4. Introduction to Pandas**

`Pandas` is the go-to library for data manipulation and analysis. It introduces powerful data structures like **DataFrames**.

### Key Concepts:

- **DataFrames**: 2D labeled data structures (similar to Excel tables).
- **Data Manipulation**: Filtering, sorting, aggregating, and handling missing values.

#### Example Code:

```python
import pandas as pd

# Load a CSV file
df = pd.read_csv('data.csv')

# Basic DataFrame operations
print(df.head())  # First 5 rows
print(df.describe())  # Summary statistics

# Filtering Data
filtered_df = df[df['age'] > 30]
print(filtered_df)
```

---

## 📈 **5. Introduction to Matplotlib and Seaborn**

`Matplotlib` and `Seaborn` are essential for creating insightful data visualizations.

### **Matplotlib**: General-purpose plotting library

#### Example Code:

```python
import matplotlib.pyplot as plt

# Basic Line Plot
x = [0, 1, 2, 3]
y = [0, 1, 4, 9]
plt.plot(x, y)
plt.title("Simple Line Plot")
plt.xlabel("X-Axis")
plt.ylabel("Y-Axis")
plt.show()
```

### **Seaborn**: High-level interface for attractive visualizations

#### Example Code:

```python
import seaborn as sns
import pandas as pd

# Load the famous Titanic dataset
titanic = sns.load_dataset("titanic")

# Create a simple Seaborn bar plot
sns.barplot(x="sex", y="survived", data=titanic)
plt.title("Survival Rate by Gender")
plt.show()
```

---

## 📚 **Cheat Sheet and Glossary**

Here are some key terms and commands you'll use throughout your data science journey.

### 📝 **Cheat Sheet:**

---

## 🔑 **Glossary of Terms**

- **Array**: A data structure that holds a fixed number of elements of a single type.
- **DataFrame**: A 2-dimensional labeled data structure with columns of potentially different types.
- **Visualization**: The representation of data in a graphical format.
- **Aggregation**: A computation that summarizes groups of data (e.g., sum, average).
- **Missing Data**: Occurs when no data value is stored for a variable in a dataset.

---

## 🎉 **Hands-on Practice**

Try the following tasks:

1. Load a dataset into Pandas.
2. Visualize the data using Matplotlib or Seaborn.
3. Apply basic data manipulations using Pandas (`filter`, `groupby`, `aggregate`).

---

## 🙋 **Q&A**

Feel free to ask any questions or clarify any doubts during this session!
