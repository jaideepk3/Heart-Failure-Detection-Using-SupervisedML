# Heart Failure Detection Using Supervised ML

This project aims to design a supervised machine learning model to classify or predict whether a patient is prone to heart failure depending on multiple attributes. It is a binary classification problem with multiple numerical and categorical features.

## Dataset

The dataset was created by combining five different heart disease datasets from the UCI Machine Learning Repository. The dataset has 918 observations and 12 features, including the target variable `HeartDisease`. The features are:

- `Age`: age of the patient in years
- `Sex`: sex of the patient (M: Male, F: Female)
- `ChestPainType`: chest pain type (TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic)
- `RestingBP`: resting blood pressure in mm Hg
- `Cholesterol`: serum cholesterol in mm/dl
- `FastingBS`: fasting blood sugar (1: if FastingBS > 120 mg/dl, 0: otherwise)
- `RestingECG`: resting electrocardiogram results (Normal: Normal, ST: having ST-T wave abnormality, LVH: showing probable or definite left ventricular hypertrophy)
- `MaxHR`: maximum heart rate achieved
- `ExerciseAngina`: exercise-induced angina (Y: Yes, N: No)
- `Oldpeak`: ST depression induced by exercise relative to rest
- `ST_Slope`: the slope of the peak exercise ST segment (Up: upsloping, Flat: flat, Down: downsloping)
- `HeartDisease`: output class (1: heart disease, 0: Normal)

## Exploratory Data Analysis

The dataset was explored using various statistical and graphical methods to understand the distribution, correlation, and relationship of the features with the target variable. Some of the key findings are:

- The dataset is imbalanced with more heart disease cases than normal cases.
- The male population has more heart disease cases than the female population.
- The ASY type of chest pain, the flat ST slope, and the exercise-induced angina are strongly associated with heart disease cases.
- The age, cholesterol, max heart rate, and oldpeak features have significant differences between the heart disease and normal groups.

## Feature Engineering

The dataset was preprocessed and transformed using the following steps:

- The categorical features were encoded using one-hot encoding.
- The numerical features were scaled using standardization or normalization depending on their distribution.
- The features were selected using correlation matrix, chi-squared test, and ANOVA test.
- The final selected features are: `Age`, `Sex`, `ChestPainType`, `Cholesterol`, `FastingBS`, `ExerciseAngina`, `Oldpeak`, and `ST_Slope`.

## Modeling

The following supervised machine learning models were used to train and test the dataset:

- Logistic Regression
- Support Vector Classifier
- Decision Tree Classifier
- Random Forest Classifier
- K-Nearest Neighbors Classifier

The models were evaluated using the following metrics:

- Accuracy
- Precision
- Recall
- F1-score
- ROC AUC

## Results

The best performing model was the Random Forest Classifier, which achieved an accuracy of 0.87, a precision of 0.88, a recall of 0.88, an F1-score of 0.88, and a ROC AUC of 0.94. 

## Conclusion

This project demonstrates how to use supervised machine learning techniques to solve a binary classification problem with multiple features. The project also shows how to perform exploratory data analysis, feature engineering, and model evaluation to find the best model for the given problem. The project can be extended by using more advanced methods such as hyperparameter tuning, cross-validation, and ensemble learning to improve the model performance. 

## References

- [Index of heart disease datasets from UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets.php?format=&task=cla&att=&area=life&numAtt=&numIns=&type=&sort=nameUp&view=table)
- [Heart Failure Prediction Dataset](https://www.kaggle.com/fedesoriano/heart-failure-prediction)
