## Stroke_Patient-Analysis
1. Installation
2. Project Motivation 
3. File Descrription
4. Results
5. Licensing, Authors, and Acknowledgements


### Installation

Use pytthon 3.

### Project Motivation and Details

#### Business Problem

The idea behind the analysis is to identify the main predictors of Stroke. 

To understand this i have looked at 3 main questions:
1. Does smoking increase the probability of getting stroke?
2. Does a patient with other underlying conditions more susceptible to stroke?
3. What are the top three predictors of stroke?
#### Data Understanding
The data contains historical information of 5000 patients with 12 attributes. The attributes have both demographic and patient healthy info: Below is the description of the variables
1. Id: Unique id
2. gender: Gender of the patient
3. Age: Age in years of the patient
4. Hypertension: Hypertension binary feature (1- has disease ,0 – No disease)
5. Heart Disease: Heart disease binary feature (1- has disease ,0 – No disease)
6. Ever Married:  Has patient ever married
7. Work Type: Work type of the patient
8. Residence_type: Residence type of the patient
9. avg_glucose_level: Average glucose level in blood
10. BMI: Body Mass Index
11. smoking_status: Smoking status of the patient
12. stroke: Stroke event- indicates whether a customer has stroke or not (1- has stroke ,0 – No stroke)


More info about the data can be found in [this link](https://www.kaggle.com/fedesoriano/stroke-prediction-dataset)

#### Prepare Data
The data was generally clean, with only one attribute with missing variables. The missing values were imputed using mean.

Categorical variables were changed into dummies, by creating k-1 variables and dropping the original variables

#### Modelling
Since it is a classification problem, I have a classification model. After running several models and optimization Adaboost Classifier performed the best.  It is an ensemble model that trains weak learners sequentially and then combines them to get a good performing model. More info about adptive boosting can be found in [this link](https://www.analyticsvidhya.com/blog/2015/11/quick-introduction-boosting-algorithms-machine-learning/)

#### Evaluation
We use recall, precision, and f1-score to evaluate the model performance. The reason for using the above and not accuracy or Area under the curve is because the data is highly imbalanced such that if our model was so naive to predict everyone as not having stroke the accuracy level will still be above 80%. 
F1-score helps in getting a good balance of the precision and recall
Also, I optimized more on recall than the precision since it is a lesser harm to label a patient that they will get stroke and not get it than fail to identify a patient who will actually get stroke

#### Results and Conclusion
Summary of the result published in a [medium article](https://medium.com/@gitahidave/what-are-the-possible-causes-of-stroke-e53325d2bfe3)



### File Description
The repo has 3 notebooks. Each addressing the 3 questions as indicated above
 
### Licensing, Authors, and Acknowledgements
The data was sourced from [kaggle](https://www.kaggle.com/fedesoriano/stroke-prediction-dataset), and the code is free for use.



