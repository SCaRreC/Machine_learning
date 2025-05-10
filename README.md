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

A Lasso regression model was trained and tested on the processed data. Unfortunately, despite a meticulous EDA process, the model performance was underwhelming.

🔢 Performance Metrics
Metric	Train Set	Test Set
MSE (Mean Squared Error)	0.208	0.234
RMSE (Root Mean Squared Error)	0.456	0.484
🔍 Lasso Coefficients (Partial)
The Lasso model automatically shrank many coefficients to zero. Selected non-zero coefficients:

Bathrooms: 0.234
Beds: 0.015
Amenity count: 0.064
Has security deposit: 0.061
Room Type_Shared room: -0.154
Most other variables (including location and city) had coefficients of zero.

🧠 Lessons Learned

The limited performance is likely due to an overemphasis on EDA and variable engineering, with not enough experimentation on:

Alternative models (e.g. Random Forest, Gradient Boosting)
Hyperparameter tuning
Feature selection and dimensionality reduction
Pipeline design and cross-validation strategies
This has been a valuable learning experience in balancing preparation and iteration in the machine learning workflow.

⚙️ Next Steps

To improve this project, future work will focus on:

Implementing multiple model types and comparing performance
Automating feature selection and transformations
Applying cross-validation and grid search
Revisiting feature encoding strategies (e.g. target encoding, interactions)
