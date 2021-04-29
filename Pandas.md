# Pandas.

- It is used for data manipulation and analysis. 
- In particular, it offers data structures and operations for manipulating numerical tables and time series.
- *Pandas* is built on the *numpy* library 

## Why Pandas over Excel?

- Pandas can handle large data sets while Excel can't
- Pandas can work with Big Data, Excel can't

## DataFrame

- It is the most common used Pandas object
- It is a 2-dimensional labeled data structure with columns of potentially different types.
- It can be thought of like a spreadsheet or SQL table, or a dict of Series objects. 

## Loading Data

```python
# pandas is a data manipulation library
import pandas as pd

# loading different kinds of file
# df is a dataframe
df = pd.read_csv('pokemon_data.csv')

# loading an excel file
df_excel = pd.read_excel('pokemon_data.xlsx')

# loading a tab separated text file
# delimiter specifies the separator in the file, it can be 'xx' or 'xox'
df = pd.read_csv('pokemon_data.txt', delimiter='\t')
```

## Reading Data

- Reading Headers

  ```python
  print(df.columns)
  ```

- Reading each Column

  ```python
  # reading each column
  print(df['Name'])
  # reading multiple columns simultaneously
  print(df[['Name', 'Type 1', 'Type 2']])
  ```

- Reading each Row

  ```python
  # reading each row
  # reading specific row
  print(df.iloc[2])
  # reading range of rows
  print(df.iloc[0:4])
  # iterating over the dataframe row by row
  for index, row in df.iterrows():
      print(index, row['Name'])
  ```

- Reading a specific location(R, C)

  ```python
  # reading a specific location (R, C)
  print(df.iloc[0, 1])
  # reading data based on conditions
  df.loc[df['Type 1'] == "Grass"] 
  ```

- #### Methods

  - **loc** is label-based, which means that you have to specify rows and columns based on their row and column labels.

  - **iloc** is integer index based, so you have to specify rows and columns by their integer index

  - describe() is used for calculating some statistical data like percentile, mean and std of the numerical values of the Series or DataFrame. 

  - describe() analyzes both numeric and object series and also the DataFrame column sets of mixed data types.

    ```python
    # calculates all the statistical data
    df.describe()
    ```

## Sorting Data

```python
# sorting rows on the basis of columns 
df.sort_values('Name', ascending=False)
df.sort_values(['Name', 'Type 1'])

# sorts 'Name' in ascending order and 'Type 1' in descending order
df.sort_values(['Name', 'Type 1'], ascending=[1, 0])
```

## Changing Data

```python
# adding a 'Total' column
df['Total'] = df['HP'] + df['Attack'] + df['Defense'] + df['Sp. Atk'] + df['Sp. Def'] + df['Speed']
df.head()
```

## Filtering Data

```python
# data with 'Grass' or 'Poison'
df.loc[(df['Type 1'] == 'Grass') | (df['Type 2'] == 'Poison')]

# data with 'Grass' and 'Poison' and 'HP' > 70
filtered_df = df.loc[(df['Type 1'] == 'Grass') & (df['Type 2'] == 'Poison') & (df['HP'] > 70)]
filtered_df
```

#### Note

- The indexes of the original DF comes into the filtered data

- So, make sure to reset the indexes of the filtered data, if you want to work on them separately

  ```python
  # to remove previous indexes
  # create a new DF
  filtered_df = filtered_df.reset_index(drop=True)
  
  # OR
  
  # can be done inplace
  filtered_df.reset_index(drop=True, inplace=True)
  
  filtered_df
  ```

## Aggregate Statistics

```python
# calculates all the statistical data
df.describe()

# groupby 
df.groupby(['Type 1']).mean().sort_values('Attack', ascending=False)
```

## Saving Data

```python
# Saving our data
df.to_csv('modified.csv')

# without indexes
df.to_csv('modified.csv', index=False)

# saving in an excel file
df.to_excel('modified.xlsx', index=False)

# saving in a tab separated file
df.to_csv('modified.txt', index=False, sep='\t')
```

