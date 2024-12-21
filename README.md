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




