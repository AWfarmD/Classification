## MVP ##

The goal of this project is to predict if an animal will find a home.

Baseline was performed with logistic regression with the following features and scores:

* 2 features: F1 = 0.854 and ROC AUC = 0.608 
* 4 features: F1 = 0.888 and ROC AUC = 0.796
* All features: F1 = 0.930 and ROC AUC = 0.923.

Below is the ROC curves of different models:

![roc curves](https://github.com/AWfarmD/Classification/blob/main/Figure/ROC%20Curves%20-%20Models.png+?raw=true)

With random forest performs the best and logistic regression comes in second, hyperparameter tunings will be done on these two models to see if the perfromance metrics can be better.



