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
![this is an image](https://www.google.com/url?sa=i&url=https%3A%2F%2Fanalyticsindiamag.com%2Fwhat-are-feature-selection-techniques-in-machine-learning%2F&psig=AOvVaw32q21CnzVKlrhBSdrekMh4&ust=1648303893580000&source=images&cd=vfe&ved=0CAsQjRxqFwoTCPDlg9q44fYCFQAAAAAdAAAAABAS)
l
