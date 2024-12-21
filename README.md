# Simple_Linear_Regression
> Regression models (both linear and non-linear) are used for predicting a real value, like salary for example.Regression is a statistical and machine learning technique used to model and analyze the relationships between variables.
>
> It is primarily used for predicting a continuous dependent variable based on one or more independent variables. Regression helps in understanding how the dependent variable changes when one or more independent variables are varied.
> If your independent variable is time, then you are forecasting future values, otherwise your model is predicting present but unknown values. Types of Regression iclude:
> + Simple Linear Regression
> + Simple Linear Regression
> + Multiple Linear Regression
> + Polynomial Regression
> + Support Vector for Regression (SVR)
> + Decision Tree Regression
> + Random Forest Regression

## Simple Linear Regression
Models a linear relationship between the dependent and independent variables.
### Formula:  𝑦 =b0 + b1𝑥1 _where y is the dependent variable, X1 is the independent variable, b0 is the y-intercept (constant) and b1 is the slope coefficient_

### Example: Assumming we are Predicting house prices based on square footage, the fomula will look like this:
+ house_prices ($) = b0 +b1Xsquare_footage(square_meter)
+ Assuming the b0 is 5000 dollar, b1 = 1000[$/square_meter]
+ If plotted, the resultant graph will be linear
+ [View Sample Graph Here](https://colab.research.google.com/drive/1FokxwBjImCwSqQj7p90Z7jhpm_mo2-me#scrollTo=AJG-Qn367bEf)

```python
import numpy as np
import matplotlib.pyplot as plt

# Constants for the regression line
b0 = 10000  # Intercept (base price in dollars)
b1 = 200    # Price increase per square footage

# Data: square footage
square_footage = np.linspace(500, 4000, 100)  # Range of square footage values
house_prices = b0 + b1 * square_footage       # Calculate house prices

# Plot the regression line
plt.figure(figsize=(8, 6))
plt.plot(square_footage, house_prices, label='House Prices = b0 + b1 * Square Footage', color='blue')
plt.scatter([1000, 2000, 3000], [b0 + b1 * 1000, b0 + b1 * 2000, b0 + b1 * 3000], color='red', label='Sample Data Points')
plt.title('House Prices vs. Square Footage', fontsize=14)
plt.xlabel('Square Footage', fontsize=12)
plt.ylabel('House Prices ($)', fontsize=12)
plt.legend()
plt.grid(alpha=0.4)
plt.tight_layout()

# Show the plot
plt.show()

```

## Ordinary Least Squares Regression
> ```python
> Ordinary Least Squares (OLS) Regression is a fundamental method for estimating the parameters of a linear regression model.
> It minimizes the sum of the squared differences (residuals) between the observed dependent variable and the predicted values 
> ```
### How do we know which of the slope line is the best. Which one fit better, this is the reason for OLS.
_The general form of a linear regression equation is:_
$y=β 
0
​
 +β 
1
​
 x 
1
​
 +β 
2
​
 x 
2
​
 +…+β 
p
​
 x 
p
​
 +ϵ$
 + y: Dependent Variable
 + xi : Independent Variables
 + βi : Regression coefficients
 + ϵ: Error term (residual)
 __OLS Objective__
> The goal of OLS is to minimize the sum of squared residuals:
### Formula: 
$SSE= 
i=1
∑
n(yi − y^i)2$

Where:
+ 𝑦𝑖: Observed values
+ y^i : Predicted values $(𝑦^𝑖 (predValue) =𝛽0+𝛽1𝑥𝑖)$

​## Summary
> In summary, Ordinary Least Squares (OLS) regression is obtained by solving for the coefficients (𝛽) that minimize the sum of squared errors (SSE) between the observed values (𝑦) and the predicted values (𝑦^) of the model.
>
> The coefficients (𝛽) describe the linear relationship between the independent variables (𝑋) and the dependent variable (𝑦).






