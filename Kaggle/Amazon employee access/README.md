# Amazon Employee Resource Access Challenge

[![Amazon Logo](https://raw.githubusercontent.com/shashank8388/ML/master/Kaggle/Amazon%20employee%20access/Amazon-PNG-Transparent-Image.png "Amazon Logo")](https://raw.githubusercontent.com/shashank8388/ML/master/Kaggle/Amazon%20employee%20access/Amazon-PNG-Transparent-Image.png "Amazon Logo")

## Problem Statement:
[![Resource sharing](https://raw.githubusercontent.com/shashank8388/ML/master/Kaggle/Amazon%20employee%20access/enterprise-reporting-tools-300x225.png "Resource sharing")](https://raw.githubusercontent.com/shashank8388/ML/master/Kaggle/Amazon%20employee%20access/enterprise-reporting-tools-300x225.png "Resource sharing")

The dataset consists of real historical data collected from 2010 & 2011 of Amazon employees. Employees are manually allowed or denied access to resources over time. This access may allow an employee to read/manipulate resources through various applications or web portals. It is assumed that employees fulfilling the functions of a given role will access the same or similar resources. It is often the case that employees figure out the access they need as they encounter roadblocks during their daily work (e.g. not able to log into a reporting portal). Create a auto access model capable of learning from this historical data to predict approval/denial of resources for employees and to minimize the human involvement required to grant or revoke employee access.

## About the dataset:
This is a considerable amount of data regarding employee's role within an organization and the resources to which they have access. Given the data related to current employees and their provisioned access, I am trying to build model that automatically determine access privileges as employees enter and leave roles within a company. These auto-access models seek to minimize the human involvement required to grant or revoke employee access.


## Python libraries used:

[![Library image](https://raw.githubusercontent.com/shashank8388/EDA/master/Summer%20Olympics%20Data/photo-1524995997946-a1c2e315a42f.jpg "Library image")](https://raw.githubusercontent.com/shashank8388/EDA/master/Summer%20Olympics%20Data/photo-1524995997946-a1c2e315a42f.jpg "Library image")

  numpy - For implementing milti-dimensional array and matrices
  <br>
  pandas - For data manipulation and analysis
  <br>
  seaborn and matplotlib - Fot data visualization purpose
  <br>
  sklearn(scikit learn) - python library providing many supervised and unsupervised algorithms<br>
 
 
 ## Exploratory Data Analysis:

[![Analysis](https://raw.githubusercontent.com/shashank8388/EDA/master/shutterstock357106388.jpg "Analysis")](https://raw.githubusercontent.com/shashank8388/EDA/master/shutterstock357106388.jpg "Analysis")
  
  1. Multicollinearity between feature variables is not present.
  2. No null values present in the dataset.
  3. Possible values of target variable ACTION is 1 and 0.
    1 - Resource is approved to the employee or Employee got the access that resource.
    0 - Resource is rejected for that employee or Employee was denied that resource.
    
## Model Building:

[![ML Mode;](https://raw.githubusercontent.com/shashank8388/ML/master/data-analyst-vs-data-scientist-article.jpg "ML Mode;")](https://raw.githubusercontent.com/shashank8388/ML/master/data-analyst-vs-data-scientist-article.jpg "ML Mode;")

 I have used below machine learning algorithms for the model building.
 1. Random Forest Classifier
 2. Decision Tree Classifier
 3. Logistic Regression<br>
 
 Analysis based on confusin matrix.<br>
 False positive - model predict a resource is approved for the employee but actually it isn't.<br>
 False negative - model predict a resource is denied for the employee but actually it isn't.<br>
 
 In this scenario, both values to be high are not good to have. We should try to minimize both false positive and false negative So, we should choose the model having highest F1 score and highest AUC_ROC score.<br>
 
 After evaluating on the basis of AUC_ROC and F1 score, I concluded that using random forest classifier for this problem statement will 
 be the best fit.
