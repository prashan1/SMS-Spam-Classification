# SMS-Spam-Classification
### About

We try to classify SMS messages as SPAM or NOT SPAM using various ML algorithms. The notebook (spam_classifier.ipynb)consists steps to process and explore the dataset, convert messages to vectors and applying ML techniques for the same.

The notebook(spam_classifier_rnn.ipynb) uses a Recurrent Neural Network (RNN) and LSTM to classify the messages. RNNs are networks with loops in them, allowing information from previous time step to persist capable of handling long-term dependencies.

### Install

This project requires **Python 3** and the following Python libraries installed:

- [xgboost](xgboost.readthedocs.io/en/latest/build.html)
- [wordcloud](https://github.com/amueller/word_cloud)
- [sklearn](scikit-learn.org/)
- [pandas](https://pandas.org/)
- [nltk](https://nltk.org/)
- [Matplotlib](https://matplotlib.org/)

Make sure you have [Jupyter Notebook](http://ipython.org/notebook.html) installed.

You could just install [Anaconda](http://continuum.io/downloads) distribution of Python, which already has the above packages and more included. 


### Run

In a terminal or command window, navigate to the top-level project directory (that contains this README) and run one of the following commands:

```bash
ipython notebook spam_classifier.ipynb
```  
or
```bash
jupyter notebook spam_classifier.ipynb
```

This will open the Jupyter Notebook software and project file in your browser.

### Dataset

The Dataset is a set of SMS tagged messages  collected for SMS Spam research. It contains one set of SMS messages in English of 5,574 messages, tagged acording being ham (legitimate) or spam.

The dataset is available [here.](https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection)

Example Messages:

```
ham What you doing?how are you? 
ham Ok lar... Joking wif u oni... 
ham dun say so early hor... U c already then say... 
ham MY NO. IN LUTON 0125698789 RING ME IF UR AROUND! H* 
ham Siva is in hostel aha:-. 
ham Cos i was out shopping wif darren jus now n i called him 2 ask wat present he wan lor. Then he started guessing who i was wif n he finally guessed darren lor. 
spam FreeMsg: Txt: CALL to No: 86888 & claim your reward of 3 hours talk time to use from your phone now! ubscribe6GBP/ mnth inc 3hrs 16 stop?txtStop 
spam Sunshine Quiz! Win a super Sony DVD recorder if you canname the capital of Australia? Text MQUIZ to 82277. B 
spam URGENT! Your Mobile No 07808726822 was awarded a L2,000 Bonus Caller Prize on 02/09/03! This is our 2nd attempt to contact YOU! Call 0871-872-9758 BOX95QU 

```

## Results 
The predictions(accuracy scores) using various ML algorithms are as follows:.

precision: 0.98582996   ,1.        
recall:    1.    ,    0.90070922.
fscore: 0.99286442 ,  0.94776119.
support:  974,       141.
############################
              precision    recall  f1-score   support.

           0       0.99      1.00      0.99       974
           1       1.00      0.90      0.95       141

   micro avg       0.99      0.99      0.99      1115.
   macro avg       0.99      0.95      0.97      1115.
weighted avg       0.99      0.99      0.99      1115.
 samples avg       0.99      0.99      0.99      1115.


The Wordclouds below show the most common words occuring in each of the categories:

# Spam Messeges

![Common Span Messeges](https://user-images.githubusercontent.com/57286404/82121082-1de3f500-97a8-11ea-848c-6c1c9729505c.jpg)

# Example
![Example](https://user-images.githubusercontent.com/57286404/82121049-e6754880-97a7-11ea-9e1d-003c653edbdc.jpg)

###### Validation accuracy using LSTM is 98.2% And by using Bidirection LSTM the test accuracy is 99/2%
