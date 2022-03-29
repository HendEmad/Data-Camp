# Making a scatter plot:
The scatter plot allow to show where each data point sits on a grid.

**_Line plots_** to visualie orderd data points, but **_Scatter plots_** to visualize un-ordered points.

for example, learning about how some people grow during heir first yeat of life

![Capture](https://user-images.githubusercontent.com/91827137/160655423-356246bd-ab9c-4ff4-bcb9-588eef8f8efb.PNG)

To create a scatter plot using matplotlib library --> ```plt.scatter(df.x_data, df.y_data)```

To add labels:
```
plt.xlabel('string_name')
plt.ylabel('string_name2')
plt.show()
```

To change the marker style --> (maker = 's' or 'd' or ....etc ) keyword argument.

To change the marker color --> (clolr = 'new_name' ) keyword argument.

If we try to plot many points on the same scatter plot, they will interfere.
![Capture](https://user-images.githubusercontent.com/91827137/160657654-708bfc99-6461-421a-9846-5b8184654784.PNG)

To make it easier to read, we use a keyword **_alpha_** 
**_Alpha_** --> accepts a number between 0 and 1 and makes each marker transparent. The smaller the alpha parameter, the more transparent the lot
```
plt.scatter(df.x_data, df.y_data, alpha = 0.1)
```

### The darker areas have may points, the lighter areas have fewer points.

# Making a bar chart
bar chart is the best way to visualize a comparison of categorical data, so x_label will be created automatically.

the function used is ```plt.bar()``` and it takes two arguments: the labels for each bar, and the height of each bar. 
 
To make a horizontal bar chart ---> we use the function ```plt.barh()```. It is useful when having many bars.

_**note**_: average dosen't always tell the full story, there will be some sort of error assiciated with our such as standard deviation or standard error of the mean.
we can add error bars to our bar chart by using keyword ```yerr``` after the first two positional arguments in ```plt.bar(x_label, y_label, yerr = df.error)```. in this case, we are filling in yerr with a column of our dataframe called 'error'.

ex:
```
plt.bar(df.precinct, df.pet_abductions, yerr = df.error)
plt.ylabel('pet avductions')
plt.show()
```
![Capture](https://user-images.githubusercontent.com/91827137/160698345-7f810876-f5fc-46ce-b042-57965a57834d.PNG)

# Stacked bar charts
we display two different sets of bars
![Capture](https://user-images.githubusercontent.com/91827137/160698762-52f9e403-04cf-4568-aed7-5bcce2179f4d.PNG)

Here, for this example:
- The height of each blue bar represents the no. of dogs.
- The height of each orange bar represents the no. of cats.
- The total height of the blue and orange bars represents the total no. of pets for each city.

Also, for the same example:
- to create the stacked bar chart:
we start by plotting dogs column as usual. ```plt.bar(df.precinct, df.dog)``` --> the blue bar

Next. we stack the cat bars on the top of the dog bars by using the keyword ```bottom```

```plt.bar(df.precinct, df.cat, bottom = df.dog)```

So, to create the full example code for the last plot:
```
plt.bar(df.precinct, df.dog, label = 'Dog')
plt.bar(df.precinct, df.cat, label = 'Cat')
plt.legend()
plt.show()
```

