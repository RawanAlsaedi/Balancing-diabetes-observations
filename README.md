# Balancing-diabetes-observations


This project focuses on the task of predicting whether a person has diabetes based on 8 features, such as plasma glucose concentration, age, body mass index (BMI), and others. The dataset is imbalanced, with more non-diabetic cases (label 0) than diabetic cases (label 1). The goal of this project is to balance the dataset and improve the model's ability to predict the minority class (diabetics).





## Model


**K-Nearest Neighbors (KNN)**  model was used to predict diabetes, with the model being trained on the balanced dataset and evaluated using key performance metrics such as accuracy, precision, recall, and F1-score.



## Model Report (before resampling):

```

Model report: 
               precision    recall  f1-score   support

           0       0.76      0.89      0.82        97
           1       0.66      0.44      0.53        48

    accuracy                           0.74       145
   macro avg       0.71      0.66      0.67       145
weighted avg       0.73      0.74      0.72       145


```

## Model Report (after resampling):


```

Model report: 
               precision    recall  f1-score   support

           0       0.70      0.83      0.76        23
           1       0.83      0.70      0.76        27

    accuracy                           0.76        50
   macro avg       0.76      0.76      0.76        50
weighted avg       0.77      0.76      0.76        50



```



## Observations

- **Before resampling**, the model showed higher precision and recall for class 0 (non-diabetic), but lower recall for class 1 (diabetic), indicating it was biased toward predicting the majority class. The overall accuracy was 74%, but the F1-score for class 1 was only 0.53, highlighting poor performance in detecting diabetics.

- **After resampling**, the model's performance on class 1 (diabetic) improved significantly, with higher recall (0.70) and precision (0.83), resulting in a balanced F1-score of 0.76 for both classes.  The overall accuracy slightly increased to 0.76 and the model now gives more attention to the minority class.
