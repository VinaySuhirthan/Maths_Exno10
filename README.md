# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step 1:  
Import the required libraries: `pandas` for data manipulation and `linear_model` from `sklearn` for regression.  

### Step 2:  
Load the dataset using `pd.read_csv()` and store it in a DataFrame.

### Step 3:  
Separate the features (independent variables) and the target (dependent variable):  
- Assign the relevant columns to `X` (features).  
- Assign the target column to `y` (output).  

### Step 4:  
Create a linear regression model using `linear_model.LinearRegression()` and fit it to the data using `regr.fit(X, y)`.  

### Step 5:  
Print the regression coefficients (`regr.coef_`) and intercept (`regr.intercept_`).  

### Step 6:  
Use the trained model to make predictions using `regr.predict()` with the given input values.  

### Step 7:  
Display the predicted output.

## Program:
```python
# Developed by: K S Vinay Suhirthan
# Reg no: 24901151

import pandas as pd
from sklearn import linear_model

df = pd.read_csv("C:\\Users\\ksvin\\Downloads\\carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']

regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:',regr.intercept_)

predictedCO2 = regr.predict([[3300, 1300]])
print('Predicted CO2 for the corresponding weight and volume',predictedCO2)
```
## Output:

![output10](https://github.com/user-attachments/assets/adbd961e-89b9-490b-8e36-029ed548c0d2)


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
