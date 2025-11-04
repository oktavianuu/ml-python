# Topics
- Regression
- Model Evaluation
- Model Evaluation; Overfitting and Underfitting
- Understanding Different Evaluation Model
- Simple Linear Regression

## Regression
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
\hat{y} = \theta_0 + \theta_1 + {x}_1
$$
__Explanation__:
$\theta_0$ and $\theta_1$ are the parameters of the line we must adjust. Also called the coefficients of linear equations.
$\theta_1$ = known as slope or gradient of the fitting line
$\theta_0$ = known as intercept

In other words, we can say that $\hat{y}$ being a function of $x_1$. Moreover, we must calculate the value of the slope and intercept in order to find the best fitted line. This line later will be used to predict the outcome of the incoming $x_1$ data points. 