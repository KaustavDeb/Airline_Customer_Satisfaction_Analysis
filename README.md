# Spam-Mail-Analysis-using-Decision-Tree
<h3> Domain</h3>
Linguistics</br>
<h3>AIM:</h3>
To predict whether a given SMS is a spam message or not.</br>
Data link : kaggle datasets download -d uciml/sms-spam-collection-dataset </br>
<h3>Software used</h3>
Python</br>
<h3> Content</h3>
The SMS Spam Collection is a set of SMS tagged messages that have been collected for SMS Spam research. It contains one set of SMS messages in English of 5,574 messages, tagged acording being ham (legitimate) or spam </br>
<h3>Data Description</h3>
The dataset has 5169 rows and 4 columns (2 of which are meaningless).</br>
<h3>Dataset Attributes</h3>
The dataset has 2 columns :</br>
v1: Contains the label of the SMS(ham or spam).</br>
v2: Contains the raw text. </br>
<h3>Statistical Techniques</h3>
At first we import the CSV file and store it in a dataframe. We drop the last two unnamed columns as they do not contain any data. We rename the columns as 'spam' and 'Messages'. We then use the LabelEncoder class to encode the 'spam' column : 1 if the text is classified as 'spam' and 0 if it is classified as 'ham' (not a spam text). To fit a Decision Tree, we need to convert our text messages from String format to numeric format. CountVectorizer is a great tool provided by the scikit-learn library in Python. It is used to transform a given text into a vector on the basis of the frequency (count) of each word that occurs in the entire text. This is helpful when we have multiple such texts, and we wish to convert each word in each text into vectors (for using in further text analysis).</br>
After converting the Messages into vectors, we use train_test_split (available in sklearn.model_selection) to split our dataset into training (used to train the model) and testing (used to check the goodness-of-fit of the model) datasets. A test size of 20% is used in this case. We use DecisionTreeClassifier available in sklearn.tree to fit our model and then used the score() function to test the goodness of fit. To check if our accuracy can be increased, we generate a set of ccp_alpha values for our dataset and then plot the model accuracy corresponding to each alpha value to see for which ccp_alpha value, our model attains the highest accuracy. </br>
