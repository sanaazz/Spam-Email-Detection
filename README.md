# Spam Email Detection

## Dataset
A dataset composed of 5172 real emails [Email](https://www.kaggle.com/balaka18/email-spam-classification-dataset-csv) is used. Each of these emails are labeled as spam (1) or not spam (0). The dataset is already preprocessed such that each column indicates the number of occurrences of a given word for a given email instance. As a preprocessing stage, we dropped the column indicating instance numbers as they have no use. Additionally, data labels (indicating whether the mail is spam or not spam) are given as a separate file.
The dataset has been split into two subsets: a 4137-email subset for training and 1035-email subset for testing. For this task, we treat test set as a validation set and assume that there is another dataset that is not provided to you as a test set. we report the model that performs best on this given validation set. To prevent any bias occurring from the order of the samples, the train-test split has been performed after shuffling the data.
Using the word frequencies, data files are generated. we use the following files:
* x_train.csv
* y_train.csv
* x_test.csv
* y_test.csv
The files that start with x contain the features and the files starting with y contain the ground truth labels.
In the data files generated, each row contains a feature vector specifying the occurrences of vocabulary words. The jth element of the feature vector given in row i indicates the number of occurrences of jth word of the vocabulary in the ith email. There are 3000 words in vocabulary, representing the most common 3000 words in all emails. For the labels, spam and not spam information is represented by a binary label (label 1 for spam mail, label 0 for a non-spam mail). In the dataset, there are no missing values both in feature vectors and data labels.
In the csv files provided, the data is organized in a tabular form. This means that we can access the vocabulary from the index row of files containing the feature vectors (x_train.csv and x_test.csv). To scan the data files and perform vectorized operations, we use external libraries (such as Pandas and NumPy libraries for Python).

##  Bag-of-Words Representation

Recall the bag-of-words document representation makes the assumption that the probability that a word appears in an e-mail is conditionally independent of the word position given the class of the e-mail.

## Coding
 in this script we implement the Bag-of-Words with two Models.
 
 * Multinomial Naive Bayes Model
 * Bernoulli Naive Bayes Model
