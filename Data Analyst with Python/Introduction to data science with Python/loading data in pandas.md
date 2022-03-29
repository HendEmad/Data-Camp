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
- We can use also ```df.info``` to know no.of columns and their data types.

### Selecting columns:
The first way we use the data is by selecting columns which means getting all values inside a specific columns. we select columns to:
1- Making calculations on them:
```credit_records.price.sum()``` ---> To get the total amount of money spent by our suspects.
OR ```credit_records['price'].sum()```
2- Using them as input to a function:

for example: ```plt.plot(ransom['letter'], ransom['frequency'])``` ---> to create a plot of frequencies of each letter in the ransom note. Here, The df called **ransom**, and the columns are **letter & frequency** 

To select a specific column: ```var = df_name['column_name_string']```. for example: ```suspect = credit_records['suspect']```
If we print the column ```print(suspect)```, we will see all values inside this particular column.

- There is anpther way we can do **ONLY IF the columns string only contains letters, numbers, and underscores**, we can use dot notation: ```var = df_name.column_name_string```. for example: ```price = credit_records.price``` and displaying the valuse within this column in the same way which is ```print(price)``` 

### Common errors while selecting columns:
1- When the column name contains spaces or special characters, you need to use bracket and string notation (the first way), not the dot notation (the second way).

If you use the second way in this case, python will gets confused and thinks that you're referring to several different variables.
