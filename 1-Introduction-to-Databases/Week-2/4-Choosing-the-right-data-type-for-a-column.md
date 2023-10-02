# Goal

Practice how to choose suitable data types for different kinds of columns in the table

# Exercise objectives

This exercise demonstrates how to choose suitable data types for a variety of columns to store data as string, integer, date and decimal values. 

# Scenario

Mr. Carl Merkel owns a small business that sells mobile devices called “CM Mobiles” in Harrow town near London. He wants to create a database to store key information about customers’ orders in order to generate invoices for his customers including customer name, order date, quantity and total price. This data can be seen in the following invoice table: 
![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/867a489b-78c3-474b-8e8e-ea06a5aa8827)



# Instructions

Please attempt the following tasks before you continue, so you can check and compare your answers with the solution.

You are required to write ‘CREATE TABLE” SQL statement with relevant attributes and data types.

1. Identify the columns and define the data type for each column of the table. 

2. Write a complete SQL statement to create the invoices table inside the cm_devices database. 


Identifying the table columns and data types

You must design the invoice table, which consists of different types of columns that will store different types of data. As a database developer, you should choose a data type which meets the expected type of data that will be stored in the column based on the following guidelines: 

If the column is expected to store numeric data, then you need to choose a numeric data type such as INT or DECIMAL.  

If the column is expected to store alphabetic or alphanumeric data, then you need to choose a string data type such as CHAR or VARCHAR.  

If the column is expected to store date data, then you need to choose the date data type.  


Take the invoice table columns one by one and apply the previous guidelines:

1. Customer name: the string data type would be very suitable for the customer's name as we expect it to store data with alphabetic characters. In this case we can use VARCHAR as we expect to have customer names with different lengths of characters. 

2. Order date: the date data type would be very suitable for the order date as we expect it to store data with dates. 

3. Product quantity: the integer data type would be very suitable for the order quantity as we expect it to store whole numbers of data. 

4. Total price: the decimal data type would be very suitable for the product price as we expect it to store numeric data with fractions. 


Building the invoice table in SQL

Note: You need to have a database so that you can create the table inside it. If you don’t have one yet, follow the steps outlined below to create the CM Mobiles database. 

  

1. Type the following SQL statement inside the SQL terminal editor on the Coursera platform:

```SQL
CREATE DATABASE cm_devices; 
```

2. Press Enter to execute the create database statement. 

3. Make sure you select the database to use it by typing the following SQL statement and press Enter:
```SQL
USE cm_devices; 
```
![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/6111562c-46f6-4fab-ba59-7872783f6b8a)


Create the SQL statement as follows:

1. Write a SQL statement that contains the CREATE TABLE command followed by by the name of the table, which is “invoice” in this case.

2. Add an open parenthesis to define the tables columns including customer name, order date, quantity and total price.  

3. Assign each column a suitable datatype as described earlier. 

4. Add a closing parenthesis and a semi-colon to the end of the SQL statement as follows: 

```SQL
CREATE TABLE invoice (customerName VARCHAR(50), orderDate DATE, quantity INT, price DECIMAL); 
```

Press Enter to execute the query

If you have followed all the steps correctly, you should now be able to see the invoices table created inside the cm_devices database by typing:
```SQL
SHOW tables;
```
Press Enter to execute the query. The output result shows the tables within the cm_devices database. 
![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/0ddcaf7f-5c59-4e16-9bef-98b380c1520f)


If you want to check the structure of the invoices table, type the following SQL statement and press Enter.
```SQL
SHOW columns FROM invoice; 
```
This statement displays the invoice table structure.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/3a8f6014-b30e-4dc9-91b1-eb6ba0079faf)


![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/cb87d109-512f-4d3a-b4b5-4d00984d4820)



In this exercise, you have learned how to choose suitable data types for a variety of columns.

Here is an optional additional task for you to test your skills.


Additional task (optional)

Mr. Carl needs to have a new table to store the contact details of each customer including customer account number, customer phone number and customer email address. 

You are required to choose a relevant data type for each of the columns.  

# Solution:

Account number: INTEGER

Phone number: INTEGER

Email: VARCHAR  
