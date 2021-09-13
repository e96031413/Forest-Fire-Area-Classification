# Forest-Fire-Area-Classification
https://www.kaggle.com/e96031413/forest-fire-area-classification

Our model is used on [Streamlit-Wildfire-Prediction](https://github.com/jason211346/Streamlit-Wildfire-Prediction)

There are two notebook in this project:

**[Forest-Fire-Area-Classification.ipynb](https://github.com/e96031413/Forest-Fire-Area-Classification/blob/master/Forest-Fire-Area-Classification.ipynb)**

In this notebook, we use forest fire dataset from [UCI Machine Learning Repository Forest Fires Data Set](https://archive.ics.uci.edu/ml/datasets/forest+fires). The originally dataset is used to predict the fire area, we use date pre-processing technique to modify the dataset so that we can see it as a classification problem.

We compare serveral different ML alogthrims, the table below shows the cross val score:

|algorithms          |cross_val_score|
|--------------------|----------|
| LogisticRegression | 49.56 |
| KNN                | 54.06 |
| DecisionTree       | 53.16 |
| GaussianNB         | 50.53 |
| SVM                | 57    |
| MLP                | 53.53 |
| GradientBoost      | 53.2  |
| AdaBoost           | 54.3  |
| Bagging            | 50.1  |
| RandomForest       | 54    |
| ExtraTrees         | 51.8  |

According to the table above, we can find that the highest cross val score is SVM, that's the reason why we choose SVM as our final model

---

**[Forest-Fire-Area-Classification-NASA.ipynb](https://github.com/e96031413/Forest-Fire-Area-Classification/blob/master/Forest-Fire-Area-Classification-NASA.ipynb)**

This notebook used different dataset from previous one, we directly use fire dataset from [NASA Active Fire Data](https://firms.modaps.eosdis.nasa.gov/active_fire/#firms-txt). Apply the same ML methods again, the cross val score is higher than previous one due to the number of data is more that UCI Machine Learning Repository.

|algorithms          |cross_val_score|
|--------------------|----------|
| LogisticRegression | 83.759  |
| KNN                | 80.61 |
| DecisionTree       | 79.05 |
| GaussianNB         | 64.80 |
| SVM                | 83.65 |
| MLP                | 83.17 |
| GradientBoost      | 85.49 |
| AdaBoost           | 84.97 |
| Bagging            | 82.59 |
| RandomForest       | 85.10 |
| ExtraTrees         | 84.61 |

According to the table above, we can find that the highest cross val score is GradientBoost rather than SVM. However, this dataset may not be the right choice for ordinary users to predict whether it is on fire or not. Because its data feature is from sattelite equipment, not from our daily equipment.
