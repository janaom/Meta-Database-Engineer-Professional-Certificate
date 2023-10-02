# Goal 

The goal of this exercise is for you to learn how to use the SQL ORDER BY and WHERE clauses to sort and filter data.


# Objectives  

1. Use the SQL ORDER BY clause to sort the result of a query  

2. Use the SQL WHERE clause to specify a condition for records filtering


The chinook database example 

In this exercise we are going to consider the well-known “chinook sample” database, which is widely used for demos and testing purposes. Also, it has been implemented in coursera platform, which is good to be familiar with as you are going to use it to complete this exercise.

The chinook sample database consists of the following database schema.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/eb698c03-ab99-41dd-b6c9-aced5c06d52a)


Before you start:

To complete this exercise you need to do the following steps first to setup the Chinook database and create the Customer table.


1. Create the chinook database and use it in MySQL terminal.
```SQL
CREATE DATABASE Chinook;
```
```SQL
USE Chinook;
```

2. Create the customer table as follows (Copy and paste the code in the terminal):

```SQL
CREATE TABLE Customer (CustomerId INT NOT NULL, FirstName VARCHAR(40) NOT NULL, LastName VARCHAR(20) NOT NULL, Company VARCHAR(80), Address VARCHAR(70), City VARCHAR(40), State VARCHAR(40), Country VARCHAR(40), PostalCode VARCHAR(10), Phone VARCHAR(24), Fax VARCHAR(24), Email VARCHAR(60) NOT NULL, SupportRepId INT, CONSTRAINT PK_Customer PRIMARY KEY (CustomerId));
```

3. Insert the following records of data into the Customer table (Copy and paste code into the terminal):

```SQL
INSERT INTO Customer (CustomerId, FirstName, LastName, Company, Address, City, State, Country, PostalCode, Phone, Fax, Email, SupportRepId) VALUES (1, 'Luís', 'Gonçalves', 'Embraer - Empresa Brasileira de Aeronáutica S.A.', 'Av. Brigadeiro Faria Lima, 2170', 'São José dos Campos', 'SP', 'Brazil', '12227-000', '+55 (12) 3923-5555', '+55 (12) 3923-5566', 'luisg@embraer.com.br', 3);


INSERT INTO Customer (CustomerId, FirstName, LastName, Company, Address, City, State, Country, PostalCode, Phone, Fax, Email, SupportRepId) VALUES (2, 'Eduardo', 'Martins', 'Woodstock Discos', 'Rua Dr. Falcão Filho, 155', 'São Paulo', 'SP', 'Brazil', '01007-010', '+55 (11) 3033-5446', '+55 (11) 3033-4564', 'eduardo@woodstock.com.br', 4);


INSERT INTO Customer (CustomerId, FirstName, LastName, Company, Address, City, State, Country, PostalCode, Phone, Fax, Email, SupportRepId) VALUES
(3, 'Alexandre', 'Rocha', 'Banco do Brasil S.A.', 'Av. Paulista, 2022', 'São Paulo', 'SP', 'Brazil', '01310-200', '+55 (11) 3055-3278', '+55 (11) 3055-8131', 'alero@uol.com.br', 5);


INSERT INTO Customer (CustomerId, FirstName, LastName, Company, Address, City, State, Country, PostalCode, Phone, Fax, Email, SupportRepId) VALUES
(4, 'Roberto', 'Almeida', 'Riotur', 'Praça Pio X, 119', 'Rio de Janeiro', 'RJ', 'Brazil', '20040-020', '+55 (21) 2271-7000', '+55 (21) 2271-7070', 'roberto.almeida@riotur.gov.br', 3);


INSERT INTO Customer (CustomerId, FirstName, LastName, Company, Address, City, State, Country, PostalCode, Phone, Fax, Email, SupportRepId) VALUES (5, 'Mark', 'Philips', 'Telus', '8210 111 ST NW', 'Edmonton', 'AB', 'Canada', 'T6G 2C7', '+1 (780) 434-4554', '+1 (780) 434-5565', 'mphilips12@shaw.ca', 5);


INSERT INTO Customer (CustomerId, FirstName, LastName, Company, Address, City, State, Country, PostalCode, Phone, Fax, Email, SupportRepId) VALUES (6, 'Jennifer', 'Peterson', 'Rogers Canada', '700 W Pender Street', 'Vancouver', 'BC', 'Canada', 'V6C 1G8', '+1 (604) 688-2255', '+1 (604) 688-8756', 'jenniferp@rogers.ca', 3); 
```

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/40fd83a8-0200-4224-8dd4-1f21102eb15d)


Instructions 

Please attempt the following tasks before you continue, so that you can check and compare your answers with our solution. 

Task 1: Write a SQL statement to display all data existing in the customer table.  

Task 2: Write a SQL statement to sort the result set in ascending order by first name.   

Task 3: Filter the result set data based on a condition where country = France. 

 

Task 1: Display data in customer table 


Before you start sorting and filtering data, let’s display some of the customer data content that already exists in the database. This can be done by writing the following SELECT statement, which retrieves all data from the customer table. 
```SQL     
SELECT CustomerID, FirstName, LastName, City, State, Country FROM Customer;
```
Press Enter to execute the query.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/aeba5c8e-2281-4b31-944f-9f2fe25b52f9)
 

You will now see loads of data about customers displayed on the screen, which makes it hard to find relevant data about specific customers.


Task 2: Sort the result set of data 

You can make it easier for the users of the database to find relevant customers by sorting the data. For example, you can sort the data alphabetically from A-Z by using the customers' first names. This can be done by adding the ORDER BY clause to the previous SQL statement as follows.
```SQL
SELECT CustomerID, FirstName, LastName, City, State, Country 
FROM Customer 
ORDER BY FirstName;
```

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/acfba441-f66c-4f10-8105-41b87fb4ba6e)


Notice now that all data from the "customer" table is displayed again. However, the data is now sorted by the "First Name" column in Alphabetical order from A to Z.  This makes it easier for the users of the database to find the customers they are looking for.


Task 3: Filter the result set of data 

You can make it even easier for users to find specific customers by filtering data based on some criteria. For example, extracting a list of customers that come from a specific country.

In this case, you can add the condition to the previous SQL statement using the "WHERE" clause as shown below and pressing Enter to execute the query.  
```SQL
SELECT * 
FROM Customer 
WHERE Country = "Canada"; 
```
The output result of the SQL statement displays all customers from Canada only.  

To make it even better, you can display all customers in Canada with the Alphabetical order from A to Z!  

To do that, you can add the ORDER BY clause at the end of the previous SQL statement as follows: 
```SQL
SELECT * 
FROM Customer  
WHERE Country = "Canada" 
 ORDER BY FirstName; 
```
The output result of the SQL statement now shows all customers from Canada with the right Alphabetical order.  

You have now learned how to sort and filter data using SQL clauses ORDER BY and WHERE.  


Additional exercise (optional) 

You are required to write a SQL statement to display only the name and the country for customers from Canada.

Once you complete the SQL statement, run the query.   


# Solution  
```SQL
SELECT FirstName, Country 
FROM Customer  
WHERE Country = "Canada"  
ORDER BY FirstName; 

+-----------+---------+ 

| FirstName | Country | 

+-----------+---------+ 

| Jennifer  | Canada  | 

| Mark  	| Canada  | 

+-----------+---------+ 
```
