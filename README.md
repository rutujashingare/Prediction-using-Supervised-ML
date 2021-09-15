#   The Sparks Foundation -Graduation Rotational Internship Program
## Task  
● Predict the percentage of an student based on the no. of study hours.

● What will be predicted score if a student studies for 9.25 hrs/ day?

● This is a simple linear regression task as it involves just 2 variables.

● Dataset : http://bit.ly/w-data

## Linear Regression

Linear regression is a statistical regression-based method for predicting outcomes. It is one of the most basic and straightforward algorithms for calculating regression and displaying the relationship between continuous variables. 

Linear regression with only one input variable is known as simple linear regression. Multiple linear regression is the term used when there are multiple input variables in linear regression.

## Simple Linear Regression

A simple linear regression algorithm is used to find a linear relationship between two variables provided a training dataset. We want to model our data with simple linear regression like this: y = B0 + B1x + u

![image](https://user-images.githubusercontent.com/70087327/133466130-156e388c-762e-418e-a613-75c1aa68d6c1.png)


Above fig shows Simple Linear Regression Equation

This is an illustration of a line where, y is the output variable we want to predict, x is the known input variable, and B0 and B1 are the coefficients that pass the line around that we need to estimate. 
•	From a technical standpoint, as B0 defines where the line intersects the y-axis, it is referred to as the intercept. This is known as bias in machine learning because it is used to offset all of our predictions. 
•	The B1 term is called the slope because it defines the slope of the line or how x translates into a y value before we add our bias and u is the residual or noise that is caused by unexplained factors.
•	The goal is to find the best coefficient estimates to reduce the errors in predicting y from x.

## Objective
Our aim here is to predict student’s percentage based on the number of hours of studies. 

## Steps

### Step 1: Import Libraries and load dataset
 
### Step 2: Creating/Splitting train and test datasets

Our main dataset needs to be split into two arrays. This can be accomplished in the following manner:
X = d_f.iloc[:, :-1]. values  # No. of Hours
y = d_f.iloc[:, 1].values  # Scores

We'll divide the x and y datasets into four new ones: X_train, y_train, X_test, and y_test. The model will use datasets ending in _train to build a line of best fit, while datasets ending in _test will be used to test the model using an accuracy metric. 
We'll use 25% of the data for testing our model and 70% to train our model.


### Step 3: Fitting our simple linear regression model

To build and train our linear regressor, we must first create an object of Linear Regression by assigning it to a variable, then train it on our dataset using the .fit process.

### Step 4: Testing/Predicting our linear regression model

This phase will be as simple as the previous ones because we will be using the regressor. predict method on the test datasets we developed.


### Step 5: Visualizing our model

We'll be using the matplotlib library, which we set up at the start.
The .scatter approach takes two key parameters: the data points' x and y values. As you can see, we used X_test and y_test to send in the values of the testing data points. The third statement simply indicates what color the data points will be. 

![image](https://user-images.githubusercontent.com/70087327/133466742-538b70d6-4de5-4912-bd0e-90392f0bdfe1.png)


## Evaluating Model Performance

We can use MAE to determine how inaccurate the predictions were. The only difference between MSE and MAE is that instead of using the absolute value, it squares the difference between real and expected output values before summing them all. The R Squared metric is commonly used for explanatory purposes, and it shows how well a range of expected output values matches the real output values. 

Finally, we've built a simple linear regression model to predict a student's score. 


We will assign a value to our, i.e. number of hours studying in order to make predictions with the aid of our model, and our model i.e. will give us a score for the number of hours studied.


## Output

No. of hour studied = 9.8
Predicted Score = 93.69








