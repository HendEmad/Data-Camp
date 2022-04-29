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
