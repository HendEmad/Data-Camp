# Charting cellphone data
We know that Freddy Frequentist is the one who kidnapped Bayes the Golden Retriever. Now we need to learn where he is hiding.

Our friends at the police station have acquired cell phone data, which gives some of Freddie's locations over the past three weeks. It's stored in the DataFrame cellphone. The x-coordinates are in the column 'x' and the y-coordinates are in the column 'y'.

The matplotlib module has been imported under the alias plt.

**Instructions**
- Display the first five rows of the DataFrame and determine which columns to plot.
- Create a scatter plot of the data in cellphone.

```solution```
```
# Explore the data
print(cellphone.head())

# Create a scatter plot of the data from the DataFrame cellphone
plt.scatter(cellphone.x, cellphone.y)

# Add labels
plt.ylabel('Latitude')
plt.xlabel('Longitude')

# Display the plot
plt.show()
```

# Modifying a scatterplot
In the previous exercise, we created a scatter plot to show Freddy Frequentist's cell phone data.

In this exercise, we've done some magic so that the plot will appear over a map of our town. If we just plot the data as we did before, we won't be able to see the map or pick out the areas with the most points. We can fix this by changing the colors, markers, and transparency of the scatter plot.

As before, the matplotlib.pyplot module has been imported under the alias plt, and the cellphone data is in the DataFrame cellphone.

**Instructions**
- Change the color of the points to 'red'.
- Change the marker shape to square.
- Change the transparency of the scatterplot to 0.1.

```solution```
```
# Change the transparency to 0.1
plt.scatter(cellphone.x, cellphone.y,
           color = 'red',
           marker = 's',
           alpha = 0.1)

# Add labels
plt.ylabel('Latitude')
plt.xlabel('Longitude')

# Display the plot
plt.show()
```

