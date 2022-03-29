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

# Build a simple bar chart
Officer Deshaun wants to plot the average number of hours worked per week for him and his coworkers. He has stored the hours worked in a DataFrame called hours, which has columns officer and avg_hours_worked. Recall that the function plt.bar() takes two arguments: the labels for each bar, and the height of each bar. Both of these can be found in our DataFrame.

**Instructions **

- Display the DataFrame hours using a print command.
- Create a bar chart of the column avg_hours_worked for each officer from the DataFrame hours.
- Use the column std_hours_worked (the standard deviation of the hours worked) to add error bars to the bar chart.

```Solution```
```
# Display the DataFrame hours using print
print(hours)

# Create a bar plot from the DataFrame hours
plt.bar(hours.officer, hours.avg_hours_worked,
        # Add error bars
        yerr=hours.std_hours_worked)

# Display the plot
plt.show()
```

# Where did the time go?
Officer Deshaun wants to compare the hours spent on field work and desk work between him and his colleagues. In this DataFrame, he has split out the average hours worked per week into desk_work and field_work.

You can use the same DataFrame containing the hours worked from the previous exercise (hours).

**Instructions **
- Create a bar plot of the time each officer spends on desk_work.
- Label that bar plot "Desk Work".
- Create a bar plot for field_work whose bottom is the height of desk_work.
- Label the field_work bars as "Field Work" and add a legend.

```Solution```
```
# Plot the number of hours spent on desk work
plt.bar(hours.officer, hours.desk_work, label='Desk Work')

# Plot the hours spent on field work on top of desk work
plt.bar(hours.officer, hours.field_work, bottom = hours.desk_work, label = 'Field Work')

# Add a legend
plt.legend()

# Display the plot
plt.show()
```

