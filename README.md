<<<<<<< HEAD
## Machine Learning Model
We are using a binary classification model to predict the outcome of the bank telemarketing campaign. We will look at multiple different models to evaluate what model gives us the most accuracy as well as a realistic running time. The data will be cleaned using a OneHotEncoder method so that we have entirely numerical data to work with.
=======
# The Success of Bank Telemarketing
## First Segment
### Overview
In the first segment, you'll work with your project team and begin assigning roles and tasks. You'll also choose the type of data you'll work with. There are many different avenues for this, so remember not to get too bogged down in making this decision.
### Purpose
By the end of this module, you will have created the foundation for your final project. By defining roles between your team members and establishing a communication structure beforehand, you'll already be off to a great start. Additionally, you'll complete the following tasks:
	- Decide on a topic for the project—think of a question that can be answered using data.
 	- Create a repository for the project and invite the other team members to join.
 	- Source a dataset that will suit your needs (you can even use multiple datasets if applicable).
 	- Begin to clean, organize, and perform exploratory data analysis on your datasets so that they're ready for analysis.
 	- Include mockups of a machine learning model and a database.
### Result
#### Roles
1. Square (Duc Thach)  
	- Created a main repository that include README.md
	- Maintain the github repository
2. Triangle (Michael Dicky)
	- Work on machine learning role
	- Updating/maintain machine learning branch
3. Circle (Almir Omerdic)
	- Work on database role
	- Updating/maitain database branch
4. X (Paul Erickson)
	- Work on Dashboard role
	- Updating/maintain dashboard branch 
#### Communication
- Slack
- Discord
- Github	
#### Topic
- We picked "The Success of Bank Telemarketing" as our topic
#### Reason for selecting the topic
- This dataset could be used to predict the success of a marketing campaign, to identify which customers are most likely to respond positively to a marketing campaign, or to determine which marketing strategies are most effective.
#### Questions that hope to answer
- Would bank telemarketing work on you?
#### Data Source
- https://www.kaggle.com/datasets/satoshidatamoto/the-success-of-bank-telemarketinge?select=bank-additional-full.csv
- The data set contains information on direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. In order to assess whether or not the product (bank term deposit) would be subscribed, often more than one contact to the same client was required.  
- There are four datasets in total: bank-additional-full.csv (41188 examples with 20 inputs), bank-additional.csv (10% of the examples with 20 inputs), bank-full.csv (all examples with 17 inputs), and bank.csv (10% of the examples with 17 inputs). The classification goal is to predict if a client will subscribe (yes/no) to a term deposit, based on the input variables available.  
- Attribute Information: Input variables include age, job type, marital status, education, credit in default?, housing loan?, personal loan?, last contact communication type, last contact month of year, last contact day of week, last contact duration in seconds, number of contacts performed during this campaign and for this client, number of days that passed by after the client was last contacted from a previous campaign, number of contacts performed before this campaign and for this client , outcome of the previous marketing campaign , employment variation rate - quarterly indicator , consumer price index - monthly indicator , consumer confidence index - monthly indicator , euribor 3 month rate - daily indicator , and number of employees - quarterly indicator
- This dataset is perfect for those who want to predict the success of bank telemarketing campaigns. The data includes information on the age, job, marital status, education, default status, balance, housing status, loan status, contact information, day of week contacted, month contacted, duration of last contact, number of contacts during campaign, number of days since last previous contact outcome and success outcome (yes/no) of each client. With all of this data available to you , you can create a model that accurately predicts whether or not a potential client will subscribe to a term deposit.
#### Machine Learning Model
- We are using a binary classification model to predict the outcome of the bank telemarketing campaign. We will look at multiple different models to evaluate what model gives us the most accuracy as well as a realistic running time. The data will be cleaned using a OneHotEncoder method so that we have entirely numerical data to work with.
#### Database Integration
- Cleaned data for PGAdmin ready to start creating tables. Removed index row, removed quotations from each row.
#### Dashboard  	
>>>>>>> 69f8cb0cfa82130626736168793fd4274b5dc852
