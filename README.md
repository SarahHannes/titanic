# Predicting Titanic passengers' survival using Machine Learning <a href="https://htmlpreview.github.io/?https://raw.githubusercontent.com/SarahHannes/titanic/main/titanic-survivor.html">[Code]</a> <a href="https://htmlpreview.github.io/?https://raw.githubusercontent.com/SarahHannes/titanic/main/report.html">[EDA Report]</a>

Submission for <a href="https://www.kaggle.com/competitions/titanic">Titanic competition</a> on Kaggle.

### Methodology
EDA reports were automated using `{DataExplorer}` and `{SmartEDA}` libraries in R. `Pclass`, `Fare` and `Sex` were chosen as the indepdendent variables as they were `high`. Train data is further split into train and validation set in 80:20 ratio. Several baseline models were built using Grid Search CV. Best scores and parameters for each model were as shown below. Best model was `DecisionTreeClassifier` with an accuracy score of 81% on train set. Test data is then predicted using the best model. Submission file can be found <a href="submission.csv">here</a>.

#### EDA
<img src="https://user-images.githubusercontent.com/78901374/169022681-dbd16da7-b7df-47ec-b216-d5248f16654a.jpg" width=550>
<img src="https://user-images.githubusercontent.com/78901374/169022120-eeb96c9a-05dc-4785-8995-f19e126ada29.png" width=550>


#### Grid Search CV result
<img src="https://user-images.githubusercontent.com/78901374/169019761-0124c20f-833b-4cde-ad17-6a4f5cee7887.png" width=550>

#### Classification Report on Validation set
```
              precision    recall  f1-score   support

          No       0.84      0.89      0.87       110
         Yes       0.81      0.74      0.77        69

    accuracy                           0.83       179
   macro avg       0.83      0.82      0.82       179
weighted avg       0.83      0.83      0.83       179
```

#### Confusion Matrix on Validation set
<img src="https://user-images.githubusercontent.com/78901374/169020699-79f85b97-1c44-4452-bf43-45e4c035bfcf.jpg" width=400>
