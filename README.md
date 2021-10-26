## The task at hand is sentiment classification using Natural Language Processing.
### I have classified the tweets by implementing Sentiment analysis on the dataset link given below. The objective is to recognize whether the given tweet is oriented as negative (-1), neutral (0), or positive (1) tone. 

### dataset link: https://www.kaggle.com/saurabhshahane/twitter-sentiment-dataset

### I'll be explaining what's happening in the code(IN DETAIL) here: 
#### 1. I start off by calling the necessary modules and required libraries for the problem statement. Before running this file, do make sure you have wordcloud installed in your local system. wordcloud will essentially be used further on for visual display of positive and negative phrases in tweets.
#### 2. Next, I import the dataset, the link to which is given above. I've created a dataframe that references the csv file, and all operations will be carried out in this data frame. 
#### 3. Now, I perform exploratory data analysis on my data. I check for null values, unique values, remove any clean text categorized null values from my dataset. I implement boxplot for graphically depicting groups of numerical data
#### 4. Next, we move onto data pre-processing. Removal of stop words and lemmatization is done using the nltk toolkit. I have printed the words using word cloud as mentioned before, and if the category equals 1, i've displayed positive words, if it's zero, i have displayed neutral words, and if it's -1, i've displayed negative words.
#### 5. Now, I perform feature extraction using count vectorizer. I call the fit() function to learn vocabulary from my 'clean_text' column and then I split the data into testing and training data set, and use the transform function to encode each of them as a vector.
#### 6. One-vs-all strategy is used to implement a logistic regression model for my problem statement. I've used logistic regression because it's the most efficient classification algorithm.
#### 7. I proceed to find the mean training accuracy, and display a confusion matrix for the same.
#### 8.  F1-score, or F-measure is also mentioned here. This is also a measure of the text accuracy. 
#### 9. Now, I use a tfidf vectorizer, which converts a collection of raw documents to TF-IDF features. You will notice that i have not used a count Vectorizer here. If i do use a count Vectorizer followed by TFIDF transformer instead, this step can be replaced with that.
#### 10. Keras Tokenize. {fit_on_texts} Updates internal vocabulary based on a list of texts. {texts_to_sequences} Transforms each text in texts to a sequence of integers. and finally, {pad_sequences} to tranform a list of sequences into a 2D array. 
#### 11. Next, i create a sequential model. It's preferred when each layer has exactly one input tensor and one output tensor, as is required by the problem statement.
#### 12. Now i use .fit() to fit my model to the training data. I have run it through 15 epochs, which essentially means the number of times that the learning algorithm will work through the entire training dataset(which is 15 times)
#### 13. Finally, I perform step 8 again, this time taking X_val in consideration. I get my classification report.
#### 14. Don't forget to use .argmax(val_preds,axis=1) after defining val_preds. It's a 2D array, and it throws a Classification metrics can't handle a mix of multiclass and continuous-multioutput targets error.
#### 15. This commences the solution to the problem statement.
