Goal

The goal of this exercise is for you to learn how to work with string values in a database. The objective is to allow you to practice working with string data types in SQL. This exercise focuses on the two most used string datatypes in SQL: CHAR and VARCHAR.

Scenario

Mr. Carl Merkel owns a small business that sells mobile devices called “CM Mobiles”. He wants to create a new table to store key information about customers including customer username, customer full name and customer email address as shown in the following table of data. 

Customer Table:
![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/10ae3560-6284-40a7-902b-6d2839e81f9f)


Instructions

Please attempt the below tasks before you continue, so you can check and compare your answers with our solution.

Create a SQL statement with relevant attributes and data types as follows:

1.      Identify a suitable name for the table in which you want to store data about mobile devices.  

2.      Identify the data type for each column of the table.

3.      Write a complete SQL statement to create the table inside the cm_devices database.


Creating the table

1.  When you create a table in a database, you need to identify a suitable name. In this case, you can call it "customers". 

2.  Based on 'CM Mobiles' requirements the customers table will have three columns: 

●	username 
●	full name 
●	email address

3.  The customer username contains alphanumeric values such as: Custom001, Custom002, and Custom003. Notice here that the username is always nine characters in length, so choose the CHAR datatype as it allows for a fixed length of characters. In this case, choose 9 characters, no more or less. Therefore you can declare the username in the SQL statement using the following SQL syntax:

username CHAR(9)

4.  The full name and email address must be more flexible in terms of the length as they can vary from one customer to another. So choose the VARCHAR datatype and define the maximum length expected for each value. Declare these two columns in SQL as follows:

fullname VARCHAR (100)

5.  This means the full name value would be a string of maximum 100 characters. Similarly, you can define the email address in SQL as:

email VARCHAR(255)

This means the maximum length of the email will be 255 characters.  

If you still have any doubts about the difference between CHAR and VARCHAR, please watch the video about string datatypes.


Note: You need to have a database to create the table inside of it. If you don’t have one yet, create the CM Mobiles database as follows.


1.	Type the following SQL statement inside the SQL terminal editor in the Coursera platform.
```
CREATE DATABASE cm_devices;
```
2.	Press Enter to execute the CREATE DATABASE statement.

3.	Make sure you select the database in order to use it by typing the following SQL statement.
```
USE cm_devices;
```
Press Enter to execute the query. The output result: “Database changed” is displayed in the terminal section. 
![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/43efc98b-990b-4752-92f8-8388ed3b5b20)


Now let’s write the SQL statement to create the customers table in the database. 

SQL statement

1.      Write CREATE TABLE command followed by the name of the table (customers in this case).

2.      Open parenthesis to define the table columns including username, full name and email. 

3.      Assign each column a suitable datatype as described earlier. 

4.      Add a closing parenthesis and a semi-colon at the end of the SQL statement. The complete SQL statement is shown below. 
```
CREATE TABLE customers (username CHAR(9), fullName VARCHAR(100), email VARCHAR(255)); 
```
5.      Execute the query by pressing enter.

If you have followed all the steps correctly, you should now be able to see the customers table created inside the cm_devices database by typing:

SHOW tables;

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/49be597c-696f-4a57-a3ad-a7dcd8429038)


Press enter to execute the query. The output displays all tables existing in the “cm_devices” database.

Well done! You have correctly defined the string data types and created the customer table.

If you want to check the structure of the customers table type the following SQL statement and press Enter.
```
SHOW columns FROM customers; 
```
This will show you all the customers table columns and data types.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/5964785c-d2ea-4ed1-8961-92634f6cbc36)


There are other SQL string data types that work like VARCHAR with varied sizes of lengths of characters. For example, the “TEXT” data type can be used to define columns requiring less than 65535 characters. This data type could be used to store text content like an article.

In this exercise, you have practiced how to define string datatypes in a database. Here is an additional task for you to test your skills.


Additional task

Mr. Carl Merkel wants to create another basic table in the cm_devices database to store the customers' feedback. This table must include three columns:

●	Feedback ID column,
●	Feedback type column with a maximum of 100 characters, 
●	A comment column with a maximum of 500 characters. 

The feedback table is illustrated below.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/3dfd8cbb-5466-454b-85b8-e679d46e973b)


You are required to complete the following tasks:

A. Declare the columns with the right data type for each. 

B. Write the SQL statement that creates the feedback table.

Solution:

A:  Feedback id: CHAR(8)

      Category: VARCHAR(100)

      Comment:  TEXT(500)  

B:  
```
CREATE TABLE feedback(feedbackID CHAR(8), feedbackType VARCHAR(100), comment TEXT(500));
```
