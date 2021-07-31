# Linear-Regression
How To Implement Simple Linear Regression From Scratch With Python
Linear regression is a prediction method that is more than 200 years old.

Simple linear regression is a great first machine learning algorithm to implement as it requires you to estimate properties from your training dataset, but is simple enough for beginners to understand.

In this tutorial, you will discover how to implement the simple linear regression algorithm from scratch in Python.

After completing this tutorial you will know:

1.How to estimate statistical quantities from training data.
2.How to estimate linear regression coefficients from data.
3.How to make predictions using linear regression for new data.

Description
This section is divided into two parts, a description of the simple linear regression technique and a description of the dataset to which we will later apply it.

Simple Linear Regression
Linear regression assumes a linear or straight line relationship between the input variables (X) and the single output variable (y).

More specifically, that output (y) can be calculated from a linear combination of the input variables (X). When there is a single input variable, the method is referred to as a simple linear regression.

In simple linear regression we can use statistics on the training data to estimate the coefficients required by the model to make predictions on new data.

The line for a simple linear regression model can be written as:

y = b0 + b1 * x
1
y = b0 + b1 * x
where b0 and b1 are the coefficients we must estimate from the training data.

Once the coefficients are known, we can use this equation to estimate output values for y given new input examples of x.

It requires that you calculate statistical properties from the data such as mean, variance and covariance.

All the algebra has been taken care of and we are left with some arithmetic to implement to estimate the simple linear regression coefficients.

Briefly, we can estimate the coefficients as follows:

B1 = sum((x(i) - mean(x)) * (y(i) - mean(y))) / sum( (x(i) - mean(x))^2 )
B0 = mean(y) - B1 * mean(x)
1
2
B1 = sum((x(i) - mean(x)) * (y(i) - mean(y))) / sum( (x(i) - mean(x))^2 )
B0 = mean(y) - B1 * mean(x)
where the i refers to the value of the ith value of the input x or output y.

Don’t worry if this is not clear right now, these are the functions will implement in the tutorial.

Swedish Insurance Dataset
We will use a real dataset to demonstrate simple linear regression.

The dataset is called the “Auto Insurance in Sweden” dataset and involves predicting the total payment for all the claims in thousands of Swedish Kronor (y) given the total number of claims (x).

This means that for a new number of claims (x) we will be able to predict the total payment of claims (y).

Here is a small sample of the first 5 records of the dataset.

108,392.5
19,46.2
13,15.7
124,422.2
40,119.4

Using the Zero Rule algorithm (that predicts the mean value) a Root Mean Squared Error or RMSE of about 81 (thousands of Kronor) is expected.
