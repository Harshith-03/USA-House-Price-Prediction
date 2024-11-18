# **USA House Price Prediction**

This project predicts house prices in the USA using a machine learning pipeline. It includes exploratory data analysis, data preprocessing, model training, hyperparameter tuning, and evaluation.

---

## **Project Overview**

The goal of this project was to create a machine learning model to predict house prices accurately based on various features. We used a Kaggle dataset, explored the data, and trained different models. The best-performing model was a tuned Random Forest Regressor.

---

## **Table of Contents**

1. [Dataset](#dataset)  
2. [Features](#features)  
3. [Workflow](#workflow)  
4. [Results](#results)  
5. [Installation](#installation)  
6. [File Structure](#file-structure)  
7. [Contributing](#contributing)  
8. [License](#license)  

---

## **Dataset**

The dataset was obtained from Kaggle.

- **Title**: *USA House Prices*  
- **Author**: Fırat Özcan  
- **Link**: [Kaggle Dataset](https://www.kaggle.com/datasets/fratzcan/usa-house-prices) 

---

## **Features**

Key features used for prediction:  

- **Numerical Features**:  
  - `sqft_living`, `sqft_above`, `bathrooms`, `bedrooms`, `sqft_lot`, etc.  

- **Categorical Features**:  
  - `city`, `waterfront`, `view`, etc.  

- **Temporal Features**:  
  - `year`, `month` (extracted from the `date` column).  

---

## **Workflow**

1. **Exploratory Data Analysis (EDA)**  
   - Data cleaning and visualization to understand key patterns.  

2. **Data Preprocessing**  
   - Handling missing values.  
   - Encoding categorical variables using one-hot encoding.  
   - Normalizing numerical variables.  

3. **Model Training and Evaluation**  
   - Models used: Linear Regression, Random Forest.  
   - Evaluated using \(R^2\) score and RMSE.  

4. **Hyperparameter Tuning**  
   - Optimized the Random Forest model using GridSearchCV.  

5. **Visualization**  
   - Feature importance plot.  
   - Actual vs. Predicted plot.  
   - Residual analysis.  

---

## **Results**

The **tuned Random Forest Regressor** achieved the best performance:  

- \(R^2\): 0.51  
- RMSE: 0.39  

### **Key Insights**

- Features like `sqft_living`, `bathrooms`, and `sqft_above` were the most influential predictors.  
- Residual analysis revealed some non-uniformity, suggesting potential for further improvement.

---

## **Installation**

1. Clone this repository:  
   ```bash
   git clone https://github.com/your-username/usa-house-price-prediction.git
   cd usa-house-price-prediction

