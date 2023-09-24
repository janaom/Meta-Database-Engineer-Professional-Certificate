Lab Instructions
Lucky Shrub is a medium-sized garden design firm that sells indoor and outdoor plants, making them a one stop shop for clients. In this lab, you are going to complete the following tasks to make it easier for Lucky Shrub staff to print relevant order data on the screen.

The Orders table contains information about the Order ID, Client ID, Product ID, Quantity and Cost as shown below.

Prerequisites

To complete this lab, you must have the Lucky Shrub database created in MySQL. Also, you must have the Orders table created and populated with relevant data inside Lucky Shrub.

The code to create the database and the Orders table is listed below.

1: Create database
```
CREATE DATABASE IF NOT EXISTS Lucky_Shrub;
```
2: Use database
```
USE Lucky_Shrub;
```
3: Create Orders table
```
CREATE TABLE Orders (OrderID INT NOT NULL PRIMARY KEY, ClientID VARCHAR(10),  ProductID VARCHAR(10),  Quantity   INT, Cost DECIMAL(6,2));
```
4: Insert data
```
INSERT INTO Orders (OrderID, ClientID, ProductID , Quantity, Cost) VALUES (1, "Cl1", "P1", 10, 500), (2, "Cl2", "P2", 5, 100), (3, "Cl3", "P3", 20, 800), (4, "Cl4", "P4", 15, 150), (5, "Cl3", "P3", 10, 450), (6, "Cl2", "P2", 5, 800), (7, "Cl1", "P4", 22, 1200), (8, "Cl3", "P1", 15, 150), (9, "Cl1", "P1", 10, 500), (10, "Cl2", "P2", 5, 100);
```

This activity aims to achieve the following objective:

Filtering data using WHERE clause and logical operators.

Tasks Instructions
Please attempt the following tasks:

Task 1: Write a SQL statement to print all records of orders where the cost is $250 or less. The expected output result should be the same as the following screenshot (assuming that you have populated the Orders table with the same data set)

Task 2: Write a SQL statement to print all records of orders where the cost is between $50 and $750. The expected output result should be the same as the following screenshot (assuming that you have populated the orders table with the same data set)

Task 3: Write a SQL statement to print all records of orders that have been placed by the client with the id of Cl3 and where the cost of the order is more than $100. The expected output result should be the same as the following screenshot (assuming that you have populated the Orders table with the same data set)

Task 4: Write a SQL statement to print all records of orders that have a product id of p1 or p2 and the order quantity is more than 2. The expected output result should be the same as the following screenshot (assuming that you have populated the Orders table with the same data set)


