# Lab Instructions

Lucky Shrub is a medium-sized garden design firm that sells indoor and outdoor plants, making them a one stop shop for clients. In this lab, you must complete a series of tasks to help Lucky Shrub access relevant data from the Orders table in their database using stored procedures.

The Orders table contains information about the Order ID, Client ID, Product ID, Quantity and Cost as shown in the following screenshot.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/57fff631-9427-4151-8014-d6855f33f072)


# Prerequisites

To complete this lab, you must have the Lucky Shrub database created in MySQL. You must also have created and populated the Orders table with relevant data in the Lucky Shrub database.

If you have not created these tables and the database, the required code is as follows:

1: Create database
```SQL
CREATE DATABASE Lucky_Shrub;
```
2: Use database

```SQL
USE Lucky_Shrub;
```
3: Create Orders table

```SQL
CREATE TABLE Orders (OrderID INT, ClientID VARCHAR(10), ProductID VARCHAR(10), Quantity INT, Cost DECIMAL(6, 2));
```
4: Insert data

```SQL
INSERT INTO Orders (OrderID, ClientID, ProductID , Quantity, Cost) VALUES (1, "Cl1", "P1", 10, 500), (2, "Cl2", "P2", 5, 100), (3, "Cl3", "P3", 20, 800), (4, "Cl4", "P4", 15, 150), (5, "Cl3", "P3", 10, 450), (6, "Cl2", "P2", 5, 800), (7, "Cl1", "P4", 22, 1200), (8, "Cl1", "P1", 15, 150);
```
There are two main objectives in this activity:

1. Create stored procedures with empty parameters.

2. Create stored procedures with two parameters.

Tasks Instructions

Please complete the following tasks.

Task 1: Write a SQL statement that creates a stored procedure called 'GetOrdersData' which retrieves all data from the Orders table.

After executing the query, call the “GetOrdersData” to show all orders on the MySQL terminal. The expected output of the call statement should be the same as the following screenshot (assuming that you have created and populated the table correctly).

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/5b1b0de3-c058-45c3-9f23-9a05ad58517e)


Task 2: Write a SQL statement that creates a stored procedure called “GetListOfOrdersInRange”. The procedure must contain two parameters that determine the range of retrieved data based on the user input of two cost values “MinimumValue” and “MaximumValue”.

Once you have executed the query, call the “GetListOfOrdersInRange” to display the data of orders that cost between $150 and $600. The expected output of the call statement should be the same as the following screenshot (assuming that you have created and populated the table correctly).

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/7acc1422-be41-44e7-8126-4f20c2df714b)


Once you have completed these tasks, check and compare your answers against the solutions.

# Solution

Once you have completed these tasks, you can check your answers against the solutions.

Task 1 solution: Write a SQL statement that creates a stored procedure called 'GetOrdersData', which retrieves all data from the Orders table.

The GetOrdersData SQL procedure syntax.
```SQL
CREATE PROCEDURE GetOrdersData ()  SELECT * FROM Orders;
```

To call the GetOrdersData procedure write the following syntax.  
```SQL
CALL GetOrdersData();
```

Task 2 solution: Write SQL statement that creates a stored procedure called “GetListOfOrdersInRange”. The procedure must contain two parameters that determine the range of retrieved data based on the user input of two cost values “MinimumValue” and “MaximumValue”.

The syntax for the GetListOfOrdersInRange prodedure is as follows:
```SQL
CREATE PROCEDURE GetListOfOrdersInRange (MinimumValue DECIMAL, MaximumValue DECIMAL) SELECT * FROM Orders WHERE Cost >= MinimumValue AND Cost <= MaximumValue;
```

Write the following syntax to call the GetListOfOrdersInRange procedure.  
```SQL
CALL GetListOfOrdersInRange (150, 600);
```


