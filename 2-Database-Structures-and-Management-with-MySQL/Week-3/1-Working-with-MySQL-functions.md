Lab Instructions: Working with MySQL Functions

Mangata and Gallo (also known as M&G) is a jewelry store that specializes in special occasions like engagements, weddings and anniversaries. In this lab, you are going to complete a series of tasks to make it easier for M&G staff to format and filter data using MySQL string, Math, Date and Comparison functions for their reports.

The data used in this lab comes from the following item and mg_orders tables:

item table

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/d01a183c-74d1-46b6-afe4-9fd053e6b21d)


mg_orders table

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/f288fb09-ad2b-4c6c-afa5-22f5677e708b)


Prerequisites

To complete this lab, you must have created the M&G jewelry store database in MySQL. This includes the item and mg_orders tables, which must be populated with relevant data.

The code required to create the database and the tables are listed below.

1: Create the database

```
CREATE DATABASE jewelrystore_db;
```
2: Use the database
```
USE jewelrystore_db;
```
3: Create the item table
```
CREATE TABLE item(ItemID INT, Name VARCHAR(150), Cost INT, PRIMARY KEY(ItemID));
```
4: Insert data into the item table

```
INSERT INTO item VALUES(1,'Engagement ring',2500),(2,'Silver brooch',400),(3,'Earrings',350),(4,'Luxury watch',1250),(5,'Golden bracelet',800), (6,'Gemstone',1500);
```
5: Create the mg_orders table

```
CREATE TABLE mg_orders(OrderID INT, ItemID INT, Quantity INT, Cost INT, OrderDate DATE, DeliveryDate DATE, OrderStatus VARCHAR(50), PRIMARY KEY(OrderID));
```
6: Insert data into the mg_orders table
```
INSERT INTO mg_orders VALUES(1,1,50,122000,'2022-04-05','2022-05-25', 'Delivered'),(2,2,75,28000,'2022-03-08',NULL, 'In progress'), (3,3,80,25000,'2022-05-19','2022-06-08', 'Delivered'), (4,4,45,100000,'2022-01-10',NULL, 'In progress'),(5,5,70,56000,'2022-05-19',NULL, 'In progress'),(6,6,60,90000,'2022-06-10','2022-06-18', 'Delivered');
```

The main objectives of this activity:
Work with MySQL String, Math, Date and Comparison functions.

Exercise Instructions
Please attempt the following tasks:

Task 1: Write a SQL SELECT query using appropriate MySQL string functions to list items, quantities and order status in the following format:

Item name–quantity–order status

Item name should be in lower case. Order status should be in upper case.

The expected output result should be similar to the following screenshot (if you have the same data set populated in the orders table).

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/4cfda539-cd2f-4cd0-aeff-9e10936ca3b0)


Task 2: Write a SQL SELECT query using an appropriate date function and a format string to find the name of the weekday on which M&G’s orders are to be delivered.

The expected output result should be like the following screenshot (if you have same data set populated in the orders table).

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/8d3e7099-0398-44a2-a1d3-58119ad89501)


Task 3: Write a SQL SELECT query that calculates the cost of handling each order. This should be 5% of the total order cost. Use an appropriate math function to round that value to 2 decimal places.

The expected output result should be like the following screenshot (if you have same data set populated in the orders table).

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/4c28eb10-9548-4a05-86e7-1f29f224b8eb)


Task 4: Review the query that you wrote in the second task. Use an appropriate comparison function to filter out the records that do not have a NULL value in the delivery date column.

The expected output result should be like the following screenshot (if you have same data set populated in the orders table).

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/cfd8b617-af4b-4285-871e-552f5bf0436e)


When you have completed these tasks, you can check and compare your answers with the solutions.
