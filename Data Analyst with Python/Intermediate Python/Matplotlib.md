## Histogram
we use it to get an idea about the distribution.

***To create them***
```
import matplotlib.pyplot as plt
help(plt.hist) //to get the documentation
```

The parameters of ```plt.hist()``` are:
- X --> A list of values we want to build a histogram for --> we should define them to python.
- The second argument, bins, tells python how many bins the data should be divided.

Based on these numbers, hist will automatically find appropriate boundries for all bins, and calculate how many values in each one.

If we don't specify the bins arguments, it will be ```10``` by default.

ex:
```
values = [0, 0.6, 1.4, 1.6, 2.2, 2.5, 2.6, 3.2, 3.5, 3.9, 4.2, 2.6]
plt.hist(values, bins = 3)
plt.show()
```

