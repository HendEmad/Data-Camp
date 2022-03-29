# [Pandas](https://pandas.pydata.org/docs/index.html):
- A very popular module to deal with data.
- It gives us many tools for working with tabular data. we can load tabular data from multiple sources (like spreadsheets or databases), search for particular rows or columns in your loaded data, calculate aggregate statistics (like averages or standard deviations), and combine data from multiple sources.
- There is another powerful datatype included in Pandas which is **DataFrame(df)** that represents the tabular data.

**_Loading data is the first step in using Pandas._**

### CSV files:
- Stands fro 'Comma- separated values'.
- It is the most common way of storing tabular data.
- We can download a csv version of data from an excel spreadsheets, a SQL database, or a Google Sheet.

### Loading a csv:
- At first: we have to import pandas module using alias pd ```import pandas as pd```
- To load the csv file we will use, we use **'read_csv('filename.csv')'**. This function takes one argument which is the data file to be loaded.

### Displaying a csv:
- We can display the data frame using ```print('df_name')``` function.
- We can use ```df.head()``` to display the first five rows from the data(n rows, but 5 by default). 
- We can use ```df.tail()``` to display the last five rows from the data(n rows, but 5 by default).
