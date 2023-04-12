## Fake_News_Detection

Dataset: https://drive.google.com/file/d/1er9NJTLUA3qnRuyhfzuN0XUsoIC4a-_q/view
Download the required dataset from the above link

### Summary:
The given code is an implementation of fake news detection using machine learning. It involves various steps such as data cleaning, data preprocessing, feature extraction, and model training.

At first, the necessary libraries are imported such as numpy, pandas, regular expression (re), Natural Language Toolkit (nltk), stop words, Porter Stemmer, TfidfVectorizer, Logistic Regression, and accuracy score.

After importing libraries, the stop words in the English language are printed using print(stopwords.words('english')) to check the stop words which will be used later in the code.

Then the dataset is loaded using the pd.read_csv() method and the first five rows of the dataset are displayed using the head() method to get an initial overview of the dataset. The dataset is checked for null values using news_dataset.isnull().sum().

Then the data is cleaned using the stemming() function. In this function, regular expression is used to remove any characters other than the alphabets, then the text is converted to lowercase and split into words. Then the Porter Stemmer algorithm is used to convert the words into their root form, and finally, the stop words are removed from the text. The cleaned data is then assigned back to the original dataset's title column.

After cleaning the data, the data and label are separated using X = news_dataset['title'].values and Y = news_dataset['label'].values. The textual data is then converted to numerical data using TfidfVectorizer. This is done using the fit() and transform() methods of the vectorizer object. The dataset is split into training and testing data using train_test_split().

Finally, the Logistic Regression model is trained on the training data using the fit() method. The accuracy score of the training data and test data is calculated using the accuracy_score() method. The model is then used to predict the class of a new data point using model.predict().

If the predicted class is 'REAL', it is printed that the news is real, and if the predicted class is 'FAKE', it is printed that the news is fake.

Overall, the given code is a basic implementation of fake news detection using machine learning. It can be improved by using more advanced algorithms and techniques, and by using larger and more diverse datasets.
