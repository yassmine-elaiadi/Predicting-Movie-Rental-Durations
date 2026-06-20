# Movie Rental Duration Prediction

## Project Overview

This project aims to predict how long a customer will keep a rented movie before returning it. Understanding rental duration can help a movie rental company improve inventory management, customer insights, and operational planning.

The project follows a complete machine learning workflow including data cleaning, feature engineering, exploratory data analysis (EDA), feature selection, model training, and model evaluation.

## Business Problem

A movie rental company wants to predict rental duration for each rental transaction.

By accurately predicting rental duration, the company can:

* Improve inventory planning
* Better understand customer rental behavior
* Support business decision-making
* Optimize rental operations

The target variable is:

**rental_length_days** = number of days between rental and return.

## Dataset

The dataset contains rental transaction information, including:

* Rental dates
* Return dates
* Rental rates
* Movie length
* Replacement cost
* Special movie features
* Movie rating categories

## Data Preparation

Several preprocessing and feature engineering steps were performed:

### Date Conversion

The rental and return dates were converted to datetime format.

### Target Variable Creation

Rental duration was calculated as:

rental_length_days = return_date - rental_date

### Feature Engineering

Two binary features were created from the special_features column:

* deleted_scenes
* behind_the_scenes

### Data Cleaning

* Removed unnecessary columns after feature extraction
* Prepared data for machine learning modeling

## Exploratory Data Analysis

### Rental Duration Distribution

Rental durations were relatively evenly distributed between 1 and 8 days, with fewer rentals at the shortest and longest durations.

### Rental Duration by Movie Rating

Average rental duration was very similar across all movie rating categories. This suggests that movie rating is not a major driver of rental duration.

### Rental Duration by Rental Rate

Movies with rental rates of $0.99, $2.99, and $4.99 all had nearly identical average rental durations. Rental price alone does not appear to influence rental duration.

### Movie Length vs Rental Duration

A scatter plot and correlation analysis were used to examine the relationship between movie length and rental duration.

The correlation coefficient was approximately:

-0.0045

This indicates virtually no relationship between movie length and rental duration.

## Modeling Approach

### Feature Selection

Lasso Regression was used for automatic feature selection.

Only features with non-zero coefficients were retained for the final model.

### Final Model

A Linear Regression model was trained using the selected features.

## Model Evaluation

The model was evaluated using Mean Squared Error (MSE).

MSE: [INSERT YOUR RESULT]

RMSE: [INSERT YOUR RESULT]

## Key Findings

* Movie rating has little impact on rental duration.
* Rental rate has little impact on rental duration.
* Movie length has virtually no relationship with rental duration.
* Predicting rental duration requires combining multiple features rather than relying on a single variable.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn

## Future Improvements

Potential improvements include:

* Testing Random Forest Regression
* Testing Gradient Boosting models
* Hyperparameter tuning
* Additional feature engineering
* Cross-validation
* More advanced model comparison

## Author

Yassmine Elaiadi
Master's Student in Data Science
Associate Data Scientist (DataCamp)
