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
	- creating tables to populate the data with csv files
	- creating account with AWS
	- Connecting PgAdmin4 to AWS
	- Using RDS on AWS to upload and retrieve data
- Machine Learning
	- Pulling the data from RDS on AWS that connected to PgAdmin4
	- Perform the algorithm to predict the outcomes 
- Dashboard
	- Pulling the data from AWS to make visulization
	- Displaying outcomes from machine learning and showing features on Tableau 	
#### Presentation Outlines
https://docs.google.com/presentation/d/1fCTdK4WLqB_CS2L9hynQPrdZWSWE_nL8I1XASwRxQaQ/edit?usp=sharing  

#### Project Outlines
##### Database
- Database Schema
	- We created an ERD database to identify our primary key. And also give us an idea what would connect our databses for the inner join table.
	- ![QuickDBD-export](https://user-images.githubusercontent.com/33468680/170830252-7aacdd63-4850-443c-9c52-3f17bd55a54c.png)     
- Database stores static data:
	- PgAdmin4
		- We use PgAdmin4 to store our data   
		- Cleaned data for PGAdmin ready to start creating tables. Removed index row, removed quotations from each row.
		- We started by creating bank_data table. With this table created we can start to load the csv file into the table.
			- ![ban_data_table](https://user-images.githubusercontent.com/33468680/170159274-85ed5819-77e5-41b6-bf5f-e0f3b4240004.png)
			- ![bank_data](https://user-images.githubusercontent.com/33468680/170831083-08e9e6d1-b2fd-4566-bd6e-084d2386250b.png)  
		- We then created two more tables first being customer personal information and the second being the loan information and the bank account balances.  
			- ![customer_info_table](https://user-images.githubusercontent.com/33468680/170159407-66e01606-938b-4f03-a7b5-3e26d0cb8a0e.png)  
			- ![customer_info](https://user-images.githubusercontent.com/33468680/170831105-930b4926-942f-4721-b9f5-bf28af193fae.png)      
			-  ![customer_loan_table](https://user-images.githubusercontent.com/33468680/170831182-98679045-3d4f-4652-be23-7bdc6fa0ce52.png)  
			- ![customer_loan](https://user-images.githubusercontent.com/33468680/170831120-0b83eb61-6df6-4de1-a769-13221fc26869.png)     
		- Next we created a table called customer_data. This is where we did the inner join of the data that only pretains to the customer.
			- ![inner_join_table](https://user-images.githubusercontent.com/33468680/170831148-528eafbb-7b2b-4a0d-8114-a2de0349b62a.png)
			- ![inner_join_data](https://user-images.githubusercontent.com/33468680/170831160-78ede24a-f095-4c43-9bf0-1eab4eaadc24.png)  
	- AWS
		- Created an account on AWS
		- Created a database on RDS
		- Connected RDS on AWS to PgAdmin4
		- Gave permission to other to access database on PgAdmin4 through AWS
- Database interfaces with the project / Connection string 
	- ![image](https://user-images.githubusercontent.com/33468680/170830672-cb2dbceb-19b8-4a36-87f7-863364c2c8bd.png)

##### Machine Learning
- Machine Learning Model   
We are using a binary classification model to predict the outcome of the bank telemarketing campaign. We will look at multiple different models to evaluate what model gives us the most accuracy as well as a realistic running time. The data will be cleaned using a OneHotEncoder method so that we have entirely numerical data to work with.
- In the folder "Trial and Error", there are multiple files that show we ran through different trials on different models to select the model that fit with our project.
- The "final_model.ipynb" has the final model that we picked, how the data processing, and machine learning algorithm.  
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
- In the "Resources/Model.csv", there are confusion tables with results to use for comparing the differences to pick out the most fit model.
##### Dashboard
- Tableau storyboard
	- https://public.tableau.com/app/profile/paul.erickson/viz/Final_Project_Group_3/SuccessPie?publish=yes 
- Tools
	- Tableau
		- Create storylines
		- Using Tableau to display the analysis
		- Showing important features 
		- Showing results from machine learning
	- Jupyter Notebook
	- Pyhon
	- Excel 
- Interactive elements
	-  Dropdown or select filters on Tableau
- The dashboard visualization will include a chart for each year there was data collected, a chart to represent the totals by day of the week, a chart for the overall success, based on filter configuration, and several filter options including type of contact, housing loan status, personal loan status, credit default status, marital status, education level and job type. The filters are interactive and will update the charts appropriately.
 

