Q1. Create a Pandas Series that contains the following data: 4, 8, 15, 16, 23, and 42. Then, print the series.

Q2. Create a variable of list type containing 10 elements in it, and apply pandas.Series function on the
variable print it.

Q3. Create a Pandas DataFrame that contains the following data:

Then, print the DataFrame.

Q4. What is ‘DataFrame’ in pandas and how is it different from pandas.series? Explain with an example.

Q5. What are some common functions you can use to manipulate data in a Pandas DataFrame? Can
you give an example of when you might use one of these functions?

Q6. Which of the following is mutable in nature Series, DataFrame, Panel?

Q7. Create a DataFrame using multiple Series. Explain with an example.

## Ans 1


```python
import pandas as pd
data = [4,8,15,16,23,42]
series = pd.Series(data)
print(series)
```

    0     4
    1     8
    2    15
    3    16
    4    23
    5    42
    dtype: int64


## Ans 2


```python
my_list = [1,2,3,4,5,6,7,8,9,10]
my_series = pd.Series(my_list)
print(my_series)
```

    0     1
    1     2
    2     3
    3     4
    4     5
    5     6
    6     7
    7     8
    8     9
    9    10
    dtype: int64


## Ans 3


```python
data = {'Name': ['Alice', 'Bob', 'Claire'],
        'Age': [25,30,27],
        'Gender': ['Female','Male','Female']}
df = pd.DataFrame(data)
print(df)
```

         Name  Age  Gender
    0   Alice   25  Female
    1     Bob   30    Male
    2  Claire   27  Female


## Ans 4
In pandas, a DataFrame is a two-dimensional table-like data structure, similar to a spreadsheet or SQL table, where each column can have a different data type (numeric, string, boolean, etc.) and can be labeled with a column name. It is one of the most commonly used data structures in pandas and is a powerful tool for data manipulation and analysis.

On the other hand, a pandas Series is a one-dimensional array-like data structure that contains homogeneous data (all of the same data type) and can be labeled with an index. A Series can be thought of as a single column in a DataFrame.


```python
## Example
data = {'name': ['Alice', 'Bob', 'Charlie', 'David', 'Emily'],
        'age': [25, 32, 18, 47, 21],
        'gender': ['F', 'M', 'M', 'M', 'F']}

# create a DataFrame from the dictionary
df = pd.DataFrame(data)

# create a Series from the 'age' column of the DataFrame
age_series = df['age']

# print the DataFrame and the Series
print(df)
```

          name  age gender
    0    Alice   25      F
    1      Bob   32      M
    2  Charlie   18      M
    3    David   47      M
    4    Emily   21      F



```python
# print the Series
print(age_series)
```

    0    25
    1    32
    2    18
    3    47
    4    21
    Name: age, dtype: int64


## Ans 5
There are many functions available in Pandas to manipulate data in a DataFrame. Here are some common functions:



```python
## df.head(n) - Returns the first n rows of the DataFrame.
df = pd.read_csv('data.csv')
print(df.head(10))
```


```python
## df.tail(n) - Returns the last n rows of the DataFrame.
df = pd.read_csv('data.csv')
print(df.tail(10))
```


```python
## df.columns - Returns a list of column names in the DataFrame
df = pd.read_csv('data.csv')
print(df.columns)
```

## Ans 6
In Pandas, both Series and DataFrame are mutable in nature, meaning you can change their values, add or remove rows or columns, and perform other modifications. However, Panel is considered as an outdated data structure in Pandas and has been deprecated since version 1.0.0. It has been replaced by the more powerful and flexible MultiIndexing capabilities of DataFrame, and is therefore considered as immutable in nature.

To summarize: Series and DataFrame are mutable, while Panel is immutable in nature in Pandas.

## Ans 7



```python
names = pd.Series(['Alice', 'Bob', 'Charlie'])

# create a Series of ages
ages = pd.Series([25, 32, 18])

# create a Series of genders
genders = pd.Series(['F', 'M', 'M'])

# create a dictionary of data
data = {'name': names, 'age': ages, 'gender': genders}

# create a DataFrame from the dictionary
df = pd.DataFrame(data)

# print the DataFrame
print(df)
```

          name  age gender
    0    Alice   25      F
    1      Bob   32      M
    2  Charlie   18      M



```python

```
