# Predicting Covid Mortality with Machine Learning.
> This project aims to design a predictor to predict mortality among confirmed CoVID-19 patients in South Korea using logistic regression and support vector machines. 
Compare the predictor based on logistic regression and support vector machines and identify best among them. 

## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Features](#features)
* [Code](#code)
* [Results](#results)
* [Conclusion](#conclusion)
* [Reference](#reference)

## General info
* Dataset for the project is taken from [kaggle](https://www.kaggle.com/kimjihoo/coronavirusdataset). The dataset was released by Korea Centers for Disease Control and Prevention, and it contains information on the Covid-19 cases in South Korea.
* Logistic regression and Support Vector Machines models are designed from scratch.
* Models are compared based on Accuracy, Precision, Recall, F1 score, and RUC_AUC_SCORE.
* The predictor is based on age, gender, province, and whether the patient had been in contact with a COVID positive patient.

## Technologies
* Programming Language -  Python3.

## Code
* Code -  [Jupyter notebook.](https://github.com/jainsanyam786/OptimizationForMachineLearning/blob/master/Predict_Mortality_due_to_COVID/FinalProject.ipynb) 
* Above jupyter notebook contains code for data pre-processing, model designing, training, and testing.

## Features
SMOTE (Synthetic Minority Oversampling Technique) and ADASYN (Adaptive Synthetic Sampling Method) are used to reduce the impact of class imbalance in data.
* ### SMOTE 
  Data augmentation technique for the minority class which duplicates exiting examples in the minority class. These examples don’t add any new information to the model.  
* ### ADASYSN 
  ADASYSN is similar to SMOTE as it also duplicates existing examples but preference is given to examples that are not in homogenous neighborhoods, thus generating "hard to learn" samples.
  
* Polyak's momentum-based stochastic gradient descent is used to train logistic regression classifier.
* Normal stochastic gradient descent is used to train the SVM classifier. 
  
## Results
* Correlation matrix for data.
<img src="./img/data_corr.png" alt="data_corr" width="500" height="500"/>

* Logistic Regression based classifier with SMOTE (Left - Training Data & Right - Testing Data).
<img src="./img/Image1.png" alt="Image1" width="800" height="500"/>

* Logistic Regression based classifier with ADASYN (Left - Training Data & Right - Testing Data).
<img src="./img/Image2.png" alt="Image2" width="800" height="500"/>

* SVM based classifier with SMOTE (Left - Training Data & Right - Testing Data).
<img src="./img/Image3.png" alt="Image3" width="800" height="500"/>

* SVM based classifier with ADASYN (Left - Training Data & Right - Testing Data).
<img src="./img/Image4.png" alt="Image4" width="800" height="500"/>

* Comparing all models based on Accuracy, Precision, Recall, F1 score, and RUC_AUC_SCORE.
<img src="./img/Image6.png" alt="Image6" width="1200" height="150"/>

## Conclusion
* In terms of overall accuracy logistic regression is better.
* In terms of F1 score and Precision logistic regression is way better than SVM.
* In terms of ROC_AUC_SCORE and Recall SVM is better but, the difference is small.
### Logistic regression-based model correctly predicts if the person will survive or not better than SVM based model.

## Reference
* [Predicting CoVID-19 community mortality risk using machine learning and development of an online prognostic tool, 2020 by Das et al](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7528809/pdf/peerj-08-10083.pdf)
