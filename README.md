# Mentorship-Program-Graduation-Analysis
Exploring what features influence students graduating from the EverythingData Africa  mentorship program. 

This notebook documents the process of analyzing participant data from a mentorship cohort to understand factors influencing graduation and to formulate recommendations for future cohorts.

Workflow Overview
The analysis followed these key steps:

Data Loading and Initial Inspection:

The mentorship program data was loaded into a pandas DataFrame.
Initial inspection of the data was performed using df.head(), df.info(), and df.shape to understand the structure, data types, and dimensions.
Data Cleaning and Preparation:

Checked for missing values (df.isna().sum()) and duplicate rows (df.duplicated().sum()). No missing values or duplicates were found.
Renamed columns for clarity and ease of use.
Cleaned and standardized values in the 'skill_level' column.
Converted the 'study_hours_per_week' column to a numerical representation ('study_hours_numeric') for potential quantitative analysis.


Exploratory Data Analysis (EDA):

Examined the distribution of categorical variables using value counts and countplots.
Visualized the relationship between categorical variables and 'Graduated' status using countplots with 'Graduated' as a hue to understand potential associations.
Performed Chi-squared tests of independence to statistically assess the association between categorical features and 'Graduated' status.
Explored the relationship between the numerical 'aptitude_test_score' and 'Graduated' status using a box plot.



Feature Engineering:

Selected relevant features for predictive modeling, including 'years_of_experience', 'aptitude_test_score', and other categorical features.
Applied one-hot encoding to the categorical features to convert them into a numerical format suitable for machine learning models using ColumnTransformer and OneHotEncoder.
Split the preprocessed data into training and testing sets using train_test_split, ensuring stratification to maintain the proportion of the target variable.



Predictive Modeling:

Trained a Logistic Regression model on the prepared data.
Evaluated the Logistic Regression model's performance using accuracy, classification report (precision, recall, F1-score), and confusion matrix.
Trained a Random Forest Classifier model on the prepared data.
Evaluated the Random Forest model's performance using accuracy, classification report, and confusion matrix.
Analysis Summary and Recommendations:

Summarized the key findings from the EDA and statistical tests, highlighting the statistically significant association between 'years_of_experience' and graduation.
Discussed the challenges encountered in predictive modeling, particularly due to the small dataset size and class imbalance, which resulted in models unable to reliably predict the minority class.
Formulated actionable recommendations for improving future mentorship cohorts based on the insights gained from the data analysis, focusing on participant selection, support systems, and program structure.


Key Findings
'Years of experience' showed a statistically significant association with graduation.
The aptitude test score did not appear to be a strong individual predictor of graduation.
Predictive modeling was challenging with the current small dataset, and models were unable to effectively predict the 'Graduated' status.


Recommendations
Based on the analysis, recommendations include refining participant selection criteria to prioritize candidates with some prior experience, enhancing support systems for beginners, adapting program structure, and improving data collection for future analysis.

Conclusion
While the small dataset limited the ability to build a highly predictive model, the analysis provided valuable insights into factors associated with graduation, particularly the importance of prior experience. The recommendations aim to leverage these insights to improve future mentorship cohorts.
