 # Importing Python modules
 In the script editor, use an import statement to import statsmodels without an alias.

Solution:
```
import statsmodels
```

# Correcting a broken import
Fix the import of numpy to run without errors: ```import Numpy as np```

solution: ```import numpy as np```

# Creating a float
- Define a variable called bayes_age and set it equal to 4.0.
- Display the variable bayes_age.

Solution: 
```
# Fill in Bayes' age (4.0)
bayes_age = 4.0

# Display the variable bayes_age
print(bayes_age)
```

# Creating strings
- Define a variable called favorite_toy whose value is "Mr. Squeaky".
- Define a variable called owner whose value is 'DataCamp'.
- Show the values assigned to these variables.

Solution:
```
# Bayes' favorite toy
favorite_toy = 'Mr. Squeaky'

# Bayes' owner
owner = 'DataCamp'

# Display variables
print(favorite_toy)
print(owner)
```

# Correcting string errors
Correct the mistakes in the code so that it runs without producing syntax errors.
```
# One or more of the following lines contains an error
# Correct it so that it runs without producing syntax errors
birthday = "2017-07-14'
case_id = 'DATACAMP!123-456?
```

solution:
```
# One or more of the following lines contains an error
# Correct it so that it runs without producing syntax errors
birthday = '2017-07-14'
case_id = 'DATACAMP!123-456?'
```

# Load a DataFrame
- Use pd.read_csv() to load data from a CSV file called ransom.csv. This file represents the frequency of each letter in the ransom note for Bayes.

Solution: 
```
# Import pandas
import pandas as pd

# Load the 'ransom.csv' into a DataFrame
r = pd.read_csv('ransom.csv')

# Display DataFrame
print(r)
```

# Correcting a function error
Correct the code so that it runs without syntax errors.
```# One or more of the following lines contains an error
# Correct it so that it runs without producing syntax errors

# Plot a graph
plt.plot(x_values y_values)

# Display the graph
plt.show()
```

Solution: 
```
# One or more of the following lines contains an error
# Correct it so that it runs without producing syntax errors

# Plot a graph
plt.plot(x_values, y_values)

# Display the graph
plt.show()
```

# Snooping for suspects
Create a variable called plate that represents the observed license plate: the first three letters were FRQ, but the witness couldn't see the final 4 letters. Use asterisks (*) to represent missing letters. 

Solution: 
```
# Define plate to represent a plate beginning with FRQ
# Use * to represent the missing four letters
plate = 'FRQ****'
```
