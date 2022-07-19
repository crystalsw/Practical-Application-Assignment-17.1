# Practical-Application-Assignment-17.1
## How many marketing campaigns does this data represent?
After examining the Materials and Methods section of the paper, I found that there are 17 marketing campaigns.
## What is the baseline performance that our classifier should aim to beat?
The baseline performance that our classifier should aim to beat is 0.8704068241469817 .
## Model Comparisons
The baseline test accuracy is 0.870407. All of the models with default parameters cannot beat the baseline or just the same as the baseline.
## Improving the Model
### More feature engineering and exploration. For example, should we keep the gender feature? Why or why not?
I am unable to answer the question "Should we keep the gender feature? Why or why not?". Because gender does not exist in the data. I have refined the question a little bit: should we keep the education feature? Why or why not?"<br />
After using permutation importance, the 4 important features in order are marital_married, marital_single, marital_divorced and education_university.degree . I see that education is somehow important, but it is not as important as marital.<br />
After some calculations and removing education related features, the accuracy did not change in SVM and Logistric Regression. While for KNN and Decision Tree, the train accuracy has slightly decreased after removal and the test accuracy has slightly increased after removal.<br />
To sum up, we can skip the education feature if the increase in 1% accuracy is not of concern.<br />
## Hyperparameter tuning and grid search
After using GridSearchCV, the model is fine tuned as belows.<br />
DecisionTreeClassifier(max_depth=1, min_samples_split=5)<br />
KNeighborsClassifier(n_neighbors=15)<br />
SVC(gamma=10.0, kernel='linear')<br />
## Further works and recommendations:
1. The data is imbalance. Some methods like SMOTE need to be used<br />
2. Try to enhance the SVM model to make it work in GridSearchCV in a resonable timeframe<br />
3. Try more parameters in GridSearchCV<br />
