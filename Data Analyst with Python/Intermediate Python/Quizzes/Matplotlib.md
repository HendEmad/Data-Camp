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

## Quiz 3: Build a histogram (1)
- Use [```plt.hist()```](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.hist.html) to create a histogram of the values in ```life_exp```. Do not specify the number of bins; Python will set the number of bins to 10 by default for you.

- Add ```plt.show()``` to actually display the histogram. Can you tell which bin contains the most observations?

***Solution***

```
# Create histogram of life_exp data
import matplotlib.pyplot as plt
plt.hist(life_exp)


# Display histogram
plt.show()
```

![28](https://user-images.githubusercontent.com/91827137/164701711-3fabea6d-dfa7-407a-bf0e-c293bc045035.PNG)

- The bin containing the most observations is the highest one.

![29](https://user-images.githubusercontent.com/91827137/164702657-0013caba-332d-4677-bd13-06b1b841cbe4.PNG)

## Quiz 4: Build a histogram (2): bins
The number of bins is pretty important. Too few bins will oversimplify reality and won't show you the details. Too many bins will overcomplicate reality and won't show the bigger picture.

- Build a histogram of ```life_exp```, with ```5``` bins. Can you tell which bin contains the most observations?
- Build another histogram of ```life_exp```, this time with ```20``` bins. Is this better?

***Solution***
```
# Build histogram with 5 bins
import matplotlib.pyplot as plt
plt.hist(life_exp, bins = 5)

# Show and clean up plot
plt.show()
plt.clf()

# Build histogram with 20 bins
plt.hist(life_exp, bins = 20)

# Show and clean up again
plt.show()
plt.clf()
```

![30](https://user-images.githubusercontent.com/91827137/164703250-a3627293-e26a-4ade-bfb6-5d2c5f78fe28.PNG)

## Quiz 5: Choose the right plot (1)
You want to visually assess if the grades on your exam follow a particular distribution. Which plot do you use?

```Answer``` Histogram

## Quiz 6: Choose the right plot (2)
You want to visually assess if longer answers on exam questions lead to higher grades. Which plot do you use?

```Answer``` Scatter Plot

## Quiz 7: Sizes(scatter plot dots' size)
Right now, the scatter plot is just a cloud of blue dots, indistinguishable from each other. Let's change this. Wouldn't it be nice if the size of the dots corresponds to the population?

To accomplish this, there is a list pop loaded in your workspace. It contains population numbers for each country expressed in millions. You can see that this list is added to the scatter method, as the argument s, for size.

***Instructions***
- Run the script to see how the plot changes.
- Looks good, but increasing the size of the bubbles will make things stand out more.
   - Import the numpy package as np.
   - Use np.array() to create a numpy array from the list pop. Call this NumPy array np_pop.
   - Double the values in np_pop setting the value of np_pop equal to np_pop * 2. Because np_pop      is a NumPy array, each array element will be doubled.
   - Change the s argument inside plt.scatter() to be np_pop instead of pop.

```Solution```

```
# Import numpy as np
import numpy as np

# Store pop as a numpy array: np_pop
np_pop = np.array(pop)

# Double np_pop
np_pop *= 2

# Update: set s argument to np_pop
# Output before changing the dots' size: plt.scatter(gdp_cap, life_exp, s = pop)
# Output after changing the dots' size
plt.scatter(gdp_cap, life_exp, s = np_pop)

# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')
plt.xticks([1000, 10000, 100000],['1k', '10k', '100k'])

# Display the plot
plt.show()
```

_Output before changing the dots' size_

![Capture](https://user-images.githubusercontent.com/91827137/165742215-79f9c0b3-58a6-4d56-b834-da5365b94130.PNG)

_Output after changing the dots' size_

![Capture](https://user-images.githubusercontent.com/91827137/165742726-d18bc1a0-d36f-46bb-a6df-93348d727729.PNG)

## Quiz 8: Colors
The next step is making the plot more colorful! To do this, a list col has been created for you. It's a list with a color for each corresponding country, depending on the continent the country is part of.

How did we make the list col you ask? The Gapminder data contains a list continent with the continent each country belongs to. A dictionary is constructed that maps continents onto colors:

``` 
dict = {
    'Asia':'red',
    'Europe':'green',
    'Africa':'blue',
    'Americas':'yellow',
    'Oceania':'black'
}
```

***Instructions***
- Add c = col to the arguments of the plt.scatter() function.
- Change the opacity of the bubbles by setting the alpha argument to 0.8 inside plt.scatter(). Alpha can be set from zero to one, where zero is totally transparent, and one is not at all transparent.

```Solution```

```
# Specify c and alpha inside plt.scatter()
plt.scatter(x = gdp_cap, y = life_exp, s = np.array(pop) * 2, c = col, alpha = 0.8)

# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')
plt.xticks([1000,10000,100000], ['1k','10k','100k'])

# Show the plot
plt.show()
```

_output-

![Capture](https://user-images.githubusercontent.com/91827137/165743454-de1c70db-331a-42e0-9615-9d01d6a47c61.PNG)

# Quiz 9: Additional Customizations
Add plt.grid(True) after the plt.text() calls so that gridlines are drawn on the plot.

```Solution```

```
# Scatter plot
plt.scatter(x = gdp_cap, y = life_exp, s = np.array(pop) * 2, c = col, alpha = 0.8)

# Previous customizations
plt.xscale('log') 
plt.xlabel('GDP per Capita [in USD]')
plt.ylabel('Life Expectancy [in years]')
plt.title('World Development in 2007')
plt.xticks([1000,10000,100000], ['1k','10k','100k'])

# Additional customizations
plt.text(1550, 71, 'India')
plt.text(5700, 80, 'China')
# The First and Second parameters represents the position where the word 'India' or 'China' will display on the grid.

# Add grid() call
plt.grid(True)

# Show the plot
plt.show()
```

_Output_

![Capture](https://user-images.githubusercontent.com/91827137/165743938-fff7b7a8-2711-4104-b7aa-8c4053512ba6.PNG)
