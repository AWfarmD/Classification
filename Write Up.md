# Classification Write-Up

### Abstract

The goal of this project was to build a classification model to identify which features lead to positive outcome (adoption or return to owner) that would assist the shelter to utilize their limited resouces properly. I worked with the Animal Shelter Intake and Outcome data from the Sonoma County, CA, utilizing different classification algorithms to achieve this goal.

### Design

Animal shelters are places to find animal welcoming homes. With limited support, it is crucial they allocate their resources effectively, so they can continue to do great work. By building a classification model to predict the adoption outcome, we can see which features contribute to animals finding future homes, so shelters can utilize their resources accordingly.  

### Data

The [Animal Shelter Intake and Outcome](https://data.sonomacounty.ca.gov/Government/Animal-Shelter-Intake-and-Outcome/924a-vesw/data) data from the Sonoma County, CA was used. The data set originally had 21,673 observations and 24 columns, each obervations was an animal's record. After data cleaning and EDA, I worked with 15,281 obervations and 11 features, and they were name of the animal, type of animal, breed, age, color, sex, size, intake type (why did the animal got sent to the shelter), outcome condition (what was the health of the animal when the outcome took place), days in shelter, outcome day of week (what is the day of week when the outcome took place). 

The target of the project were two groups: finding a home (positive outcome) or not finding a home (negative outcome), and the distribution of these groups was 75% and 25% respectively. Finding a home includes adoption and return to owner, and not finding a home includes transfer to a different shelter, euthanized, appointment made to interact with the animals, died, disposal, and escaped/stolen.

### Algorithms

**Cleaning and EDA**

At this stage, some of the columns (impound number, animal ID, intake subtype, etc) from the original dataset were dropped since they were irrelavent. Then, name of the animal was converted to yes (has a name) or no (doesn't have a name), animals' birthdays in days were calculated by subtracting their birth dates from the outcome date, outcome day of week was converted to integer, where Monday is 0 and Sunday is 6, and outliers for days in shelter and obervations that had NaN value in the outcome column were dropped.

Some of the categories within a feature had to be consolidated since there were too many categories. An example was the color of the animal. There were several combinations of different colors. An example with white color, there are black/white, brown/white, tan/white, and gray/white, etc. The color feature was consolidated to mixed color or single color. The categories in outcome condition and intake type were also consolidated.

**Model Training**

KNN, logistic regression, decision tree, and random forest were tried to see which one performs the best, and ROC AUC was used for model selection because it helps us to find a model that better distinguishes positive and negative classes. With these four models, random forest was the top performer with an ROC AUC of 0.916 and an accuracy of 0.876, and it was moved forward for hyperparameter tuning.

For my analysis, accuracy was another performance metric. It was chosen because we can only trust the contributing features will lead to a particular outcome and utilize them when we know the model can accurately predict the outcome.

GridSearchCV with a list of criterion ("gini" and "entropy") was set up to find the best hyperparameters for the random forest classifier, and the n estimator was just set to a very high number, 10,000. The model was then trained with the best hyperparameters (criterion = entropy and n estimator = 10000), and provided an ROC AUC of 0.93 and an accuracy of 0.88 on the test data.

**Feature Importance**

The feature importance was explained with SHAP values. One thing that stood out was Tuesday increases the probability of an animal having a positive outcome, and Sunday decreases the probability of an animal having a good outcome. The shelters can find out what happens on Tuesday which as a work day, actually increases the probability of the positive outcome. Maybe there is always a special activity on that day or friendly volunteers who provide extensive help and knowledge to the people who is looking to adopt an animal work on that day, and then the shelters can take action and make changes accordingly. Similarly, the shelter can find out what happens on Sunday which I thought more adoption will take place as more people do not have to work on that day and can visit the shelter, actually decreases the chance of animals having a positive outcome.

Other feature importance is shown in the presentation slides.

### Tools

* Pandas for data cleaning and EDA

* Python sklearn package for classification models
* SHAP for feature importance
* Matplotlib and seaborn for visualizations

### Communication

Findings and slides will be presented.

