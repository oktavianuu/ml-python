# <center>Topics<center>
- Regression
- Model Evaluation
- Model Evaluation; Overfitting and Underfitting
- Understanding Different Evaluation Model
- Simple Linear Regression

## <center>Regression<center>
- Regression is the process of predicting continuous value.
- There are two types of variable in regression:
  - dependent: is the target variable we try to study or predict (Y). Y value should be continuous and it totally cannot be discrete.
  - independent: the explanatory varible. A variable used to predict (X). The values of this variable can be categorical or continuous.
#### Two types of regression
- Simple: one independent variable is used to estimate dependent variable. 
  - linear
  - non-linar
- Multiple: more than one independent variable is present.
  - multiple linear 
  - multiple non-linear
#### Applications
- Sales forecasting 
- Price estimation
- Employment income
#### Regression Algorithm
- Ordinal regression
- Poisson regression
- Fast forest quantile regression
- Bayesian linear regression
- Neural network regression
- Decision forest regression
- KNN (K-nearest neighbors)
### Simple Linear Regression
In simple linear regression, there are only two variable exist. Dependent and independent variable. 
Simple Linear regression formula:
$$
\hat{y} = \theta_0 + \theta_1{x}_1
$$
__Explanation__:
$\theta_0$ and $\theta_1$ are the parameters of the line we must adjust. Also called the coefficients of linear equations.
$\theta_1$ = known as slope or gradient of the fitting line
$\theta_0$ = known as intercept

In other words, we can say that $\hat{y}$ being a function of $x_1$. Moreover, we must calculate the value of the slope and intercept in order to find the best fitted line. This line later will be used to predict the outcome of the incoming $x_1$ data points. Visually, the fitted line is used to see how differ is our prediction model to the actual value. for example if the distance between the  fitted line and the actual value is far, then the prediction is not accurate, meaning that we need to improve our model. The distance of between the data points with the fitted regression line is called `error` and we measure it, mathematically using `MSE` (Mean Squared Error). In regression, our objective is to minimize the value of `MSE`, the smaller the better which means that all of the distance of each data points to the fitted regression line is small.

The objective of linear regression is to minimize the `MSE` equation and to minimize its value. In order to do it, we must find the best parameters for our line, the value of $\theta_0$ and $\theta_1$.
If the value of those parameters are so important, then how we can calculate it? How can we find a perfect line? Move it randomly and calculate its MSE everytime we move the line?
There are two approach for this:
1. Use mathematic approach
2. Use an optimization approach

As discussed before $\theta_0$ and $\theta_1$ are the coefficients of the fit line. So here is how we do it:

**Mathematical Approach**
1. Calculate the average of x ($\bar{x}$) and y ($\bar{y}$).
2. Then we plug it into the slop equation to find $\theta_1$.
3. After we find the value of $\theta_1$, we plug the value again to the equation to find the $\theta_0$.
4. The $\theta_0$ is the bias coeffcient and the $\theta_1$ is the coefficient of $x_1$.
5. After we find all of the parameters, we can plug all values into the equations.

#### Model Evaluation in Regression Models
-  goal of regression: build a model to predict an unknown case. 
-  There are two approach to evaluate a model
   -  train and test on the same dataset
   -  train/test split

**How do we know that our model is accurate enough to predict and unknown case?**  
how to measure the accuracy of our model? How much we can trust the model?
1. Train and test on the same dataset
   - train our model on the whole dataset, let say we have 10 rows of data point, we use them all to train our data. Then after the model is built, we test our model for example on the row of 7 and 10 without label. Means that, we remove the target variable of those rows. After that, we compare our predicted and our actual value of the data. 
   - the accuracy of the model depends on the difference between predicted value and the actual value. 
   - the error of the model is calculated as the average difference between the predicted and the actual values of all rows. 
   - because we already now the target values for each data point, this approach gives us high training accuracy but low **out of sample accuracy**. 
   - Training accuracy is the percentage of correct predictions the model make during test
   - High training accuracy isn't necessarily a good thing. It may result in an over-fitting; overly trained to the dataset, capture noise and produce non-generalized model.
   - **Out of sample accuracy** is the percentage of correct predictions by the model on new dataset, the data that has not been training on. 
   - Doing **train and test** on the same dataset will most likely produce low out of sample accuracy because the model tend to overfit. 
   - We the expect the model to have high out of sample accuracy since the purpose of our model is to predict unknown data. 
2. Train/Test Split
   - Select a portion of our data for training, for example if we have 10 rows, rows 0-5 for training and the rest for testing. 
   - These training and testig set are mutually exclusive. We feed the training set during training and then feed the testing set during testing.
   - This approach usually produce a better model, meaning high out of sample accuracy, since the training and testing are on different dataset, closer to the real world scenario where the model must predict future unknown incoming data. 
   - The only problem with this method is its total dependency on the training and test data.
3. K-Fold Cross Validation
   - this method solves all of the problem above. 
   - concept: if k = 4 folds, means we divide the dataset into 4, 25% for testing and the rest for training. The accuracy for the model is calculated.
   - the model is built using training and evaluated using test set. 
   - then, on the next round of training, the second 25% or second fold is used for testing and the rest for training. Then again the accuracy is calculated. Then the same cycle is done until no fold remaining. 

#### Evaluation Metrics in Regression
Used to explain the performance of the model. In other words, it is used to evaluate a model. Some of them are:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

**Error**
In regression, error is the difference between the data points and the trend line generated by the algorithm. Since the data points are many, there will be many, more than one error value. 

**Mean Absolute Error (MAE)**
Mean of the absolute value of the errors, it is just the average of the error. 

**Mean Squared Error (MSE)**
- It is the mean of the squared error, the average of the error being squared.
- More popular than MAE, since the error is being squared meaning that larger errors are exponentianlly increase compared to smaller one.

**Root Mean Squared Error (RMSE)**
- The square root of the mean squared error. 
- most popular because it is interpretable as the response vector (y) making it easier to relate its information.

**Relative Absolute Error (RAE)**
later ...

**Relative Squared Error (RSE)**
- used to calculating R-squared.
- metrics for model accuracy.
- represents how close the data value to the fitted regression line. 
- the higher R-squared, the better the model fit the data

**What metrics to choose?**
- Type of model
- Data type
- Knowledge domain

## <center>Non Linear Regression <center>
If the data is not linear, then linear regression will not produce a satisfying result. Non linear indicated by curved line. 
- **Quadratic** regression line is a curved line (a parabola) that best fits the data. A curve that has one bend.
- **cubic** regression line is a more complex curved line that best fits the data. A curve that has two bends or a shallow "S" shape.
- These kind of non linear regression is called polynomial regression. 

**How can we know a problem is linear or non-linear?**
- Visually examine the relationship
  - plot bivariate plots of output and input variable
  - calculate the correlation coefficient between dependent and independent variables.
  - if the correlation coefficient is 0.7 or higher, it is linear (most likely)
