# The Success of Bank Telemarketing

Cleaned data for PGAdmin ready to start creating tables. Removed index row, removed quotations from each row. 

We started by creating bank_data table. With this table created we can start to load the csv file into the table. 

![CODE1](Images/bank_data_table.png)



We then created two more tables first being customer personal information and the second being the loan information and the bank account balances. 

![CODE1](Images/customer_info.png)

![CODE1](Images/customer_loan_table.png)

Next we devicded to split the data into 3 different csv files and sorted them by each year that the data was collected. 

![CODE1](Images/bank_data_08.png)

![CODE1](Images/bank_data_09.png)

![CODE1](Images/bank_data_10.png)

We created an ERD database to identify our primary key. And also give us an idea what would connect our databses for the inner join table. 

![CODE1](Images/QuickDBD-export.png)


Next we created a table called customer_data. This is where we did the inner join of the data that only pretains to the customer. 

![CODE1](Images/inner_join_data.png)

![CODE1](Images/inner_join_table.png)


We linked all of our data using amazon RDS. The reason behind using RDS was to make it easier for rest of the team to be able to access all the data tables that were created in the PgAdmin. We have looked at different options but RDS seemd more user friendly and it gave everyone a chance to get more practice with it. 


