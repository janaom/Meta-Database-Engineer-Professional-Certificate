## Lab Instructions

Lucky Shrub needs to query their database. They can do this by using functions and stored procedures in MySQL. In this lab, you must complete a series of tasks to help Lucky Shrub staff query data from the Orders table in their database.

The Orders table contains information about the Order ID, Client ID, Product ID, Quantity and Cost as shown in the following screenshot.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/6f32750e-5625-47bf-bbee-cbb6bc771584)

## Prerequisites

First, create the Lucky Shrub database in your MySQL environment. Then, create and populate the Orders table with the relevant data inside the Lucky Shrub database.

The code to create the database and the Orders table is listed below.

1: Use the following code to create the database:
```SQL
CREATE DATABASE Lucky_Shrub;
```
2: Make use of the following code to use the database:
```SQL
USE Lucky_Shrub;
```

3: Use the following code to create the Orders table: 

```SQL
CREATE TABLE Orders (OrderID INT NOT NULL PRIMARY KEY, ClientID VARCHAR(10), ProductID VARCHAR(10), Quantity INT, Cost DECIMAL(6,2), Date DATE); 
```
4: Use the following code to insert the data: 

```SQL
INSERT INTO Orders(OrderID, ClientID, ProductID , Quantity, Cost, Date) VALUES
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
(11, "Cl4", "P5", 5, 100, "2020-09-15"), 
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
(29, "Cl3", "P3", 20, 800, "2021-09-03"),  
(30, "Cl1", "P1", 10, 500, "2022-09-01");
```

## There are two main objectives in this activity:

Develop a user defined function

Develop a stored procedure

## Tasks Instructions
Please attempt the following tasks to help make it easier for Lucky Shrub staff to query data from their database.

Task 1:

Create a SQL function that prints the cost value of a specific order based on the user input of the OrderID. The expected output result should be the same as the result in the screenshot below when you call the function with an OrderID of 5.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/51d46ea6-d7f6-4301-9ae2-7754337b54b5)


Task 2:

Create a stored procedure called GetDiscount. This stored procedure must return the final cost of the customer's order after the discount value has been deducted. 

The discount value is based on the order's quantity. The stored procedure must have the following specifications: 

The procedure should take one parameter that accepts a user input value of an OrderID. 

The procedure must find the order quantity of the specific OrderID. 

If the value of the order quantity is more than or equal to 20 then the procedure should return the new cost after a 20% discount. 

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/432bdf20-66fc-4d87-b62e-db26331498bf)


If the value of the order quantity is less than 20 and more than or equal to 10 then the procedure should return the new cost after a 10% discount.

The expected output result should be the same as the result in the screenshot below when you call the procedure with OrderID 5.

# Solution: Developing functions in MySQL

Once you have completed the tasks in the ungraded lab, you can check and compare your answers with the following solutions.


Task 1 solution: 

Create a function that prints the cost value of a specific order. This should be based on the user input of the OrderID. The expected output result should be the same as the result in the screenshot below when you call the function with OrderID 5.

```SQL
CREATE FUNCTION FindCost(order_id INT) 
RETURNS DECIMAL (5,2) DETERMINISTIC 
RETURN (SELECT Cost FROM Orders WHERE OrderID = order_id);
```

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/d015b3f7-db17-47da-abcd-39e1e208a974)

Task 2 solution:

Create a stored procedure called GetDiscount(). This stored procedure must return the final cost of the customer’s order after the discount value has been deducted. The discount value is based on the order’s quantity. The stored procedure must have the following specifications:

The procedure should take one parameter that accepts a user input value of an OrderID. 

The procedure must find the order quantity of the specificOrderID. 

If the value of the order quantity is more than or equal to 20 then the procedure should return the new cost after a 20% discount. 

If the value of the order quantity is less than 20 and more than or equal to 10 then the procedure should return the new cost after a 10% discount.

```SQL
DELIMITER // 

CREATE Procedure GetDiscount(OrderIDInput INT) 
     BEGIN 
         DECLARE cost_after_discount DECIMAL(7,2); 
         DECLARE current_cost DECIMAL(7,2); 
         DECLARE order_quantity INT; 
         SELECT Quantity INTO order_quantity FROM Orders WHERE OrderID = OrderIDInput; 
         SELECT Cost INTO current_cost FROM Orders WHERE OrderID = OrderIDInput; 
        IF order_quantity >= 20 THEN
          SET cost_after_discount = current_cost - (current_cost * 0.2);              
        ELSEIF order_quantity >= 10 THEN
          SET cost_after_discount = current_cost - (current_cost * 0.1); 
        ELSE SET cost_after_discount = current_cost;
        END IF;
    SELECT cost_after_discount; 
END//

DELIMITER ;
```

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/5e827d9b-50aa-4fce-a474-bf1888187479)

The expected output result should be the same as the result in the screenshot when the procedure is called with an OrderID value of 5.  

