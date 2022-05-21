## Machine Learning Model
We are using a binary classification model to predict the outcome of the bank telemarketing campaign. We will look at multiple different models to evaluate what model gives us the most accuracy as well as a realistic running time. The data will be cleaned using a OneHotEncoder method so that we have entirely numerical data to work with.

## Description of preliminary data preprocessing
For the machine learning section we performed the data preprocessing in steps as follows.
1. look for and drop any null values
2. look for and drop any duplicate entries
3. Drop unnecessary columns, in this case 'index'
4. Change columns with binary entries to Bool values 'credit_default','housing_loan','personal_loan','subscription'
5. changes dates to a Linux timestamp data format
6. used 'OneHotEncoder' to transform remaining string/object values into numerical format

* We also attempted other preprocessing that did not end up making it to the final model including 
1. 'binning' numerical data
2. oversampling data
3. undersampling data
4. using a 'StandardScaler' on the data

## Description of preliminary feature engineering and preliminary feature selection
We ended up using all features available in the information given. We looked at the feature analysis given by the Random Forests analyzer to determine significant features. We did attempt to drop columns other columns including 'pdays','previous','poutcome' but this did not have a significant impact on model performance and in fact decreased from the effectiveness of the model.

## Description of how data was split into training and testing sets
To split the data into training and testing sets we used the built in train_test_split function of sklearn. We kept the default values of test size 25% and train size 75% of the entire dataset.

## Explanation of model choice, including limitations and benefits
For our model we wanted the highest precision possible over a high recall. Given that there is a limited amount of time in a day we want the highest percent chance that the person we call will be a subscriber. The Random Forest Classifier gives us almost the best precision while still keeping recall, accuracy, and model run time at an adequate level.

Benefits: No feature scaling required.Random Forest works well with both categorical and continuous variables which our data has.

Limitations: Random forests can be complex and harder to understand. Random Forest require much more time to train as compared to decision trees
