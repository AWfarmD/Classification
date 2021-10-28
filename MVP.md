## MVP ##

The goal of this project is to build a classification model to identify which features contribute more to the positive outcomes (animals get adopted or return to owner), so the shelter will be able to utilize this information to distribute their limited resources properly.

ROC AUC will be used for model selection, and accuracy will be used for final model performace metric.  Accuracy is chosen because we can only believe the contributing features will lead to a particular outcome and utilize them when we know the model can accurately predict the outcome.

Baseline was performed with logistic regression with the following features and scores:

* 2 features: accuracy = 0.746 and ROC AUC = 0.608
* 7 features: accuracy =  0.779 and ROC AUC = 0.749
* All features: accuracy = 0.846 and ROC AUC = 0,872

Below is the ROC curves of different models:



With random forest performs the best, my next step will be tuning its hyperparameters and see if better accuracy score can be obtained. And the feature importance will be explained with SHAP values.





