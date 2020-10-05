# Forest-Fire-Area-Classification
https://www.kaggle.com/e96031413/forest-fire-area-classification

Our model is used on [Streamlit-Wildfire-Prediction](https://github.com/jason211346/Streamlit-Wildfire-Prediction)

There are two notebook in this project:

**[Forest-Fire-Area-Classification.ipynb](https://github.com/e96031413/Forest-Fire-Area-Classification/blob/master/Forest-Fire-Area-Classification.ipynb)**

In this notebook, we use forest fire dataset from [UCI Machine Learning Repository Forest Fires Data Set](https://archive.ics.uci.edu/ml/datasets/forest+fires). The originally dataset is used to predict the fire area, we use date pre-processing technique to modify the dataset so that we can see it as a classification problem.

We compare serveral different ML alogthrims, the table below shows the cross val score:

|algorithms          |cross_val_score|
|--------------------|----------|
| LogisticRegression | 0.495667 |
| KNN                | 0.540667 |
| DecisionTree       | 0.531667 |
| GaussianNB         | 0.505333 |
| SVM                | 0.57     |
| MLP                | 0.535333 |
| GradientBoost      | 0.532    |
| AdaBoost           | 0.543    |
| Bagging            | 0.501    |
| RandomForest       | 0.54     |
| ExtraTrees         | 0.518    |

According to the table above, we can find that the highest cross val score is SVM, that's the reason why we choose SVM as our final model

---

**[Forest-Fire-Area-Classification-NASA.ipynb](https://github.com/e96031413/Forest-Fire-Area-Classification/blob/master/Forest-Fire-Area-Classification-NASA.ipynb)**

This notebook used different dataset from previous one, we directly use fire dataset from [NASA Active Fire Data](https://firms.modaps.eosdis.nasa.gov/active_fire/#firms-txt). Apply the same ML methods again, the cross val score is higher than previous one due to the number of data is more that UCI Machine Learning Repository.

|algorithms          |cross_val_score|
|--------------------|----------|
| LogisticRegression | 0.83759  |
| KNN                | 0.806166 |
| DecisionTree       | 0.790570 |
| GaussianNB         | 0.648099 |
| SVM                | 0.836511 |
| MLP                | 0.831783 |
| GradientBoost      | 0.854933 |
| AdaBoost           | 0.849769 |
| Bagging            | 0.825925 |
| RandomForest       | 0.851002 |
| ExtraTrees         | 0.846120 |

According to the table above, we can find that the highest cross val score is GradientBoost rather than SVM. However, this dataset may not be the right choice for ordinary users to predict whether it is on fire or not. Because its data feature is from sattelite equipment, not from our daily equipment.
