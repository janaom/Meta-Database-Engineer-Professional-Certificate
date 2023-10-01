# Lab Instructions

Lucky Shrub need to execute a series of SELECT queries against their database to retrieve information on their employees and client orders.

However, they need to optimize these queries first to make sure that they execute quickly and efficiently. They can make these queries more efficient using MySQL database optimization techniques.

In this lab, you must complete a series of tasks to help Lucky Shrub optimize their SQL SELECT statements.

The SELECT statements are to be executed against the database’s Employees and Orders tables.

Let's take a quick look at these tables and the information they contain.

The Orders table contains information about the OrderID, ClientID, Product ID, Quantity, Cost and Date of each order.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/4ae0556f-6199-4baf-a2c0-17e94e7fa0c2)


The Employees table contains information about the EmployeeID, FullName, Role, Department of each employee as shown below.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/91957a6b-1dba-40ae-b5ce-d0c5c8d96d45)


# Prerequisites

First, you must create the Lucky Shrub database in your MySQL environment. Then, you must create and populate the Orders and Employees tables with the relevant data.

The code to create the database and related tables is as follows:

1: Create the database
```SQL 
CREATE DATABASE Lucky_Shrub; 
```
2: Use the database
```SQL 
USE Lucky_Shrub;
```
3: Create the Orders table

```SQL 
CREATE TABLE Orders(OrderID INT NOT NULL, ClientID VARCHAR(10) DEFAULT NULL, ProductID VARCHAR(10) DEFAULT NULL, Quantity INT DEFAULT NULL, Cost DECIMAL(6,2) DEFAULT NULL, Date DATE DEFAULT NULL, PRIMARY KEY (OrderID)); 
```
4: Create the Employees table

```SQL 
CREATE TABLE Employees(EmployeeID INT DEFAULT NULL, FullName VARCHAR(100) DEFAULT NULL, Role VARCHAR(50) DEFAULT NULL, Department VARCHAR(255) DEFAULT NULL); 
```
5: Insert data into the Orders table

```SQL 
INSERT INTO Orders (OrderID, ClientID, ProductID , Quantity, Cost, Date)  
VALUES  
(1, "Cl1", "P1", 10, 500, "2020-09-01"), 
(2, "Cl2", "P2", 5, 100, "2020-09-05"),  
(3, "Cl3", "P3", 20, 800, "2020-09-03"),  
(4, "Cl4", "P4", 15, 150, "2020-09-07"),  
(5, "Cl3", "P3", 10, 450, "2020-09-08"),  
(6, "Cl2", "P2", 5, 800, "2020-09-09"),  
(7, "Cl1", "P4", 22, 1200, "2020-09-10"),  
(8, "Cl3", "P1", 15, 150, "2020-09-10"),  
(9, "Cl1", "P1", 10, 500, "2020-09-12"),  
(10, "Cl2", "P2", 5, 100, "2020-09-13"),  
(11, "Cl1", "P2", 15, 80, "2020-09-12"), 
(12, "Cl1", "P1", 10, 500, "2022-09-01"),  
(13, "Cl2", "P2", 5, 100, "2022-09-05"),  
(14, "Cl3", "P3", 20, 800, "2022-09-03"),  
(15, "Cl4", "P4", 15, 150, "2022-09-07"),  
(16, "Cl3", "P3", 10, 450, "2022-09-08"),  
(17, "Cl2", "P2", 5, 800, "2022-09-09"),  
(18, "Cl1", "P4", 22, 1200, "2022-09-10"),  
(19, "Cl3", "P1", 15, 150, "2022-09-10"),  
(20, "Cl1", "P1", 10, 500, "2022-09-12"),  
(21, "Cl2", "P2", 5, 100, "2022-09-13"),   
(22, "Cl2", "P1", 10, 500, "2021-09-01"),  
(23, "Cl2", "P2", 5, 100, "2021-09-05"),  
(24, "Cl3", "P3", 20, 800, "2021-09-03"),  
(25, "Cl4", "P4", 15, 150, "2021-09-07"),  
(26, "Cl1", "P3", 10, 450, "2021-09-08"),  
(27, "Cl2", "P1", 20, 1000, "2022-09-01"),  
(28, "Cl2", "P2", 10, 200, "2022-09-05"),  
(29, "Cl3", "P3", 20, 800, "2021-09-03"); 
```
5: Insert data into the Employees table

```SQL 
INSERT INTO Employees (EmployeeID, FullName,  Role, Department)  
VALUES    
(1, "Seamus Hogan", "Manager", "Management"),    
(2, "Thomas Eriksson", "Assistant ", "Sales"),   
(3, "Simon Tolo", "Executive", "Management"),   
(4, "Francesca Soffia", "Assistant  ", "Human Resources"),   
(5, "Emily Sierra", "Accountant", "Finance"),    
(6, "Greta Galkina", "Accountant", "Finance"), 
(7, "Maria Carter", "Executive", "Human Resources"), 
(8, "Rick Griffin", "Manager", "Marketing"); 
```
This activity aims to achieve the following objectives:
Apply MySQL SELECT query optimization techniques

Use indexes on a table column to enhance query performance

Tasks Instructions
Please attempt the following tasks:

Task 1
Lucky Shrub need data on client orders. They have written the following SELECT query to retrieve all data from the Orders table:
```SQL 
SELECT * FROM Orders;
```

However, the data they need is contained within the OrderID, ProductID, Quantity and Date columns. So, these are the important fields that their query must target. Targeting other columns in the table is an inefficient use of resources.

Rewrite the SELECT statement so that it is optimized.

The expected output result should be the same as the following screenshot when you execute the rewritten query.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/9f24466f-2389-4c27-9b03-5a2333cfee4c)


Task 2
Lucky Shrub need to find the order placed by the client Cl1. They have written the following query to complete this task:
```SQL 
SELECT * FROM Orders WHERE ClientID ='Cl1'; 
```
However, this query's execution plan shows that it does not use an index to perform this search, as indicated by the NULL values in possible_keys and keys columns.  

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/4052facb-a473-41cc-b8f0-563158a3a2f5)


Help Lucky Shrub to optimize this query by creating an index named IdxClientID on the required column of the Orders table. Once you have created the index, run the same SELECT statement as above with the EXPLAIN statement.

The expected output result should be the same as the following screenshot when executed:

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/d3810f45-a2b8-4f70-add2-2612d30546cc)


Task 3
Lucky Shrub have written the following SELECT query to find the details of the employee whose last name is 'Tolo'

```SQL 
SELECT * FROM Employees WHERE FullName LIKE '%Tolo'; 
```

However, there’s an index on the FullName column which the query cannot use because it contains a leading wildcard (%) in the WHERE clause condition.

The following steps can be taken to eliminate the leading wildcard:

Step 1: Add a new column to the Employees table called ReverseFullName.

Step 2: Populate the ReverseFullName column with the name of each employee as its values, but in reverse.

Step 3: Finally, create an index named IdxReverseFullName on the ReverseFullName column.

Follow these steps first and then rewrite the SELECT query and improve its performance so that it uses a trailing wildcard instead of the leading wild card.
The expected output result when you execute the rewritten query should be the same as the result in the following screenshot:


![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/f4337617-2c88-44dd-8cd0-fa90f542d393)


# Solution: SELECT statement optimization in MySQL

Once you have completed the tasks in the ungraded lab, you can check and compare your answers with the following solutions.


Task 1 solution
Lucky Shrub need data on client orders. They have written the following SELECT query to retrieve all data from the Orders table:

```SQL
SELECT * 
FROM Orders;
```

However, the data they need is contained within the OrderID, ProductID, Quantity and Date columns. So, these are the important fields that their query must target. Targeting other columns in the table is an inefficient use of resources.

Rewrite the SELECT statement so that it is optimized.

The expected output result should be the same as the following screenshot when you execute the rewritten query.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/a10615f8-76a4-45d2-8ab8-3e692a24f54b)

Solution
```SQL
SELECT OrderID, ProductID, Quantity, Date 
FROM Orders;
```

Task 2 solution
Lucky Shrub need to find the order placed by the client Cl1. They have written the following query to complete this task:
```SQL
SELECT * 
FROM Orders 
WHERE ClientID='Cl1';
```

However, this query’s execution plan shows that it does not use an index to perform this search, as indicated by the NULL values in possible_keys and keys columns.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/1873cda4-ae4f-4cad-8d86-44484d01e469)

Help Lucky Shrub to optimize this query by creating an index named IdxClientID on the required column of the Orders table. Once you have created the index, run the same SELECT statement as above with the EXPLAIN statement.

The expected output result should be the same as the following screenshot when executed:  

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/bcea19eb-f288-49bf-8e51-6fbdfea3b745)

Solution

Create the index using the following statement: 
```SQL
CREATE INDEX IdxClientID ON Orders(ClientID);
```

Then call the SELECT query using the EXPLAIN statement:
```SQL
EXPLAIN SELECT * 
FROM Orders 
WHERE ClientID='Cl1';
```

Task 3 Solution
Lucky Shrub have written the following SELECT query to find the details of the employee whose last name is Tolo:
```SQL
SELECT * 
FROM Employees 
WHERE FullName LIKE '%Tolo';
```

However, there’s an index on the FullName column which the query cannot use because it contains a leading wildcard (%) in the WHERE clause condition.

The following steps can be taken to eliminate the leading wildcard:

Step 1: Add a new column to the Employees table called ReverseFullName.

Step 2: Populate the ReverseFullName column with the name of each employee as its values, but in reverse.

Step 3: Finally, create an index named IdxReverseFullName on the ReverseFullName column.

Follow these steps first and then rewrite the SELECT query and improve its performance so that it uses a trailing wildcard instead of the leading wild card.

The expected output result when you execute the rewritten query should be the same as the result in the following screenshot:

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/ed582c25-5710-4037-8daf-84b476e0aa01)

```SQL
ALTER TABLE Employees ADD COLUMN ReverseFullName VARCHAR(255); -- Add the ReverseFullName column

UPDATE Employees
SET ReverseFullName = CONCAT(
    SUBSTRING_INDEX(FullName, ' ', -1),  -- Extract last name
    ' ',                                 -- Add a space
    SUBSTRING_INDEX(FullName, ' ', 1)   -- Extract first name
);

CREATE INDEX IdxReverseFullName ON Employees (ReverseFullName); -- Index

SELECT * 
FROM Employees 
WHERE ReverseFullName LIKE 'Tolo%';
```





