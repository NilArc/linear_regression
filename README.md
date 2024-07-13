# Data Linear Regression Model (Salary Predition)

## Data Used

**Dataset**: dataset/ai_gen_data.csv

## Data Information

It includes 149 rows and three columns: Job, Experience, and Salary. The jobs were obtained using keywords like "Junior", "Senior", "Chief Technology Officer", and "Project Manager". Each job title has 37 instances.

## Problem Statement

The goal is to train a linear regression model to predict salaries based on job positions and work experience. This model will be used in a Flask web application to provide salary predictions. The model needs to be trained using the Job and Experience columns, saved in a pickle format, and then loaded into the Flask application.

## Method

A linear regression model will be trained using the dataset. After training and evaluating the model, it will be saved as a pickle file for use in the Flask application.

## Algorithm

The algorithm used is linear regression, a supervised machine learning technique that identifies a linear relationship between variables. In this case, it will find the relationship between job positions, work experience, and salary.

### Steps

**Train the Linear Model**:
   - Import dependencies.
   - Load the CSV file.
   - Convert job titles to nominal integer values.
   - Reshape the dataset.
   - Split the dataset into training and testing sets.
   - Train the model.
   - Evaluate the model.
   - Save the model as a pickle file.

## Evaluation

The model’s accuracy and precision will be evaluated using Analysis of Variance (ANOVA). Key metrics include coefficients and the R-squared value. 

## Data Preparation

The dataset was preprocessed as follows:
- **Job Titles**: Converted to nominal values (Junior = 1, Senior = 2, Chief Technology Officer = 3, Project Manager = 4).
- **Salary**: Reformatted from string to float.
- **Experience**: Filled null values with mean imputation.

## Results & Discussion

The scraping process successfully retrieved the necessary data but required transformation and cleaning:
- **Final Dataset**: 149 rows and 3 columns ("Job", "Experience", "Salary"). 
- **Model Training**: The dataset was further processed and then used to train the model.
- **Evaluation**:
  - **Coefficients**: Job = 31.22, Experience = 13.24. This indicates that higher job positions and more experience lead to higher salaries.
  - **R-squared value**: 0.0083, meaning that only 0.83% of the variance in the dependent variable (salary) can be predicted from the independent variables (job and experience). This suggests a weak linear relationship in the dataset.

### Conclusion

The linear regression model indicates that higher job positions and more work experience lead to higher salaries. However, the model's low R-squared value suggests that the relationship is weak. This model can still be used in the Flask application for demonstration purposes, but further refinement and additional features may be needed for more accurate predictions.