# Machine Learning Analysis for Credit Risk

## Background
Credit risk is an inherently unbalanced classification problem, as the number of good loans easily outnumber the number of risky loans. Therefore, there is a need to employ different techniques to train and evaluate models with unbalanced classes. This analysis uses Python's imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. Finally I evaluated the performance of these models and made a recommendation on whether they should be used to predict credit risk.

## Analysis results

### Credit Risk Resampling Techniques

Logistic regression analysis was carried out using different resampling techniques to predict high or low risk loans.

***Naive Random Oversampling results:***

Accuracy score: 0.8446


| | pre   |      rec      |  f1 |
|:---:|:----------:|:-------------:|------:|
|Low| 1.00 |  0.84 | 0.92 |
|High| 0.03 |    0.82   |   0.06 |
|avg/total| 0.99 |    0.84   |   0.91 |


***SMOTE Oversampling:***

Accuracy score: 0.8655


| | pre   |      rec      |  f1 |
|:---:|:----------:|:-------------:|------:|
|Low| 1.00 |  0.87 | 0.93 |
|High| 0.03 |    0.81   |   0.07 |
|avg/total| 0.99 |    0.87   |   0.92 |


***Undersampling by ClusterCentroids:***

Accuracy score: 0.7626


| | pre   |      rec      |  f1 |
|:---:|:----------:|:-------------:|------:|
|Low| 1.00 |  0.76 | 0.86 |
|High| 0.02 |    0.88   |   0.04 |
|avg/total| 0.99 |    0.76   |   0.86 |

***Combination (Over and Under) Sampling:***

Accuracy score: 0.5568


| | pre   |      rec      |  f1 |
|:---:|:----------:|:-------------:|------:|
|Low| 1.00 |  0.56 | 0.71 |
|High| 0.01 |    0.71   |   0.02 |
|avg/total| 0.99 |    0.56   |   0.71 |


### Credit Risk Ensemble Techniques

***Balanced Random Forest Classifier***

Accuracy score: 0.7735


| | pre   |      rec      |  f1 |
|:---:|:----------:|:-------------:|------:|
|Low| 1.00 |  0.90 | 0.95 |
|High| 0.04 |    0.64   |   0.07 |
|avg/total| 0.99 |    0.90   |   0.94 |

***Easy Ensemble AdaBoost Classifier***

Accuracy score: 0.9319


| | pre   |      rec      |  f1 |
|:---:|:----------:|:-------------:|------:|
|Low| 1.00 |  0.94 | 0.97 |
|High| 0.09 |    0.92   |   0.16 |
|avg/total| 0.99 |    0.94   |   0.97 |

## Recommendations

Judging by the accuracy score, the model algorithm that produced classification results with the highest accuracy was the Easy Ensemble AdaBoos Classifier (0.9319).
Hence this would be the recommended method to predict high risk loans.
