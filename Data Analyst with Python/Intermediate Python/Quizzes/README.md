## Quiz 1: Scatter plot
When you have a time scale along the horizontal axis, the line plot is your friend. But in many other cases, when you're trying to assess if there's a correlation between two variables, for example, the scatter plot is the better choice. Below is an example of how to build a scatter plot.

```
import matplotlib.pyplot as plt
plt.scatter(x,y)
plt.show()
```

Let's continue with the ```gdp_cap``` versus ```life_exp``` plot, the GDP and life expectancy data for different countries in 2007. Maybe a scatter plot will be a better alternative?

Again, the ```matplotlib.pyplot``` package is available as ```plt```.

_**Instructions**_
- Change the line plot that's coded in the script to a scatter plot.
- A correlation will become clear when you display the GDP per capita on a logarithmic scale. Add the line ```plt.xscale('log')```.
- Finish off your script with ```plt.show()``` to display the plot.

***Solution:***

```
# Change the line plot below to a scatter plot
plt.scatter(gdp_cap, life_exp)
 
# Put the x-axis on a logarithmic scale
plt.xscale('log')
 
# Show plot
plt.show()
```

## Quiz 2: Scatter plot (2)
In the previous exercise, you saw that the higher GDP usually corresponds to a higher life expectancy. In other words, there is a positive correlation.

Do you think there's a relationship between population and life expectancy of a country? The list ```life_exp``` from the previous exercise is already available. In addition, now also ```pop``` is available, listing the corresponding populations for the countries in 2007. The populations are millions of people.

***Instructions***
- Start from scratch: ```import matplotlib.pyplot as plt```.
- Build a scatter plot, where ```pop``` is mapped on the horizontal axis, and ```life_exp``` is mapped on the vertical axis.
- Finish the script with ```plt.show()``` to actually display the plot.

***SOLUTION***

```
# Import package
import matplotlib.pyplot as plt
 
# Build Scatter plot
plt.scatter(pop, life_exp)
 
# Show plot
plt.show()
```


