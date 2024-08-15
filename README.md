# Big-Mart-Sales-Prediction-using-Machine-Learning-XGBoost-and-Random-Forest-Regressor-

This project aims to predict the sales of products across various outlets of Big Mart using machine learning techniques. The goal is to develop a model that can accurately forecast sales based on product attributes and outlet characteristics.

**Dataset**

The dataset consists of the following columns:

**Item_Identifier:** Unique identifier for each item

**Item_Weight:** Weight of the item]

**Item_Fat_Content:** Fat content of the item (low fat, regular, etc.)

**Item_Visibility:** Percentage of total display area allocated to this item in the store

**Item_Type:** Category of the item

**Item_MRP**: Maximum Retail Price (list price) of the item

**Outlet_Identifier:** Unique identifier for each outlet

**Outlet_Establishment_Year:** Year the outlet was established

**Outlet_Size:** Size of the outlet (small, medium, large)

**Outlet_Location_Type:** Type of city in which the outlet is located

**Outlet_Type:** Type of outlet (grocery store, supermarket, etc.)

**Item_Outlet_Sales:** Sales of the item in the particular outlet (target variable)

**Steps Involved**

**1. Data Preprocessing**

Checked for Null Values: The dataset had missing values, which were initially handled using mode and mean imputation. However, this led to biased data.

Handled Missing Data with Linear Interpolation: To avoid bias, the linear interpolation method was used for missing values, which provided a more accurate reflection of the data.

Created New Feature: A new column, outlet_age, was created to represent the age of the outlet.

**2. Feature Engineering**

Handled Categorical Variables: Used Ordinal Encoder to convert categorical columns into numerical values.

Feature and Target Separation: Split the dataset into features (X) and target (y) where y contains the target variable (Item_Outlet_Sales).

**3. Model Training**

**Trained the following models:**

**Random Forest Regressor**

**XGBoost Regressor**

**Model Comparison:** XGBoost Regressor outperformed Random Forest Regressor in terms of accuracy and prediction quality.

**4. Feature Selection**

Feature Importance: Identified the importance of each feature using XGBoost.

Feature Reduction: Removed the least important features, including:
Item_Visibility_interpolate
Item_Weight_interpolate
Item_Type
Outlet_Location_Type
Item_Identifier
Item_Fat_Content
The remaining features were used to create a final dataset for model training.

**5. Prediction and Evaluation**

**Final Model:** Retrained the XGBoost Regressor on the refined dataset.

**Prediction on Unseen Data:** The final model was tested on unseen data, and the sales values were predicted.

**Error Analysis:** Calculated the Mean Squared Error (MSE) for model evaluation.

**Sales Prediction Range:** The sales value was estimated within a range calculated as pred ± 714.42.

**Conclusion**

The XGBoost Regressor proved to be the most effective model for predicting Big Mart sales, outperforming the Random Forest Regressor. The use of linear interpolation for handling missing values and the selection of important features contributed significantly to the model’s accuracy. The final predictive system can estimate sales within a specified range, making it a reliable tool for forecasting Big Mart sales.
