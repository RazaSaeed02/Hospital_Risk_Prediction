# Hospital_Risk_Prediction

## Project Objectives
- Develop a Machine Learning Model to predict a patients chances of being admitted to the hospital
- The model will give a risk level between 0 and 1
- Risk level less than 0.1 will be classified as low risk, between 0.1 and 0.5 will be classified as medium risk, and higher than 0.5 will be classified as high risk

## Model Methodology
- 748 Patients were in the dataset
- Trained model on 70 % of the data (523 patients) and tested it on the remaining 30 %  (225 patients)
- The training set had 324 out of the 523 patients (62 %) with risk of 0 and 199 out of the 523 patients (38 %) with risk of 1
- The test set had 130 out of the 225 patients (58 %) with risk of 0 and 95 out of the 225 patients (42 %) with risk of 1
- Trained 3 models (a logistic regression model, a random forest model, and a gradient boosting model)

## Model Performance
- Best performing model was the Gradient Boosting Model
- Average score using 5-fold cross validation was 88 % and standard deviation of 2.3 %
- The accuracy on the test set was 88.90 %
- Precision was 87.23 % and Recall was 86.32 %
- Of the 130 patients with risk of 0 in the test dataset, the model correctly identified 118 of them
- The model therefore had a false positive rate of 9.23 % (12 / 130)
- Of the 95 patients with risk of 1 in the test dataset, the model correctly identfied 82 of them (this is the same as Recall)
- The model therefore had a false negative rate of 13.68 % (13 / 95)
- The model predicted 95 out of the 225 patients (42 %) in the test dataset as high risk, 37 patients as medium risk (16 %), and 93 patients as low risk (41 %)
- AUC on the test set was 0.962

## Model Interpretation
- The factors which contributed the most to the risk of hospitalization were systolic blood pressure, body temperature and body weight
- An increase of roughly 35 mm Hg in Systolic Blood Pressure leads to a 171 % increase in the odds of hospitalization (all other factors held constant)
- An increase in body temperature of roughly 0.67 degrees fahrenheit leads to a 56 % increase in the odds of hospitalization (all other factors held constant)
- An increase of roughly 21 kg in body weight leads to a 56 % increase in the odds of hospitalization (all other factors held constant)
- The patients who have at least one disease have a 42 % higher chance of being hospitalized compared to patients without any disease
- Going up 1 level of stress (ex. from no stress to little stress, from little stress to medium stress, etc.) is associated with a 21 % increase in the odds of being hospitalized

  
