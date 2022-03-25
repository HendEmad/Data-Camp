Feature selection is the process of reducing the input variables to the model by using only relevant data and get rid of noise of the data.
example: Consider we have a dataset of a library that wants to denote some old books to make place in their shells for new books and we want to train a model to automate this task. The features we have are: (Name, no.of times read, condition of the book, color). In this case, color of the book is not matter and keeping it can cause a model to learn to denote books based on color, we can remove it as a feature.

Using feature selection, we can optimize the model in several ways:
1. Prevent learning from noise(overfitting).
2. Prevent the wrong prediction, which means improving accuracy(getting predictions that are close to the right answer)
3. Reduce the training time

# Feature selection methods:
**1. For supervised learning: Used the output label class for feature selection**
   i. Intrinsic
   ii. Wrapper method
   iii. Filter method
**2. For unsupervised learning**

### 1- Filter method:
Features are dropped based on their relation or how they are correlated to the output.
![this is an image](https://analyticsindiamag.com/wp-content/uploads/2019/04/filte.jpg)

### 2- Wrapper method:
we split the data into subsets and train a model using this. Based on the output of the model, we add and subtract seatures and train the model again.
![this is an image](https://www.analyticsvidhya.com/wp-content/uploads/2016/11/Wrapper_1.png)
