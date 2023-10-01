# Introduction

In this exercise you'll design a database model in MySQL Workbench for Mangata & Gallo (M&G) jewelry store.


# Scenario

Mangata & Gallo (M&G) jewelry store wants to make use of the logical database model outlined in the diagram below. You need to help the company to develop this model using MySQL Workbench and implementing it in your MySQL server.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/2e02f4c0-2c69-485e-9d65-fb6986ae3364)


# Instructions
Design and implement a database model in MySQL by completing the following steps. 


Step 1: Create an ER diagram
Your first step is to use the visual data modeling tool in MySQL Workbench to create the proposed ER diagram for M&G. Your data model should resemble the following diagram.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/48338adf-9162-4bea-89dc-66a0c86f1826)


Step 2: Implement the internal schema
Next, you need to use MySQL Workbench’s forward engineer feature to implement the internal schema in your MySQL server.

Once you have implemented this feature, you should be able to see your schema implemented in the MySQL Workbench’s SCHEMAS section as shown below. 

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/c98b00de-ddfb-4fd3-b316-1858c9d9baeb)


Step 3: Populate the M&G database
Next, you need to populate the M&G database with data using the SQL Workbench editor. 

Use the INSERT statements code attached in Appendix A as shown in the screenshot below. 

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/f18cd3cf-8316-4ba5-a2f4-d0448c31c1f9)


M&G wants to create a virtual table so that they can easily find information on their orders. This information must contain data from all tables including:

Clients, 

Orders, 

Products, 

Delivery 

and Address.

For example, if you were to write this SQL statement, then the following output result is printed:

SQL statement
```SQL
SELECT * FROM orders_view;
```

Output:

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/04196db6-868b-4128-b202-0c1a00600376)


Hint: In this situation you need to use the INNER JOIN clause to obtain relevant information. 

Appendix A: INSERT SQL statements:
```SQL
INSERT INTO clients
VALUES 
(1, 'Vanessa McCarthy', 757536378, 'vm@mangatagallo.com'), 
(2, 'Marcos Romero', 757536379, 'mr@mangatagallo.com'), 
(3, 'Hiroki Yamane', 757536376, 'hy@mangatagallo.com'), 
(4, 'Anna Iversen', 757536375, 'ai@mangatagallo.com'), 
(5, 'Diana Pinto', 757536374, 'dp@mangatagallo.com');

INSERT INTO products 
VALUES 
(1, 'Engagement ring', 2000, 2500, 25), 
(2, 'Silver brooch', 300, 400, 100), 
(3, 'Earrings', 1000, 1250, 100), 
(4, 'Luxury watch', 500, 800, 50), 
(5, 'Golden bracelet', 800, 1200, 100);

INSERT INTO orders 
VALUES 
(1, '2022-10-15', 1, 1, 1, 2500), 
(2, '2022-10-16', 2, 2, 2, 800), 
(3, '2022-10-17', 3, 5, 1, 800), 
(4, '2022-10-17', 4, 3, 3, 1050), 
(5, '2022-10-18', 5, 4, 1, 1250);

INSERT INTO address
VALUES 
(1, '223 Golden Hills, North Austin, TX', '78758', 'Texas'),
(2, '119 Silver Street, Bouldin Creek, TX', '78737', 'Texas'), 
(3, '785 Bronze Lane, East Austin, TX', '78717', 'Texas'), 
(4, '908 Diamond Crescent, South Lamar, TX','76643 ', 'Texas'), 
(5, '345, Golden Hills, North Austin, TX', '78759', 'Texas'), 
(6, '812, Diamond Crescent, North Burnet, TX', '78611', 'Texas');

INSERT INTO delivery 
VALUES 
(1, '2022-10-17', 'Done', 1, 'None', 1), 
(2, '2022-10-20', 'Done', 2, 'None', 2), 
(3, '2022-10-22', 'Done', 3, 'None', 3), 
(4, '2022-10-25', 'Done', 4, 'None', 4), 
(5, '2022-10-27', 'Done', 5, 'None', 5);
```

Conclusion
In this reading you designed a database model in MySQL Workbench. You created the proposed database model using MySQL Workbench. You implemented the database schema inside MySQL server using the Forward Engineer method. And you created a virtual table to summarize data from multiple tables.

# Solution

In this reading, you will receive step-by-step guidance on how to complete the "Design a database model in MySQL Workbench" exercise. Below, you will find a breakdown of each step.


Breakdown of individual steps
Step 1: Create an ER diagram
Your first step is to use the visual data modeling tool in MySQL Workbench to create the proposed ER diagram for M&G. Your data model should resemble the following diagram.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/08a904ac-4ab3-44de-ae1d-ddc945dc7780)

To create this diagram, access the MySQL Workbench home screen. 


![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/2285312d-573d-4a49-9274-d4ebf160be78)

Select data model option.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/3b5b3f33-056a-4cb9-b6f4-a37e4b5e9c48)

Click on the (+) icon.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/d0077a9e-1cd7-446f-a36a-cb8641ab0660)

Click on Add diagram as shown below:

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/5f79b5a1-f354-4883-954f-381f19244eea)

Begin building your data model in the MySQL Workbench Designer. 

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/80c76d9b-db69-4a16-8ce0-2900ff7088d8)

Step 2: Implement the internal schema
Use MySQL Workbench’s forward engineer feature to implement the physical data model that you created.

In MySQL Workbench, select the right model, then select the Database tab and the Forward Engineer option.

In the Connection Options, select the MySQL connection and click Next.

The Options step lists optional advanced options. You can ignore these and click Next.

Make sure that the “Export MySQL Table Objects” check box is ticked and click Next.

The Review SQL Script step displays the SQL script to be executed on the live server to create your schema in MySQL. Click Next to execute the forward-engineer process.

The Commit Progress step confirms that each task has been executed. Click Close to close the wizard.

The new database schema is now created in MySQL server as shown below.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/bbf0b5df-e882-420d-b61c-93067b41405f)

Step 3: Populate the M&G database
After you have successfully completed the previous task, you then need to populate the M&G database with data using the SQL Workbench editor.

Use the following SQL statements to create the virtual table:
```SQL
CREATE VIEW orders_view AS SELECT orders.OrderID, clients.ClientID, clients.FullName, products.ProductName, orders.Quantity, orders.TotalCost, delivery.DeliveryStatus, delivery.DeliveryDate,  address.Street 
FROM clients INNER JOIN orders 
USING (ClientID)
INNER JOIN products using (ProductID)
INNER JOIN delivery using (OrderID)
INNER JOIN address using (AddressID);
```

To query this virtual table, execute the following SQL statement:
```SQL
SELECT * FROM orders_view;
```

The following output result is printed:

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/bb3eb1bd-5814-49eb-ad25-221e48645d7e)



