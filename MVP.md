## MVP ##

The goal of this project is to predict if an animal will find a home, and see what features contribute to it, so the shelters can allocate their resources effectively to continue the greate work.

Baseline was performed with logistic regression with 2 features, 4 features, and all features, and the 2 feature subset provided F1 of 0.854 and ROC AUC of 0.608 and 4 features provided F1 of 0.888 and ROC AUC of 0.796.  The subset with all the features provide the best score of F1=0.930 and ROC AUC=0.923.

Below is the ROC curves for the three subsets.

![ROC Curve](https://github.com/AWfarmD/Classification/blob/main/Figure/Baseline%20ROC%20Curve.png?raw=true)

My plan next is to build other models with all features and compare which one performs the best, and then further tuning the model to see if it can perform better.



