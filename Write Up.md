## Classification Project



**Abstract**

____

The goal of this project was to build a classification model predicting if an animal from a shelter would find a home and seeking more insight on the contributing factors.  I worked with the Animal Shelter Intake and Outcome data from the Sonoma County, CA, utilizing different classification algorithms to achieve this goal.



**Design**

____

Animal shelters are places to find animal welcoming homes.  With limited support, it is crucial they allocate their resources effectively, so they can continue to do great work.  By building a classification model to predict the adoption outcome, we can see which features contribute to animals finding future homes, so shelters can utilize their resources effectively.  



**Data**

____

I worked with the Animal Shelter Intake and Outcome data from the Sonoma County, CA.  The data set originally has 21,673 rows and 24 columns. However, after EDA, I worked with 10 features, and they are type of animal, breed, color, neutered/spayed, size, age, days in shelter, reason for intake, animals condition when leaving the shelter, and day of week the animals found ahomes.  Many features were dummified, and the final dataset has 15,281 and 20 features.

The target of the project were two groups: finding a home or not finding a home, and the distribution of these groups in the dataset was 75% and 25% respectively.  Finding a home includes adoption and return to owner, and not finding a home includes transfer to a different shelter, euthanized, appointment made to interact with the animals, died, disposal, escaped/stolen.



**Methodology**

____

I first used logistic regression to build a baseline model on two, seven, and all the features, and the subset with all the features provided the best performace with F1 = 0.871 and AUC = 0.815.

Since the subset with all the features provided the highest scores, I then tried different classification algorithms to see which one moves forward for further hyperparameter tuning.  I tried KNN, logistic regression, decision tree,  and random forest, and the top performer was random forest. 

For my analysis, F1 was the target metric.  I care about F1 because resources will be allocated to the wrong place with increased false positive or increased false negative, so I would like a balanced precision and recall.  With this in mind, GridSearchCV was then used to tune the model to find the best parameters, and the final random forest model gave an F1 score of 0.915 and AUC of 0.918.

**Tools**

____

* Pandas for data cleaning and EDA
* Python sklearn package for classification models
* SHAP for feature importance
* Matplotlib and seaborn for visualizations

**Communication**

____

Findings and slides will be presented.

