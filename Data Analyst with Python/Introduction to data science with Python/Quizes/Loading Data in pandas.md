# Loading Data in pandas

- Import the pandas module under the alias pd.
- Load the CSV "credit_records.csv" into a DataFrame called credit_records.
- Display the first five rows of credit_records using the .head() method.

Solution:
```
# Import pandas under the alias pd
import pandas as pd

# Load the CSV "credit_records.csv"
credit_records = pd.read_csv("credit_records.csv")

# Display the first five rows of credit_records using the .head() method
print(credit_records.head())
```

# Inspecting a DataFrame
Use the .info() method to inspect the DataFrame credit_records.

Solution: 
```
# Use .info() to inspect the DataFrame credit_records
print(credit_records.info())
```

# Two methods for selecting columns
- Select the column item from credit_records using brackets and string notation.
- Select the column item from credit_records using dot notation.

Solution: 
``` 
# Select the column item from credit_records
# Use dot notation
items = credit_records.item

# Display the results
print(items)
```

# Correcting column selection errors
Correct the code so that it runs without errors.
```
# One or more lines of code contain errors.
# Fix the errors so that the code runs.

# Select the location column in credit_records
location = credit_records[location]

# Select the item column in credit_records
items = credit_records."item"

# Display results
print(location)
```

Solution: 
```
# One or more lines of code contain errors.
# Fix the errors so that the code runs.

# Select the location column in credit_records
location = credit_records['location']

# Select the item column in credit_records
items = credit_records.item

# Display results
print(location)
```

# More column selection mistakes
Inspect the DataFrame mpr using info().


Solution:
```
print(mpr.info())
```

# Logical testing
The variable height_inches represents the height of a suspect. Is height_inches greater than 70 inches?

Solution:
```
# Is height_inches greater than 70 inches?
print(height_inches > 70)
```

# Selecting missing puppies
- Select the dogs where Age is greater than 2.
- Select the dogs whose Status is equal to Still Missing.
- Select all dogs whose Dog Breed is not equal to Poodle.

Solution:
```
# Select the dogs where Age is greater than 2
greater_than_2 = mpr[mpr.Age > 2]
print(greater_than_2)

# Select the dogs whose Status is equal to Still Missing
still_missing = mpr[mpr.Status ==  'Still Missing']
print(still_missing)

# Select all dogs whose Dog Breed is not equal to Poodle
not_poodle = mpr[mpr['Dog Breed'] != 'Poodle']
print(not_poodle)
```

# Narrowing the list of suspects
Select rows of credit_records such that the column location is equal to 'Pet Paradise'.

Solution:
```
# Select purchases from 'Pet Paradise'
purchase = credit_records[credit_records.location == 'Pet Paradise']

# Display
print(purchase)
```

