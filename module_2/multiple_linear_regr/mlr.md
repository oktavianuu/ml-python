## Multiple Linear Regression
It is the extension of simple linear regression. The only difference is that multiple linear regression, just like its name, has multiple independent variable.

#### What kind of problem can multiple linear regression solve?
- when we would like to identify the strength of the effect that the dependent variables have on dependent variable. For example, does revision time, test anxiety, lecture attendance and gender have any effect on exam performance of student?
- to predict the impact of changes; that is to understand how the dependent variable changes when we change the independent variables. For example, if we were reviewing a person's health data, a multiple linear regression can tell how much that person's blood pressure goes up or down for every unit increase or decrease in a patient's body mass index (BMI), holding other factors constant. 

#### Multiple Linear Regression Model
$$
\hat{y} = \theta_0 + \theta_1 x_1 + \theta_2 x_2 + ... + \theta_n x_n
$$
Explanation:
- $\theta$ is the coefficient and the parameter
- x is the feature set

#### How do we optimize the parameters?
1. understand what optimized parameters are, in short, optimized parameters are the one which lead to a model with fewest error.
2. to find the error, we just need to find the difference between our predicted value and original value. 
3. We look at the MSE (mean squared error) to see how good does our model representing the dataset. It is the mean of residual error. 
4. the best model is the one with minimum MSE. 
5. to minimize it, we must find the best value for $\theta$, but how?

#### Find the best $\theta$
Most common methods are ordinary least square (OLS) and optimization approach.
- OLS tries to estimate coefficients' value by minimizing MSE. This approach uses data matrix and linear algebra operations to estimate optimal $\theta$ value. This approach has problem that is time complexity of calculating matrix operations, as it can take very long time to finsih. If the number of rows is less than 10,000, there might be no problem of choosing this method. 
- Optimization algorithm, a process of optimizing the values of the coefficients by iteratively minimizing the error of the model on the training data. For example, we can use gradient descent which starts optimization by random values for each coefficient. Then calculate the errors and tries to minimize it through wise changing of the coefficients in multiple iterations. **Gradient descent** is best for large dataset. 
- There are many other approach as well. 
- After we find the best parameter, we can proceed to the prediction.

#### How many independent variables are best?
- Should we use all independent variables in our dataset?
- Too many variables causing over-fitting. Means that our model is too complicated and not general enough for predition. 
- the relationship of dependent and independent variables should be linear as its name of the method. We can use scatterplot to visualize the relationship.
