# E-commerce---Users-of-a-C2C-fashion-store
## Context
There are a lot of unknowns when running an E-commerce store, even when you have analytics to guide your decisions. Users are an important factor in an e-commerce business. This is especially true in a C2C-oriented store, since they are both the suppliers (by uploading their products) AND the customers (by purchasing other user's articles).<br>
There are a lot of unknowns when running an E-commerce store, even when you have analytics to guide your decisions. Users are an important factor in an e-commerce business. This is especially true in a C2C-oriented store, since they are both the suppliers (by uploading their products) AND the customers (by purchasing other user's articles).

Introduction to the Project
This project focuses on analyzing and predicting the buying behavior of users in a consumer-to-consumer (C2C) fashion e-commerce platform. In C2C marketplaces, users act as both sellers, listing their fashion items, and buyers, purchasing items from others. Understanding these dynamics is critical for enhancing user engagement, optimizing marketing strategies, and personalizing experiences.

The goal of this project is to predict the likelihood of a user making a purchase, based on features such as user demographics, browsing patterns, and activity data. By leveraging this dataset, which encapsulates user behavior on the platform, the analysis aims to uncover the key drivers of purchase decisions and provide actionable insights to support business growth and user satisfaction.

Goal of the Project
The goal of this project is to predict the likelihood of a user making a purchase on a C2C fashion e-commerce platform, utilizing various user attributes. By understanding the factors influencing purchase behavior, the analysis aims to provide actionable insights that help optimize user engagement, personalize experiences, and enhance marketing strategies. The predictive model will enable the platform to identify and target potential buyers more effectively, fostering growth and improving overall user satisfaction.

Main Objective
The primary objective of this project is to develop a predictive model that classifies users based on their likelihood to make a purchase on the platform. Achieving this goal involves the following key steps:
Data Exploration: Analyze and understand the dataset’s structure, relationships, and patterns to gain insights into user behavior.
Data Preprocessing: Clean and prepare the data for modeling, addressing missing values, encoding categorical variables, and scaling features as needed.
Feature Engineering: Create new features or select the most relevant ones to enhance model accuracy and interpretability.
Model Building: Build and evaluate classification models to predict the probability of users making a purchase.
Performance Evaluation: Use key metrics to assess model performance and ensure reliable, actionable predictions.

Description
Explore user behaviour of a successful website to get benchmarks. Get actionable insights about online sales and clients

Describing user data from a C2C
identifierHash: A unique identifier for each user (integer).
type: The type of account (e.g., "user").
country: The country associated with the user.
language: The language preference of the user.
socialNbFollowers: Number of followers the user has on social media.
socialNbFollows: Number of accounts the user follows on social media.
socialProductsLiked: Number of products the user liked on social media.
productsListed: Number of products the user has listed for sale.
productsSold: Number of products the user has sold.
productsPassRate: Percentage of sold products meeting certain criteria (float).
productsWished: Number of products the user has wished for.
productsBought: Number of products the user has purchased.
gender: Gender of the user (e.g., "male", "female").
civilityGenderId: Numeric ID corresponding to gender.
civilityTitle: Title indicating the user's civility (e.g., "mr", "mrs").
hasAnyApp: Boolean indicating if the user has any app (True/False).
hasAndroidApp: Boolean indicating if the user uses the Android app.
hasIosApp: Boolean indicating if the user uses the iOS app.
hasProfilePicture: Boolean indicating if the user has a profile picture.
daysSinceLastLogin: Days since the user last logged in.
seniority: Total days of the user's membership.
seniorityAsMonths: Seniority of the user in months (float).
seniorityAsYears: Seniority of the user in years (float).
countryCode: The ISO country code for the user's country.

Data Story
The dataset captures various aspects of user interaction with a C2C fashion e-commerce platform. It likely includes features such as the number of sessions, time spent on the platform, product views, wishlist activity, and demographic details (e.g., age, gender, location). These attributes provide valuable insights into user behavior and help characterize the typical C2C fashion store user.

The target variable, productsBought, indicates whether a user has completed a purchase. The challenge lies in identifying the features that most strongly influence this outcome. By analyzing these variables, we aim to uncover patterns and trends that signal a high likelihood of purchase. For instance, frequent platform engagement, high interaction with specific product categories, or active use of platform features like wishlisting may correlate with purchase behavior. This analysis will help improve the understanding of user behavior, enabling targeted interventions to boost conversions.

Content
The dataset was sourced from a thriving online C2C fashion store with over 9 million registered users. Initially launched in Europe in 2009, the platform has since expanded its operations globally. The dataset encapsulates user activity and behavior on the platform, providing a rich foundation for analyzing and predicting purchase likelihood.

Summary
Foreword
This users dataset is a subset of a much larger dataset, which includes additional related data such as product listings by sellers, comments on listed products, and more. This preview focuses on user behavior and interactions, serving as a foundation for understanding and predicting purchasing patterns on the platform.

The values in the columns are mostly near zero or equal to zero, which is why the outliers appear in this range. If we remove all outliers using the IQR method, the descriptive statistics of the dataset, such as the mean, standard deviation, and maximum values, will also approach zero. Therefore, the observed outliers are values close to or equal to zero in the columns.

Conclusion for the Project
The goal of the project was to predict the number of products bought by users based on their behavioral, social, and demographic features. Several regression models were evaluated to determine the most accurate approach for this task. Here's a summary of the findings and insights:

Best Model: Stacking Regressor
The Stacking Regressor outperformed all other models, achieving:
The lowest error metrics: MSE (0.00959), RMSE (0.09793), MAE (0.03820).
The highest R² score (0.296), explaining approximately 29.63% of the variability in the target variable.
This demonstrates the power of combining multiple base models to enhance predictive accuracy and generalization.

Individual Model Performance
Linear Regression:
Achieved reasonable accuracy with an R² score of 0.240 and relatively low errors, making it a strong baseline model.
Decision Tree:
Performed inconsistently with high variance, as evidenced by a cross-validated R² of 0.240 but occasional overfitting.
Random Forest:
Showed strong predictive performance with an R² of 0.284 and consistent accuracy across the test set.
Gradient Boosting:
Marginally outperformed Random Forest with an R² of 0.295 and demonstrated robustness.
Support Vector Regressor:
Struggled significantly with poor performance, evidenced by a negative R² score and higher error metrics.

Insights from Feature Engineering
Feature Importance: Social interaction features like socialNbFollowers, socialProductsLiked, and productsListed showed a strong correlation with the target variable, making them key predictors.
Dimensionality Reduction: Applying PCA reduced the feature set to 13 principal components while retaining 95% of the variance, optimizing model performance.
Scaling: Standardizing features improved the stability and accuracy of the machine learning models.

Final Remark
The Stacking Regressor demonstrated the best balance between accuracy and reliability, making it the recommended model for predicting product purchases. These insights can guide data-driven decisions to improve user engagement and boost revenue.
