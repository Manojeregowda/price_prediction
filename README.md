# Bengaluru House Price Prediction

## Overview  
This project predicts **house prices in Bengaluru** based on property features such as location, size, total square feet, and number of bathrooms. By applying data analysis, feature engineering, and machine learning regression techniques, the model aims to estimate property prices accurately.

## Dataset  
The dataset used is `bengaluru_house_prices.csv`, which includes the following columns:

| Column       | Description                                 |
|--------------|---------------------------------------------|
| `area_type`  | Type of property area (e.g., Super built-up, Plot) |
| `availability`| Property status (e.g., Ready to move, Immediate) |
| `location`   | Area or locality name                         |
| `size`       | Number of bedrooms (e.g., 2 BHK, 3 BHK)       |
| `total_sqft` | Total area in square feet                     |
| `bath`       | Number of bathrooms                           |
| `price`      | Property price (in lakhs)                     |

## Technologies Used  
- Python  
- NumPy & Pandas – for data manipulation  
- Matplotlib & Seaborn – for data visualization  
- Scikit-learn – for model building and evaluation  
- Jupyter Notebook – for development and experimentation  

## Project Workflow  
### 1. Data Cleaning  
- Handle missing and duplicate values.  
- Remove outliers and inconsistent entries.  
- Convert text columns (such as “2 BHK”) into numeric form.  

### 2. Feature Engineering  
- Extract the number of bedrooms (BHK) from the `size` column.  
- Simplify and group rare locations to avoid overfitting.  
- One-hot encode categorical features like `location`.  

### 3. Model Building  
- Split data into training and testing sets.  
- Train regression models including:  
  - Linear Regression  
  - Lasso Regression  
  - Decision Tree Regressor  
- Evaluate them using metrics such as R² score and cross-validation.  

### 4. Prediction Function  
A function is built that takes inputs such as:  
- Location  
- Total Square Feet  
- Number of Bathrooms  
- Number of Bedrooms (BHK)  
… and returns an estimated house price using the trained model.

## Key Insights  
- Property price generally increases with area, but growth flattens beyond a certain size.  
- Location is a major determinant of value.  
- Removing outliers and combining rare categories improve model performance significantly.  

## Results  
The Linear Regression model achieved an **R² score of approximately 0.85-0.90**, indicating a good level of predictive accuracy on unseen data. The model can provide reasonable price estimates given input features.

## How to Run the Project  
### 1. Clone the Repository  
```bash
git clone https://github.com/Manojeregowda/price_prediction.git
