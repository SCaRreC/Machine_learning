🏡 Machine Learning on Airbnb Listings

This project explores machine learning techniques to predict Airbnb listing prices using a dataset of property features and host information.

📊 Objective

The goal was to build a predictive model that estimates the nightly price of an Airbnb listing. I focused heavily on the exploratory data analysis (EDA) and feature engineering stages, aiming to build a clean and informative dataset before modeling.

🔍 Dataset

The dataset contains listing attributes including:

Location (longitude, city)
Property details (room type, number of bathrooms, bedrooms, beds)
Pricing factors (cleaning fee, security deposit)
Availability and guest limits
Amenities (count, luxury amenity count)
Categorical features like cancellation policy and room type
🧪 Model Used

During most of the time and the different tries at it, a Lasso regression model was trained and tested on the processed data. Unfortunately, despite a meticulous EDA process, the model performance was underwhelming.
[see file: Practica_Machine_Learning](./Practica_Machine_Learning.ipynb)
Then I decided to try other models quickly (Random Forest and Decision Tree), and tried with a different aproach to the inital data (one of the many tries). These last ones performed greatly compared to the Lasso model.
[see file: Other Models](./Practica_Machine_Learning_Other_Models.ipynb)

🔢 Modeling and Results

Lasso Regression
Lasso regression was used as an initial model due to its ability to perform automatic feature selection. However, it did not perform well, likely due to its inability to capture non-linear interactions between variables.
The Lasso model automatically shrank many coefficients to zero. 
Feature coefficients showed that many variables were pushed to zero, indicating strong regularization but poor overall model fit.

🔍 Tree-Based Models
I later implemented Decision Tree and Random Forest regressors. These models performed significantly better on both train and test sets. The improvement is likely due to their ability to capture non-linear relationships and interactions between variables—something Lasso regression cannot do.

🧠 Lessons Learned

The limited performance is likely due to an overemphasis on EDA and variable engineering, with not enough experimentation on:

Alternative models (e.g. Random Forest, Gradient Boosting)
Hyperparameter tuning
Pipeline design and cross-validation strategies
This has been a valuable learning experience in balancing preparation and iteration in the machine learning workflow.

⚙️ Next Steps

Tune hyperparameters of tree-based models
Explore ensemble methods (e.g., Gradient Boosting, XGBoost)
Evaluate feature importance and SHAP values for interpretability
Build a lightweight dashboard or report

###Conclusion

This project was a valuable exercise in end-to-end machine learning, from EDA to model comparison. While Lasso regression offered a simple and interpretable baseline, tree-based models clearly outperformed it due to their flexibility in modeling complex relationships.
