# Crowfunding-ETL

## Overview

We have been helping Independent Funding, which is a crowdfunding platform for funding independent projects or ventures that has been growing, so now it needs to move all their accessible data from one large Excel file onto a PostgreSQL database. This way, the analytics team will be able to perform analysis and create reports for company stakeholders as well as individuals who donate to projects.

Now, for this project we’ve been asked to perform both an ETL process and a data analysis by using SQL queries from a new dataset that contains information about the backers who’ve pledged to the live projects.

We used Python, Pandas, and Jupyter notebooks to do the extract and transform phases. Specifically, we extracted and transformed the backers’ contact information from a CSV file to create a DataFrame that was exported as a CSV file. Then we used the dataset to create an ERD and a table schema for creating a new table in the crowdfunding database. And we uploaded the CSV file that contains the backers’ information into this table. Finally, performed a data analysis on the crowdfunding database by using SQL queries.

## Analysis and Results

First we used Python, Pandas and jupyter notebook for the extraction of the data, and with the help of Python dictionary methods we created a Data Frame and exported to the Backers.csv file.

<img width="223" alt="Backers_before_cleaned" src="https://user-images.githubusercontent.com/113747210/202513165-7fe8122f-fa77-4844-b7d6-1930ccdce339.png">

For the step two we transformed and cleaned the data via formatting, splitting, converting data types, and restructuring to create a DataFrame that can be loaded into a postgreSQL database as a CSV file.

<img width="297" alt="backers_transformed" src="https://user-images.githubusercontent.com/113747210/202513242-6a62c95c-a1f2-4d42-ade2-2ec3d0d816d9.png">

Then we used ERD to connect our tables and through pgAdmin we created a new table named Backers with the information from our backers.csv file.

![crowfunding_db_relationships](https://user-images.githubusercontent.com/113747210/202513330-c0260eaf-a23f-4cde-bbc1-3129cdeb4450.png)

Finally with our information from the backers we could perform an analysis writing the following queries:

•	One that retrieved the number of backer counts in descending order for each cf_id for all the live campaigns.

•	A query that creates a new table named “email contacts remaining goal amount” that contains the first name of each contact, the last name, the email address, and the remaining goal amount (as "Remaining Goal Amount") in descending order for each live campaign. And exported the table to a csv file.

<img width="335" alt="email_remaining_goal_amount" src="https://user-images.githubusercontent.com/113747210/202513448-fec99e0b-9799-431e-beac-d39f97bbe3cc.png">

•	A query that creates a new table named “email backers remaining goal amount” that contains the email addresses of the backers in descending order, the first and the last name of each backer, the cf_id, the company name, the description, the end date of the campaign, and the remaining amount of the campaign goal as "Left of Goal". Also we exported the table into a csv file.

<img width="442" alt="email_backers_left_to_goal" src="https://user-images.githubusercontent.com/113747210/202513523-23751003-6b00-4526-b5dd-391be07fa7d2.png">

## Summary
With the help of SQL, we were able to help Independent Funding to perform a data analysis on their growing database, between our knowledge of Python, Pandas and SQL queries we managed to work with a large dataset, extract it, transform it and clean it to made the job easier and faster.


