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

![Dataframe](https://user-images.githubusercontent.com/44360746/64412267-98109580-d0c1-11e9-9eb9-9b29ba406b90.png)

**Coefficients for different values of lambda**

![Weights](https://user-images.githubusercontent.com/44360746/64412222-84652f00-d0c1-11e9-8c0e-5b27562fc3ce.png)

**Regression Trace**

![Trace](https://user-images.githubusercontent.com/44360746/64412352-c8583400-d0c1-11e9-9442-94af00faf363.png)

‘Room’ should be the best indicator for house price by intuition. This is why the line in red does not quite shrink over iteration. On the contrary, ‘Highway Access’ (blue) decreases remarkably, which means the feature loses its importance as we seek more general models.

**Comparision to OLS**

![](https://user-images.githubusercontent.com/44360746/64412508-140add80-d0c2-11e9-8b7b-f763e97ee1b9.png)

The green dotted line is from OLS on the graph above with the X-axis being drawn by increasing lambda values. The MSE values decreases in the beginning as the lambda value increases, which means the model prediction is improved (less error) to a certain point. In short, an OLS model with some bias is better at prediction than the pure OLS model, we call this modified OLS model as the ridge regression model.

# Conclusion

    OLS simply finds the best fit for given data
    Features have different contributions to RSS
    Ridge regression gives a bias to important features
    MSE or R-square can be used to find the best lambda

**Additional**

Lasso Regression : The cost function for Lasso (least absolute shrinkage and selection operator) regression can be written as

![image](https://user-images.githubusercontent.com/44360746/64412718-9a272400-d0c2-11e9-81b8-f9b5d98db410.png)


This type of regularization (L1) can lead to zero coefficients i.e. some of the features are completely neglected for the evaluation of output. So Lasso regression not only helps in reducing over-fitting but it can help us in feature selection. Just like Ridge regression the regularization parameter (lambda) can be controlled.
