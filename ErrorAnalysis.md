# Error Analysis of the kNN predictive model

## Introduction to computer programming in science and engineering - section 2

## Author: Todor Stefanov

Date: 14 May 2019

## Distributions of Model Accuracy

It is normal that every time the classification model is ran it gives a different accuracy, as it is based on a training set and a test set. The training set represents 70% of the entire dataset, and the test set is the other 30%. Every time it is ran, this split is made, and since the entire set is shuffled before being split into training and test sets, it means that they are always different, thus the program is trained on different datapoints every time, which may differ more or less from the testset, thus yielding different accuracies.

Running the program many times (1000 times), sows how the accuracy of the predictive model is around 96%, and does not fluctuate much. In fact, the mean is of 96.7% and the standard deviation is of 1.31 x 10^-4, which shows how close the accuracies between predictions are. This model can be said to be fairly accurate, given such numbers, but most importantly, consistent in its accuracy. 

## Analysis of different error types

A false positive is a wrong positive prediction. In our case, a false positive would be a healthy patient, which the program predicts to have breast cancer. A false negative is a wrong negative prediction. It would be a patient who has breast cancer, but the program predicts they are healthy. These two errors are important factors in the medical field, and are to be considered in predictive models. A false positive implies treating a patient who does not need treatment, and a false negative implies not treating a patient who needs treatment, and thus have different consequences for erroneous predictions.

Precision is the number of true positives over the total number of predicted positives (true positives + false positives). The closer the precision approaches to 1, the lower the number of false positives. Recall is the number of true positives over the total number of positives. The closer the recall approaches to 1, the lower the number of false negatives. Running the code shows a mean of 96% for the precision, and 99% for the recall, meaning the model has more difficulty with false positives, than false negatives. Changing the hyperparameter k to be higher seems to lower the recall, but heighten the precision. This means that considering more closest neighbours help the model with false negatives, but is detrimental for the false positives. 
