The classification problems have discrete and finite outputs(classes / categories). for example classifying if the emails are spam(true) or not(false).

Classification problems have two main types:

1- Binary(Binomial classification): Two classes(true or false/ 0 or 1/ positive or negative) to choose from.

2- Multiclass(multinomial classification): Three or more classes to choose from.

Logistic Regression:
Supervised learning model that is used in classification problems where there are only two classes, it performs the classification by applying the sigmoid function for which the formula is: 1 / (1 + e^-t)

for example: spam filtering(spam 1 or not 0), tumor classification(malignant1 or not 0).  



* Logistic regression assumptions:
1- The dependent variable must be binary.

2- The desired output should be represented with the factor level 1(In binary regression).

3- The meaningful variables only included in the model.

* Advantages and Disadvantages:
Advantages	Disadvantages
Easy to implement and very efficient to train.

Quite sensitive to noise.

It also can affect performance is the independent variables are correlated.

have good accuracy. It performs well in linearity separable datasets and it requires less training.

It may lead to overfitting if the no. of observations is smaller than the no. of features.
Less inclined to overfitting . It can overfit in high dimensional datasets, but it can be avoided using regularization techniques.

It has a linear decision surface, so can't be used to solve non-linear problems although the linearly separate data is rarely in real- world problems.

Logit function : Z = Yi * (W^T)Xi
Where (W^T)Xi represents the distance between the point i the straight line.

- It the point is above the straight line, the values of the points are positive Yi = +1 =, hence (W^T)Xi > 0

- If the points are below the straight line, thy are negative Yi = -1 , hence (W^T)Xi < 0.

y = (W^T)Xi + b where:

intercept b = 0; Y = (W^T)X; Green = +1; Red = -1

-There are four cases:

1- Case 1: green point is above the plane --> Yi = +1, (W^T)Xi > 0 --> Result = Yi * (W^T)Xi > 0 --> Outcome: Good(correct) classification.

2- Case 2: green point is below the plane --> Yi = +1, (W^T)Xi < 0 --> Result = Yi * (W^T)Xi < 0 --> Outcome: Bad(incorrect) classification.

3- Case 3: red point is below the plane --> Yi = -1, (W^T)Xi < 0 --> Result = Yi * (W^T)Xi > 0 --> Outcome: Good(correct) classification.

4- Case 4: red point is above the plane --> Yi = -1, (W^T)Xi > 0 --> Result = Yi * (W^T)Xi < 0 --> Outcome: Bad(incorrect) classification.

Cost Function: maximizing the sum of all logic function outcomes for the data points in the dataset . so, if we have 1 million records, we will have 1 million logit function outcomes which represent the classification of the records and at the end, all of them are summed up. The higher the sum, the better classification of the record is performed.

This result is used to decide where the best fit line should be placed in order to separate the two classes in the best way possible and on each iteration, we are updating the omega value(W) then the part (W^T ),; because y is always +1 or -1 and the value of the record in the dataset. So, if the point is 10 that means that the value for x is going to be 10.

- The sigmoid function is used to mitigate the issue with outliers by normalizing the results calculated by the logic function and transforming them to values in the range between 0 and 1 which is done by applying the formula: Sigmoid f(z) = 1 / (1 + e^-z) where '-z' is the result of the logic function for the specific record, and 'e' is a constant with value 2.718  
