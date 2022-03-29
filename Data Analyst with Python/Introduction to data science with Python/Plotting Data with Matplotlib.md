# Creating line plots
#### 1. Importing the mpdule:
```from matplotlib import pyplot as plt```

### 2. Creating and displaying the line plot:
**#Creating the plot**
plt.plot(first positional argument(x-values), second positional argument(y-values))

ex: ```plt.plot(data1.x_values, data1.y_values)```

**#Displaying thr plot**

plt.show()        #Tankes no arguments

we can add another commands(lines) as title line or another line to be plotted.

**_If we want to plot multiple lines on the samw axis: _**

we add a second ```plt.plot(first positional argument(x-values), second positional argument(y-values))```. for example:
```plt.plot(data2_xvalues, data2_yvalues)```

# Adding labels and legends

we need to add labels ans legends to make communication to judges easier.

### Axes and title labels

**label x_axis: **```plt.xlabel("string_represents_the_xlabel")```

**label y_axis: **```plt.ylabel("string_represents_the_ylabel")```

**title: **```plt.title("string_represents_the_ylabel")```

These 3 functions must come before ```plt.show()``` as this function only displaying all what we did.

# Legends:

we can add it using the keyword argument **'label'** to each instance of ```plt.plot()```

In order to display the legend: ```plt.legend()``` as ```plt.show()``` will display only the line with its x&y_labels and its title.

example:
```
plt.plot(aditya.days, aditya.cases, label = "Aditya")
plt.plot(deshaun.days, deshaun.cases, label = "Deshaun")
plt.plot(mengfei.days, mengfei.cases, label = "Mengfei")
plt.legend()
```

The output will be
![Capture](https://user-images.githubusercontent.com/91827137/160604400-5c17c50d-45d7-49e4-a407-a0e37f7ffa4c.PNG)

 ## To add a quick note directly onto the plot:
 
 Using function ```plt.text(x_coor._where_thetext_isadded, y_coor._where_thetext_isadded, thetext_tobe_displayes_asastring)```, this takes 3 arguments 
 
 for example: ```plt.text(5, 9, "Unusually low H frequency")```--> The note will appear at the coordinate (5, 9) ![Capture](https://user-images.githubusercontent.com/91827137/160605063-d811e08b-96e2-4963-929d-c474185d4208.PNG)

# Modifying text:

**_Change font size: _** ```fontsize = n``` keyword argument

**_Change [font color](https://en.wikipedia.org/wiki/Web_colors): _** ```color = "new_color"``` keyword argument

example:
```
plt.title("plot title", fontsize = 20)
plt.legend(color = "green")
```
