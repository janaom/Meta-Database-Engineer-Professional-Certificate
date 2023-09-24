Goal

The goal of this exercise is to teach you how to delete records. You will have the opportunity to practice deleting a record from a table in a database.

Scenario

Mr. John Ericson owns a small bookshop. His bookshop database includes a “Customers” table that contains the bookshop’s customers’ details. The image below displays all records of data stored in the customers’ table.
![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/69311e80-4559-4c75-8f0b-d0794dab8372)


Mr. Ericson wants to remove the customer record of Jimmy with ID number 3.
The steps below will guide you through the process for deleting Jimmy’s record from the bookshop database

Instructions

Please attempt the tasks below before you continue so you can check and compare your answers with the solution.

You are expected to have the bookshop database and the customers table created in a previous exercise. 

You need to populate the customers table with relevant data to complete this exercise.

However, before you copy and paste this code, make sure you empty the table to avoid duplication of records.

Type the following SQL statement:
```
TRUNCATE TABLE customers;
```
Then copy and paste the following SQL statement into the SQL terminal section. 
```
INSERT INTO 'customers' ('customerID', 'customerName', 'customerAddress') VALUES
(1, 'Jack', '115 Old street Belfast'),
(2, 'James', '24 Carlson Rd London'),
(4, 'Maria', '5 Fredrik Rd, Bedford'),
(5, 'Jade', '10 Copland Ave Portsmouth '),
(6, 'Yasmine', '15 Fredrik Rd, Bedford'),
(3, 'Jimmy', '110 Copland Ave Portsmouth');
```
Write a SQL statement to delete Jimmy’s record from the customers table. 

Select the database in order to use it by typing the following SQL statement.
```
USE bookshop;
```
Press Enter.

Write the SQL statement to delete the customer.

1. Write the “DELETE” command, followed by the FROM keyword to identify the source table containing the records. In this case, the table name is called “customers” table.

2. Write the WHERE clause followed by the condition to specify the record you want to delete. The condition should be WHERE customerID = 3. The full syntax is as follows: 
```
DELETE FROM customers WHERE customerID = 3;
```
Execute the query by pressing the Enter button on the keyboard. The SQL statement is executed, and Jimmy's record is deleted from the bookshop database.

To view the content of the customers table after deleting the record, you can type the following select statement:

This statement displays all data that exists in the customer table.
![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/9c1ab860-40c9-4297-99ef-6958b233f735)



Notice that the customer record with ID 3 has been removed from the bookshop database. 

In this exercise, you have practiced how to delete a record of data from the database using SQL DELETE command. 

Additional task (optional)

Mr. Ericson wants to delete the record of Yasmine. Your task now is to remove this customer's details from the customer table.

Hint: you should use the SQL "DELETE" command.
