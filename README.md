# The Success of Bank Telemarketing
## Second Segment
### Overview
In this segment, building the separate pieces that will make the project great—and also start putting them together! Selecting data and started exploring it for analysis. Also, prepareing a mockup of a machine learning model and fabricated a database in anticipation of the next step. This is an exciting segment because starting to really see how the works are going to come together.
### Purpose
By the end of this segment, there are great strides in building the different pieces of the project. The analysis is coming along nicely, work on the machine learning model has commenced, and the database will be transitioned into an operational, data-holding tool.
### Result
#### Communication Protocols
- Database
	- A database is created with PgAdmin4
	- creating tables to populate the data with scv files
	- creating account with AWS
	- Connecting PdAdmin4 with AWS
	- Using RDS on AWS to upload and retrieve datas
- Machine Learning
	- Pulling the data from AWS that connected to PgAdmin
	- Perform the algorithm to predict the outcomes 
- Dashboard
	- Pulling the data from AWS to make visulization
	- Using outcomes from machine learning to make graphs for better displays 	
#### Project Outlines
##### Database
- Database Schema 
- PgAdmin4
	- Cleaned data for PGAdmin ready to start creating tables. Removed index row, removed quotations from each row.
	- We started by creating bank_data table. With this table created we can start to load the csv file into the table.
		- ![ban_data_table](https://user-images.githubusercontent.com/33468680/170159274-85ed5819-77e5-41b6-bf5f-e0f3b4240004.png) 
	- We then created two more tables first being customer personal information and the second being the loan information and the bank account balances.  
		- ![customer_info_table](https://user-images.githubusercontent.com/33468680/170159407-66e01606-938b-4f03-a7b5-3e26d0cb8a0e.png)  
		- ![customer_loan](https://user-images.githubusercontent.com/33468680/170159451-5113aaf4-6621-460d-ba5d-cca40654095e.png)  
	- Next we devicded to split the data into 3 different csv files and sorted them by each year that the data was collected.  
		- ![bank_data_08](https://user-images.githubusercontent.com/33468680/170159620-212f63d4-9780-4159-a165-c9bff2a914a6.png)
		- ![bank_data_09](https://user-images.githubusercontent.com/33468680/170159671-691f5464-1754-43a2-ba73-370b85853a5c.png)
		- ![bank_data_10](https://user-images.githubusercontent.com/33468680/170159703-209cd840-b011-4ad5-9744-4148ba6ce201.png)
- AWS
	- Created an account on AWS
	- Created a database on RDS
	- Connected RDS on AWS to PgAdmin4
	- Gave permision to other to access database
##### Machine Learning
- Machine Learning Model
We are using a binary classification model to predict the outcome of the bank telemarketing campaign. We will look at multiple different models to evaluate what model gives us the most accuracy as well as a realistic running time. The data will be cleaned using a OneHotEncoder method so that we have entirely numerical data to work with.
- Description of preliminary data preprocessing
	- For the machine learning section we performed the data preprocessing in steps as follows:
		1. look for and drop any null values
		2. look for and drop any duplicate entries
		3. Drop unnecessary columns, in this case 'index'
		4. Change columns with binary entries to Bool values 'credit_default','housing_loan','personal_loan','subscription'
		5. changes dates to a Linux timestamp data format
		6. used 'OneHotEncoder' to transform remaining string/object values into numerical format
	- We also attempted other preprocessing that did not end up making it to the final model including 
		1. 'binning' numerical data
		2. oversampling data
		3. undersampling data
		4. using a 'StandardScaler' on the data
- Description of preliminary feature engineering and preliminary feature selection  
We ended up using all features available in the information given. We looked at the feature analysis given by the Random Forests analyzer to determine significant features. We did attempt to drop columns other columns including 'pdays','previous','poutcome' but this did not have a significant impact on model performance and in fact decreased from the effectiveness of the model.
- Description of how data was split into training and testing sets  
To split the data into training and testing sets we used the built in train_test_split function of sklearn. We kept the default values of test size 25% and train size 75% of the entire dataset.
- Explanation of model choice, including limitations and benefits   
For our model we wanted the highest precision possible over a high recall. Given that there is a limited amount of time in a day we want the highest percent chance that the person we call will be a subscriber. The Random Forest Classifier gives us almost the best precision while still keeping recall, accuracy, and model run time at an adequate level.
	- Benefits: No feature scaling required.Random Forest works well with both categorical and continuous variables which our data has.
	- Limitations: Random forests can be complex and harder to understand. Random Forest require much more time to train as compared to decision trees
##### Dashboard
- Web Connector
	- Using web connector to pull the data
	- Connecting data to Tableau
- Tableau
	- Create storylines
	- Using Tableau to display the analysis
	- Showing important features 
	- Showing results from machine learning

