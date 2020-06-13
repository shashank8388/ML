# SMS classification problem


[![SMS filter](https://github.com/shashank8388/ML/blob/master/MISC/SMS_detection/SPAM.png?raw=true "Amazon Logo")](https://github.com/shashank8388/ML/blob/master/MISC/SMS_detection/SPAM.png?raw=true "SMS filter")

## Problem Statement:
[![Classification](https://github.com/shashank8388/ML/blob/master/MISC/SMS_detection/sms_classify.png "Resource sharing")](https://github.com/shashank8388/ML/blob/master/MISC/SMS_detection/sms_classify.png "Classification")

In this assignment we will take an interesting usecase of NLP(Natural Language Processing), we won't dig deep into it, but just that much which is required to solve this case-study problem. The SMS Spam Collection is a set of SMS tagged messages that have been collected for SMS Spam research. It contains one set of SMS messages in English of 5,572 messages, tagged acording being ham (legitimate) or spam.

We need to create a model which will detect if an SMS is spam or not spam.

## About the dataset:
The SMS Spam Collection is a set of SMS tagged messages that have been collected for SMS Spam research. It contains one set of SMS messages in English of 5,574 messages, tagged acording being ham (legitimate) or spam.
The dataset consists of 5572 rows.
Below is a table having brief description of features present in the dataset.

Feature	Description<br>
v1 - Target variable, with only 2 set of values, spam or ham.
<br>
v2 - Explanatory variable, actual SMS which has to be categorized as spam or ham.
<br>



## Python libraries used:

[![Library image](https://raw.githubusercontent.com/shashank8388/EDA/master/Summer%20Olympics%20Data/photo-1524995997946-a1c2e315a42f.jpg "Library image")](https://raw.githubusercontent.com/shashank8388/EDA/master/Summer%20Olympics%20Data/photo-1524995997946-a1c2e315a42f.jpg "Library image")

  numpy - For implementing milti-dimensional array and matrices
  <br>
  pandas - For data manipulation and analysis
  <br>
  seaborn and matplotlib - Fot data visualization purpose
  <br>
  sklearn(scikit learn) - python library providing numerous supervised and unsupervised algorithms<br>
 
 
 
 ## Exploratory Data Analysis:

[![Analysis](https://raw.githubusercontent.com/shashank8388/EDA/master/shutterstock357106388.jpg "Analysis")](https://raw.githubusercontent.com/shashank8388/EDA/master/shutterstock357106388.jpg "Analysis")
  
  1. Most of the SMSs are of length varying between 20-150 characters.
  2. In the given dataset, most of the ham SMS are of length 10-180. However, spam SMS are generally 100-180 characters long.
  3. Possible values of target variable label is 1 and 0.<br>
    1 - SMS is spam<br>
    0 - SMS is ham(legitimate)
    

## Bag of Words Approach:

![Bag of words](https://raw.githubusercontent.com/shashank8388/ML/master/MISC/SMS_detection/images.jpg "Bag of words")
 
What we have here in our data set is a large collection of text data (5,572 rows of data).
Most ML algorithms rely on numerical data to be fed into them as input, and email/sms messages are usually text heavy. We need a way to represent text data for machine learning algorithm and the bag-of-words model helps us to achieve that task.

1. It is a way of extracting features from the text for use in machine learning algorithms.<br>
2. In this approach, we use the tokenized words for each observation and find out the frequency of each token.<br>
3. Using a process which is shown in the notebook file, we can convert a collection of documents to a matrix, with each document being a row and each word(token) being the column, and the corresponding (row,column) values being the frequency of occurrence of each word or token in that document.<br>

<br>

![Approach](https://github.com/shashank8388/ML/blob/master/MISC/SMS_detection/countvectorizer.png "Approach")

<br>


    
## Model Building:

[![ML Mode;](https://raw.githubusercontent.com/shashank8388/ML/master/data-analyst-vs-data-scientist-article.jpg "ML Mode;")](https://raw.githubusercontent.com/shashank8388/ML/master/data-analyst-vs-data-scientist-article.jpg "ML Mode;")

 I have used below machine learning algorithms for the model building.
 1. Random Forest Classifier
 2. Decision Tree Classifier
 3. Logistic Regression
 4. Naive Bayes<br>
 
 Analysis based on confusin matrix.<br>
 False positive - model predict a SMS to be spam but actually it isn't.<br>
 False negative - model predict a SMS to be ham but actually it isn't.<br>
 
 Here in this case, if prediction from model indicates the SMS to be spam but actually it's not spam, that model is not correct. In this case, an important SMS may be lost if model predicts that ham to be spam. Hence our false positives should be as low as possible. And to decrease the false positive, precision should be high.<br>
 
 After evaluating on the basis of precision, I concluded that using random forest classifier for this problem statement will 
 be the most suitable as False positive for testing data is 0 in this case.

