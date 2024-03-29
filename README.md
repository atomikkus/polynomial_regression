## Polynomial Regression

Polynomial regression is a type of regression analysis used to model the relationship between the independent variable `x` and the dependent variable `y` as an nth-degree polynomial. Unlike simple linear regression, which fits a straight line to the data, polynomial regression can capture more complex relationships by introducing polynomial terms.

In polynomial regression, the model equation takes the form:

$$ y = \beta_0 + \beta_1x + \beta_2x^2 + ... + \beta_nx^n + \varepsilon $$

where:
- $y$ is the dependent variable,
- $x$ is the independent variable,
- $\beta_0, \beta_1, ..., \beta_n$ are the coefficients,
- $n$ is the degree of the polynomial,
- $\varepsilon$ represents the error term.

By including higher-degree polynomial terms, polynomial regression can better fit nonlinear patterns in the data. However, selecting an appropriate degree for the polynomial is crucial to prevent overfitting or underfitting. Polynomial regression is a powerful tool in predictive modeling when relationships between variables are not linear and require a more flexible approach to capture the underlying patterns in the data.
![image](https://github.com/atomikkus/polynomial_regression/assets/87168509/fe063f23-a5b9-4a1e-93f3-556d5b459583)

## Hyperparameter Tuning: Regularization

Polynomial Regression models can tend to overfit, when increase their degree in return for a better R2
![image](https://github.com/atomikkus/polynomial_regression/assets/87168509/aea8a88a-26d7-457f-8695-46e23c3cbe4d)

You can either decrease the degree and sacrifice the higher performance and adjust the weights learned globally, that's where Regularisation helps:

### Ridge Regression

Ridge regression is a regularization technique used to prevent overfitting in linear regression models by adding a penalty term to the cost function. It is particularly useful when dealing with multicollinearity, where predictor variables are highly correlated. 

### Key Points:
- **Objective**: Minimize the sum of squared residuals along with a penalty term that is the L2 norm of the coefficients multiplied by a regularization parameter (alpha).
- **Regularization**: Helps in shrinking the coefficients towards zero, reducing model complexity and variance.
- **Bias-Variance Tradeoff**: Ridge regression helps in finding a balance between bias and variance by penalizing large coefficients.
- **Parameter Tuning**: The regularization parameter (alpha) controls the strength of regularization, with higher values leading to more shrinkage.
- **Feature Selection**: Ridge regression does not perform feature selection but can shrink coefficients close to zero, making it useful for models with many predictors.


### Mathematical Notations:

In Ridge regression, the cost function is modified by adding a penalty term that includes the squared magnitude of the coefficients:

The Ridge regression cost function is defined as:

$$ J(\theta) = \sum_{i=1}^{m} (y^{(i)} - h_{\theta}(x^{(i)}))^2 + \lambda \sum_{j=1}^{n} \theta_j^2 $$

$$ \lambda \sum_{j=1}^{n} \theta_j^2 $$

Higher the regularization, lesser the weights disbursed to the model, hence working to optimise the model from overfitting to optimal fit

### Lasso Regression

Lasso regression, short for Least Absolute Shrinkage and Selection Operator, is another regularization technique used in linear regression to prevent overfitting and perform feature selection by adding a penalty term to the cost function. It is particularly effective when dealing with high-dimensional datasets and selecting important features.

### Key Points:
- **Objective**: Minimize the sum of squared residuals along with a penalty term that is the L1 norm of the coefficients multiplied by a regularization parameter (alpha).
- **Regularization**: Lasso regression shrinks the coefficients towards zero and encourages sparsity by setting some coefficients to exactly zero, effectively performing feature selection.
- **Bias-Variance Tradeoff**: Lasso regression helps in balancing bias and variance by penalizing and shrinking coefficients, leading to a simpler model.
- **Parameter Tuning**: The regularization parameter (alpha) controls the strength of regularization, with higher values promoting more coefficients to be set to zero.
- **Feature Selection**: Lasso regression automatically selects important features by setting less important ones to zero, aiding in model interpretability and efficiency.

### Mathematical Notations:

In Lasso regression, the cost function is modified by adding a penalty term that includes the absolute sum of the coefficients:

The Lasso regression cost function is defined as:

$$ J(\theta) = \sum_{i=1}^{m} (y^{(i)} - h_{\theta}(x^{(i)}))^2 + \lambda \sum_{j=1}^{n} |\theta_j| $$

$$ \lambda \sum_{j=1}^{n} |\theta_j| $$

A higher regularization parameter leads to more coefficients being shrunk to zero, facilitating feature selection and reducing model complexity.

Citations:

[1] https://www.geeksforgeeks.org/python-implementation-of-polynomial-regression/

[2] https://www.javatpoint.com/machine-learning-polynomial-regression

[3] https://stats.stackexchange.com/questions/92065/why-is-polynomial-regression-considered-a-special-case-of-multiple-linear-regres

[4] https://towardsdatascience.com/introduction-to-linear-regression-and-polynomial-regression-f8adc96f31cb

[5] https://en.wikipedia.org/wiki/Polynomial_regression
