# SGD-Regressor-for-Multivariate-Linear-Regression

## AIM:
To write a program to predict the price of the house and number of occupants in the house with SGD regressor.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Collect and preprocess the dataset.
2. Initialize the SGD Regressor model.
3. Train the model using training data.
4. Predict outputs and evaluate performance. 

## Program:
```
/*
Program to implement the multivariate linear regression model for predicting the price of the house and number of occupants in the house with SGD regressor.
#SGD-ex4
import pandas as pd
from sklearn.linear_model import SGDRegressor
from sklearn.preprocessing import StandardScaler

# Load dataset
data = pd.read_csv("house.csv")
#print(data.columns)
data.columns = data.columns.str.strip()
# Features (inputs)
X = data[['Size', 'Bedrooms']]

# Targets (outputs)
y_price = data['Price']
y_occ = data['Occupants']

# Scaling (important for SGD)
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

# Models
price_model = SGDRegressor(max_iter=1000, learning_rate='constant', eta0=0.01)
occ_model = SGDRegressor(max_iter=1000, learning_rate='constant', eta0=0.01)

# Train models
price_model.fit(X_scaled, y_price)
occ_model.fit(X_scaled, y_occ)

# Input
size = float(input("Enter house size: "))
bed = int(input("Enter number of bedrooms: "))

# Scale input
new_data = scaler.transform([[size, bed]])

# Prediction
pred_price = price_model.predict(new_data)
pred_occ = occ_model.predict(new_data)

print("Predicted Price:", pred_price[0])
print("Predicted Occupants:", round(pred_occ[0]))
Developed by: Ritika S
RegisterNumber:  212225220086
*/
```

## Output:
![multivariate linear regression model for predicting the price of the house and number of occupants in the house](sam.png)
<img width="940" height="858" alt="WhatsApp Image 2026-04-27 at 2 29 02 PM" src="https://github.com/user-attachments/assets/450e2fdf-03ea-49ee-afc1-94095e5d6119" />

## Result:
Thus the program to implement the multivariate linear regression model for predicting the price of the house and number of occupants in the house with SGD regressor is written and verified using python programming.
