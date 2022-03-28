# Module:
Modules help together related tools in python. For example:
- Matplotlip: which create charts(the tools to plot data).
- Pandas: which loads tabular(the tools to read data from a file).
- Scikit-learn: which performs machine learning.
- Scipy: which contains statistics functions.
- nltk: which works with text data.

To work the tools in these modules, we have to import them at first:
for example: ```import pandas as pd```
note: pd is called an **alias** of pandas module.

# Variables:
a block of memory that we can save a piece of data like height of some one for example.
### There are some rules to define the variables:
- Variables must start with a letter. 
- We can't use special characters like exclamation points or dashes.
- Variable names are case sensitive, which means that variable **MY_VAR** differs from **my_var**.

Note: It we don't follow the variable definition rule, we will get a syntax error.

### There are many types of variables in Python like: 
float for integers, decimals & string for text, letters, numbers, spaces, and special characters. 
Note: we define string by putting either single or double quotes around a piece of text.

We can use **print()** function and our variable name inside the parentheses to dispaly the **current** value of it.

# Functions:
Functions are actions, we pass the inputs to it and we get the output based on the calcualtions made inside it.
- There are two types of functions: Built-in functions and user-defined functions.
**Built-in functions: **

functions that is built inside the module itself. these functions are built to do a specific task like print()
- Print() functions is made to display the value inside its parentheses. This is a built in function within Python library
- pd.read_csv('filename.csv'):
Here **pd** is the module contained read_csv()function, read_csv() is the function itself and **filename.csv** is the file we want to pass into the funciton.
- Values to pass to the function are called: **Arguments**, and they must be comma separated.

### There are some types of errors you can get while using functions:
- **Syntax errors:** where you may miss the comma between each argument, you also may miss one of the parentheses.

- We use **read_csv()** function-->  to load the dataframe that represents the data we will deal with.
- **Data Frame** is a type variables, specific to pandas. This is the way we can deal with tabular data via pandas module.
