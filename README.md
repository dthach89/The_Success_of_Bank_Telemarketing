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







