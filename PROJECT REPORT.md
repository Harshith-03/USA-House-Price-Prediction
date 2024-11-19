# **Project Report: House Price Prediction using Machine Learning**

This project explores the relationship between various features of homes in the USA and their prices. Using a Kaggle dataset, I aimed to build an introductory machine-learning model to predict house prices based on features such as square footage, the number of bedrooms, bathrooms, city, and more.

---

## **1. Feature Importance**
The feature importance plot (shown in the repository) highlights which features had the greatest influence on the predictions made by the **tuned Random Forest model**.

![Feature Importance Plot](https://github.com/user-attachments/assets/ddbbb1f0-345f-4cd5-997f-6317dd21ccff)


### **Key Insights**
- **Living Area (`sqft_living`)**: The most important predictor of house prices, with a feature importance of ~20%.
- **Above Ground Square Footage (`sqft_above`)**: Another significant feature, indicating that the overall size of the property above ground greatly impacts prices.
- **Number of Bathrooms and Bedrooms**: These also play a substantial role, though to a lesser extent than square footage.
- **City**: The city where the house is located influences pricing, likely due to regional economic factors, desirability, and amenities.
- Features such as **waterfront view**, **year built**, and specific cities (like Seattle) also contributed but were less influential.

### **Recommendations**
This analysis suggests focusing on features like square footage and the number of bathrooms when appraising or predicting house prices.

---

## **2. Actual vs. Predicted Prices**
The scatter plot comparing **Actual Prices** vs. **Predicted Prices** gives us a visual representation of the model's performance. 

![Actual vs. Predicted Prices](https://github.com/user-attachments/assets/9e305725-6ded-4ad5-b4f2-4d546f3642b8)


### **Key Observations**
- **Trend Alignment**: The red dashed line represents a perfect prediction scenario (i.e., where actual prices equal predicted prices). Many points cluster around this line, indicating the model captured the overall trend well.
- **Outliers**: A few outliers deviate significantly from the line, suggesting some houses had prices that were harder to predict accurately, due to external factors.
- **Correlation**: The model performs best for mid-range prices, with some variance for extremely high or low prices.

### **Conclusion**
While the tuned Random Forest model performs better than the other two, further fine-tuning or more data preprocessing may help reduce the variance and handle outliers better.

---

## **3. Residual Plot**
The residual plot provides a detailed look at the errors made by the model (difference between actual and predicted values).


![Residual Plot](https://github.com/user-attachments/assets/41afca0d-4708-447f-a51a-a416192f6cc4)


### **Observations**
- **Uniform Residual Distribution**: Residuals are mostly centered around 0, which indicates the model has no significant bias in underestimating or overestimating prices.
- **Spread of Residuals**: The spread of residuals increases slightly as the predicted price grows, which means the model performs less reliably for higher-priced homes.
- **Random Scatter**: The lack of a clear pattern in the residuals confirms the model does not have systematic errors.

### **Recommendations**
Improving the handling of higher-priced homes may involve:
1. Log-transforming prices to normalize their distribution further.
2. Incorporating additional features related to luxury properties, such as proximity to landmarks or income levels in the region.

---

## **Model Performance Metrics**
The performance of the models is summarized below:

| **Model**                 | **R² Score** | **RMSE** |
|---------------------------|--------------|----------|
| Baseline Linear Regression | 0.48         | 0.40     |
| Baseline Random Forest     | 0.35         | 0.45     |
| **Tuned Random Forest**    | **0.51**     | **0.39** |

### **Key Takeaways**
- The **tuned Random Forest model** outperformed the Linear Regression model in both R² score and RMSE, demonstrating its superior ability to capture non-linear relationships in the data.
- An R² score of 0.51 indicates the model explains approximately 51% of the variance in house prices, which is reasonable for a dataset of this nature.

---

## **Limitations and Future Improvements**
### **Limitations**
1. **Feature Selection**: Some features, such as city names, may benefit from better encoding (e.g., grouping cities into tiers based on average house prices).
2. **Model Generalizability**: The model's performance may not generalize well to unseen data from other regions or time periods without retraining.
3. **Outliers**: Extreme house prices remain challenging for the model to predict accurately.

### **Future Improvements**
1. **Data Enrichment**: Include additional features such as average neighborhood income, crime rates, proximity to schools, or parks for better predictions.
2. **Model Fine-Tuning**: Experiment with other models, such as Gradient Boosting Machines (e.g., XGBoost or LightGBM), for potentially better performance.
3. **Advanced Hyperparameter Tuning**: Use methods like Bayesian optimization instead of RandomizedSearchCV for more precise hyperparameter tuning.
4. **Handling High Prices**: Explore ensemble models that treat high-priced houses as a separate class for more accurate predictions.

---

## **Final Remarks**
This project successfully built a machine learning pipeline for predicting house prices, demonstrating the importance of feature engineering, model evaluation, and hyperparameter tuning. The insights from this project can be used as a foundation for further real estate analytics and forecasting.
