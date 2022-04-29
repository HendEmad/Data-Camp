## Dictionaries
- It cantains values and keys --> ```dict = {'key1' : 'value1', 'key2' : 'value2', ......}```

- ex: ```world = {'egypt' : 100, 'albania' : 2.77, 'algeria' : 36.21}```

- To access the values --> ```.values()``` method --> ```print(world.values())```

- To access keys --> ```.keys()``` method--> ```print(world.keys())```

- The keys should be **_unique_**.  if we try to add another repeated key, the output will contain only one of the repeated keys. 

- The keys have to be **_immutable_** which means that the content of them cannot be changed after they are created.

- dict = {0 : 'hello', True : 'dear', 'two' : 'world'} --> Valid dictionary

- dict = {['just', 'to', 'test'] : 'value'} --> Not valid dictionary

- To add new values to it: ```dict_name['new_key'] = new_value``` --> 
ex: ```world['sealand'] = 0.0027```

- To check if the key and value of it are added:
 ```'new_key' in dict_name``` --> ex: ```'sealand' in world``` --> The output will be boolean(true or false)
 
- Because the keys are unique, we can change any value in the same way as creating a new one --> ex: world['sealand'] = 0.0028 --> here we changed the value of the key seabland

- To remove a value with its key --> ```del() function``` --> ex: ```del(world['sealand'])```

- List vs. Dictionary

![Capture](https://user-images.githubusercontent.com/91827137/165941279-3ad785f7-5eb4-466e-95a5-2a28554341c7.PNG)

## Pandas
- A data manipulation and analysis tool.
- It adds to python pandas series and pandas dataFrame.

### Creating Pandas DataFrame
### 1.  Manually --> From Dictionary:

```
# importing
import pandas as pd

# Creating pandas dataframe from a dictionary
# The keys represent the column labels of the dataframe, the values represent the observations (data column by column)
dict = {
    'Country' : ['Brazil', 'Russia', 'India', 'China', 'South Africa'],
    'Capital' : ['Brasilia', 'Moscow', 'New Delhi', 'Beijing', 'Pretoria'],
    'Area' : [8.516, 17.10, 3.286, 9.597, 1.221],
    'Population' : [200.4, 143.5, 1252, 1357, 52.98]
}

# Converting the dictionary to the Pandas DataFrame
brics = pd.DataFrame(dict)
print(brics)
```

_Output_

![Capture](https://user-images.githubusercontent.com/91827137/165949558-4c9199ff-567e-4bb5-93bd-367618560945.PNG)

The list from 0 to 4 labels are created automatically but we can change it:

```
# Changing the lablels:
brics.index = ['BR', 'RU', 'IN', 'CH', 'SA']
print(brics)
```

_Output_

![Capture](https://user-images.githubusercontent.com/91827137/165949735-b27d6031-247f-4bdc-8682-ba12436fa572.PNG)

### 2. From external file
```
brics = pd.read_csv("file_path")
print(brics)
```

_Output_

![Capture](https://user-images.githubusercontent.com/91827137/165950131-de9fd8e6-a934-4a21-8f20-3517fcf5d40c.PNG)

To remove the additional labels that are created automatically by Pandas:

Set the argument ```index_col``` to 0 --> 
ex: ```brics = pd.read_csv("file_path", index_col = 0)```

_Output_

![Capture](https://user-images.githubusercontent.com/91827137/165950644-ac6338dd-eccc-4f64-9daf-f23048f4dfd8.PNG)
