## Line plot
- The most basic plot.
- to build it:
```
import matplotlib.pyplot as plt
plt.plot(x,y)
plt.show()
```

## Scatter Plot (1)
- When we are trying to assess if thereis a correlation between two variables, the scatter plot if better choice
- To build it:
```
import matplotlib.pyplot as plt
plt.scatter(x,y)
plt.show()
```
- sometimes a correlation will become clear when we display one of the variables on a logarithmic scale, to add it: ```plt.xscale('log') OR plt.yscale('log')``` 

## Histogram
- we use it to get an idea about the distribution of the variables.
- The height of the bar corresponds to the number of data points that fall in the bin.

![Capture](https://user-images.githubusercontent.com/91827137/165603874-2db85d61-3840-4d87-a489-51c9e69e8c72.PNG)

***To create them***
```
import matplotlib.pyplot as plt
help(plt.hist) //to get the documentation
```

The parameters of ```plt.hist()``` are:
- X --> A list of values we want to build a histogram for --> we should define them to python.
- The second argument, bins, tells python how many bins the data should be divided.

Based on these numbers, hist will automatically find appropriate boundries for all bins, and calculate how many values are in each one.

If we don't specify the bins arguments, it will be ```10``` by default.

ex:
```
values = [0, 0.6, 1.4, 1.6, 2.2, 2.5, 2.6, 3.2, 3.5, 3.9, 4.2, 2.6]
plt.hist(values, bins = 3)
plt.show()
```

Output:

![Capture](https://user-images.githubusercontent.com/91827137/165604570-4923531f-8ea0-463f-904b-c15bbf580bb5.PNG)

```notes``` 
- The bin containing the most observations is the highest one.
- Controlling no.of bins is pretty important. Too few bins will oversimplify reality and won't show us the details. Too many bins will overcomplicate reality and won't show the bigger picture.

