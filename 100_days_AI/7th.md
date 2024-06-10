# Day 7: Introduction to Pandas

## Goals
- Understand the basics of Pandas and its importance in data manipulation.
- Learn to create, manipulate, and analyze data using Pandas DataFrames and Series.
- Practice fundamental data manipulation tasks using Pandas.

## Tasks

### 1. Introduction to Pandas
- **Overview:** Pandas is a high-level data manipulation tool developed by Wes McKinney. It is built on the Numpy package and its key data structure is called DataFrame. DataFrames allow you to store and manipulate tabular data in rows of observations and columns of variables. Pandas is crucial for data analysis in Python because of its ability to handle large datasets efficiently and its integration with other Python libraries like NumPy and Matplotlib.

### 2. Pandas Series
- **Concepts to Explore:**
  - **Definition:** A Series is a one-dimensional array-like object capable of holding any data type (integers, strings, floating point numbers, Python objects, etc.). It has a sequence of values and an associated array of data labels, called its index.
  - **Creation:** Learn how to create a Series from different data types such as lists, dictionaries, and numpy arrays.
  - **Basic Operations:**
    - **Indexing:** Access elements using index labels.
    - **Slicing:** Retrieve multiple elements using slice notation.
    - **Vectorized Operations:** Perform operations on entire Series without using loops.
  - **Functions and Methods:** Commonly used functions like `.head()`, `.tail()`, `.describe()`, and methods like `.sum()`, `.mean()`, `.max()`, etc.

 
  ```python
  import pandas as pd

  # Creating a Series from a list
  data = [1, 3, 5, 7, 9]
  series = pd.Series(data)
  print(series)

  # Accessing elements
  print(series[0])  # First element
  print(series[1:4])  # Slicing

  # Creating a Series from a dictionary
  data_dict = {'a': 10, 'b': 20, 'c': 30}
  series_dict = pd.Series(data_dict)
  print(series_dict)
  ```

### 3. Pandas DataFrame
- **Concepts to Explore:**
  - **Definition:** A DataFrame is a two-dimensional, size-mutable, potentially heterogeneous tabular data structure with labeled axes (rows and columns).
  - **Creation:** Understand how to create DataFrames from various data structures like dictionaries, lists of lists, and numpy arrays.
  - **Basic Operations:**
    - **Selecting Data:** Methods to select rows and columns using `.loc[]`, `.iloc[]`, and simple indexing.
    - **Adding/Removing Columns:** Techniques to add new columns and remove existing ones.
    - **Filtering Data:** Use boolean indexing to filter DataFrame rows based on column values.
    - **Data Cleaning:** Handle missing values using `.dropna()`, `.fillna()`, and other techniques to ensure data quality.
```python
# Creating a DataFrame from a dictionary
data = {
    'Name': ['John', 'Anna', 'Peter', 'Linda'],
    'Age': [28, 24, 35, 32],
    'City': ['New York', 'Paris', 'Berlin', 'London']
}
df = pd.DataFrame(data)
print(df)

# Selecting columns
print(df['Name'])

# Adding a new column
df['Country'] = ['USA', 'France', 'Germany', 'UK']
print(df)

# Filtering data
filtered_df = df[df['Age'] > 30]
print(filtered_df)
```
### 4. Data Manipulation with Pandas
- **Skills to Develop:**
  - **Merging and Joining:** Learn how to combine multiple DataFrames using merge and join operations.
    - **Merge:** Use `.merge()` to combine DataFrames based on a common column or index.
    - **Join:** Use `.join()` to combine DataFrames based on index.
  - **Grouping and Aggregation:** Group data using `.groupby()` and perform aggregate operations like `.sum()`, `.mean()`, `.count()`.
  - **Reshaping Data:**
    - **Pivot Tables:** Create pivot tables using `.pivot_table()` to summarize data.
    - **Stack and Unstack:** Use `.stack()` and `.unstack()` to reshape the layout of DataFrames.
  - **Data Cleaning:** Practice handling missing data, removing duplicates, fixing incorrect data types, and using `.replace()` for data standardization.
```python
# Merging DataFrames
df1 = pd.DataFrame({
    'ID': [1, 2, 3],
    'Name': ['Alice', 'Bob', 'Charlie']
})
df2 = pd.DataFrame({
    'ID': [1, 2, 4],
    'Score': [85, 90, 78]
})
merged_df = pd.merge(df1, df2, on='ID', how='inner')
print(merged_df)

# Grouping and Aggregation
grouped = df.groupby('City').agg({'Age': 'mean'})
print(grouped)
```

### 5. Mini-Project: Data Analysis with Pandas
- **Project Overview:**
  - Use the Netflix Movies and TV Shows dataset to perform a comprehensive data analysis. Begin with data loading and proceed with cleaning, manipulation, and visualization tasks.
  - **Dataset:** [Netflix Movies and TV Shows](https://www.kaggle.com/shivamb/netflix-shows)

  - **Steps:**
    - **Loading the Dataset:** Load the dataset into a Pandas DataFrame using `pd.read_csv()`.
    - **Data Cleaning and Preprocessing:**
      - Handle missing values by either dropping rows/columns or filling them with appropriate values.
      - Convert data types if necessary to ensure consistency and correctness.
    - **Exploratory Data Analysis (EDA):**
      - Summarize statistics for numerical columns using `.describe()`.
      - Visualize distributions of key features using Matplotlib or Seaborn for more advanced plots.
    - **Analysis:**
      - Identify the most common genres using `.str.split()` and `.explode()` to handle lists within cells.
      - Analyze the number of shows released each year with `.value_counts()` and `.sort_index()`.
      - Compare the number of movies vs. TV shows using `.value_counts()` on the `type` column.
    - **Visualization:**
      - Create bar plots, histograms, and pie charts to visualize your findings and make the analysis more interpretable.
```python
# Loading the Netflix dataset
url = 'https://raw.githubusercontent.com/prasertcbs/basic-dataset/master/netflix_titles.csv'
netflix_df = pd.read_csv(url)

# Data cleaning and preprocessing
netflix_df = netflix_df.dropna(subset=['release_year'])  # Drop rows with missing release_year values
netflix_df['rating'] = netflix_df['rating'].fillna('Not Rated')  # Fill missing rating values with 'Not Rated'

# Exploratory Data Analysis
print(netflix_df.describe())

# Visualization (using Matplotlib)
import matplotlib.pyplot as plt

netflix_df['release_year'].hist(bins=30)
plt.title('Release Year Distribution')
plt.xlabel('Year')
plt.ylabel('Frequency')
plt.show()

# Most common genres
genres = netflix_df['listed_in'].str.split(', ').explode()
common_genres = genres.value_counts().head(10)
print(common_genres)

# Number of shows released each year
release_year_counts = netflix_df['release_year'].value_counts().sort_index()
release_year_counts.plot(kind='bar', figsize=(10, 5))
plt.title('Number of Shows Released Each Year')
plt.xlabel('Year')
plt.ylabel('Count')
plt.show()

# Compare movies vs TV shows
content_type_counts = netflix_df['type'].value_counts()
content_type_counts.plot(kind='pie', autopct='%1.1f%%', figsize=(7, 7))
plt.title('Movies vs TV Shows')
plt.show()
```

## Resources
- **Pandas Documentation:** [Official Pandas Documentation](https://pandas.pydata.org/docs/)
- **Video Tutorials:**
  - [Exploratory Data Analysis with Pandas Python](https://www.youtube.com/watch?v=xi0vhXFPegw)
  - [Pandas Full Course](https://www.youtube.com/watch?v=PcvsOaixUh8)
- **Dataset:** [Netflix Movies and TV Shows dataset](https://www.kaggle.com/shivamb/netflix-shows)

## Conclusion
- By the end of Day 7, you should be comfortable with basic and intermediate Pandas operations, capable of handling real-world data analysis tasks effectively. Ensure you practice regularly and explore additional resources to deepen your understanding.
