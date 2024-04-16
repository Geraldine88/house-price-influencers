# House Price Influencers

## Problem Statement
Real estate leasers often face challenges in identifying the most effective strategies to enhance the value of their properties, including homes, apartments, and villas. This project aims to analyze key property features that significantly influence market value. By identifying these critical features, leasers can make informed decisions on where to allocate resources to improve property quality and maximize profitability.


1. During basic EDA, many missing values were identified in a column/features.
2. The interpolate method was used to handle them, which takes the average of neighbouring values so as to avoid a lot of variation.
4. The distribution of your Sale Price was plotted.
5. There was a lot of cycling back, re-loading the clean data, , removing outliers, re-thinking approaches, refitting the model  and finding a better solution, refitting the model.

## EDA
- **Read the data dictionary.**
- Determined _what_ missing values mean from the dataframe.info() method.
- Figured out what each categorical value represents.
- Identify outliers.
- Identified least correlated columns with sale price

## Data Cleaning
- Decided how to impute null values using interpolate() method, in a efforts to avoid numerous variations.
- Decide how to handle outliers by using the z-score to identify and drop them.
- Manually assisgned low correlated values to SalePrice , assigning to a list and dropping them.
  
## Exploratory Visualizations
- Looking at distributions, that of SalePrice is right-skewed, so many houses had low house prices and few had the high ones.
- Looking at correlations, the most correlated to house prices are Overall Quality of the house.

## Pre-processing
- Used pandas get_dummies.
- Train/test split your dataset.
- Scaled the data using standard scaler.

## Modeling
- **Establish your baseline score.**
- Fitted logistic regression regression.
- Fitted ridge with default parameters.
- Went back and removed features that might be causing issues in the models.
- Tunned hyperparameters.
- **Identify a production model.** Ridge regression
- Refined and interpreted your production model.

## Inferential Visualizations
- Looked at how accurate the models were. 80%

## Business Recommendations
- Overall Quality seemed to add the most quality to home
- Low quality in square feet hurt the model the most
- The overall  quality is at the top, followed by Above ground living area in square feet, Second floor in square feet, House age, quality of the material on the exterior, exterior kitchen quality, Size of garage in car capacity, first floor in square feet and Screen porch area in square feet.

- Do you feel that this model will generalize to other cities? : There is room for improvement giving that the root mean square is till far from zero.
How could you revise your model to make it more universal OR what date would you need from another city to make a comparable model? The model is to be revised.

# Example Directory Structure
Here's how you might structure a project with multiple notebooks.

```
project-2
|__ code
|   |__ 01_EDA_and_Cleaning.ipynb   
|   |__ 02_Preprocessing_and_Feature_Engineering.ipynb   
|   |__ 03_Model_Benchmarks.ipynb
|   |__ 04_Model_Tuning.ipynb  
|   |__ 05_Production_Model_and_Insights.ipynb
|   |__ 06_Kaggle_Submissions.ipynb   
|__ data
|   |__ train.csv
|   |__ test.csv
|   |__ submission_lasso.csv
|   |__ submission_ridge.csv
|__ images
|   |__ coefficients.png
|   |__ neighborhoods.png
|   |__ predictions.png
|__ presentation.pdf
|__ README.md
```