# Ridge-Regression
What is Ridge Regression?

**Rige Regression is a variation of Linear Regression**

Linear Regression is a simple yet powerful linear model which predicts the dependent variable using linear combination of various independent variables.

Ridge regression is one of the simple techniques to reduce model complexity and prevent over-fitting which may result from simple linear regression.

***Ridge Regression : In ridge regression, the cost function is altered by adding a penalty equivalent to square of the magnitude of the coefficients.***

***Cost function for a simple Linear Regression:***

![image](https://user-images.githubusercontent.com/44360746/64410995-d2c4fe80-d0be-11e9-8b0d-00ec7be77e67.png)

This method finds the co efficients without any bias to the features that best fits the data. OLS doesnt consider which independent variable is more important in the prediction. So there is only one set of weights (coefficients). 

***Cost function for a Ridge Regression:***

![image](https://user-images.githubusercontent.com/44360746/64411039-ef613680-d0be-11e9-872d-7fda2b0c97a2.png)

This method finds co efficients with a bias to the features by altering the lambda. Bias means how equally a model cares about its predictors. Let’s say there are two models to predict an apple price with two predictor ‘sweetness’ and ‘shine’; one model is unbiased and the other is biased. Therefore, an OLS model becomes more complex as new variables are added.

The term with lambda is often called ‘Penalty’ since it increases RSS. We iterate certain values onto the lambda and evaluate the model with a measurement such as ‘Mean Square Error (MSE)’. So, the lambda value that minimizes MSE should be selected as the final model. 

***Never becomes to zero***

As we increase the lambda value, the weight decreases. It converges to zero but never becomes zero. It gives different importance to the weights but never drops the unimportant features.  

# Results

On performing experiments with the house dataset available in scikit library, below are the results.

**Dataframe**

x-special/nautilus-clipboard
copy
file:///home/praveen/Pictures/Screenshot%20from%202019-09-06%2016-09-04.png

**Coefficients for different values of lambda**

x-special/nautilus-clipboard
copy
file:///home/praveen/Pictures/Screenshot%20from%202019-09-06%2016-11-26.png



