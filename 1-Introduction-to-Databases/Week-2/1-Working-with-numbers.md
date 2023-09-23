Goal 

The goal of this exercise is for you to learn how to work with numerical values in a database. The objective of the exercise is that you will be able to demonstrate how to work with numerical data types in SQL. In this exercise, you will learn about two main variations of numeric data types. 

Scenario 

Mr. Carl Merkel owns a small business named CM Mobiles that sells mobile devices. He wants to create a database to store key information about mobile devices. This information includes: 
●	The device ID or number, 
●	The device name,
●	And the price of the device.

This information is displayed in the following table:
![Screenshot-2023-09-23-203952 png](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/1a1ef28c-d679-4b39-8142-0e30730adb91)


Instructions 

Please attempt the tasks below before you continue, so that you can check and compare your answers with our solution. 

Task 1: Create a database called cm_devices

1.	Type the following SQL statement inside the SQL terminal editor in the Coursera platform:

CREATE DATABASE cm_devices; 

2.	Press Enter to execute the create database statement. 

3.	Make sure you select the database you want to create the table inside of by typing the following SQL statement: 

USE cm_devices; 

4.	The SQL ‘USE’ keyword is used to select a database in MySQL followed by the name of the database. Press Enter to execute the query. The output will be “Database changed”, as demonstrated in the following screenshot:
   ![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/b8da5eb2-6963-4b40-adf8-8afdb03df498)


Task 2: Create a SQL statement with relevant attributes and data types 

1.	Identify a suitable name for the table in which you want to store the data about mobile devices. In this case, you can call the table “devices”.

2.	Identify the data type for each column within the table.

Based on CM Mobiles’ requirements, the mobile devices table must contain three columns as follows:

●	A column called “Device ID” that stores whole numbers. In this case, you should use INT as the data type.

●	A second column called “Device name” that is expected to store data as a string-like alphanumeric value. For example, iPhone XR 1.

●	And a third column called “Price”. This final column is expected to store numeric data with possible fractional values. In this case, you should use the DECIMAL data type. With the decimal data type, there is no issue with storing a whole number because the fractional part is separated by a decimal point with 00 on the right side of the number. This is indicated in the third row of the mobile devices table, where the price is 1050.00 (which is equivalent to 1050).

3.	Write a complete SQL statement to create the mobile devices table inside the cm_devices database.

3.1	Write the SQL statement that contains the CREATE TABLE command followed by the name of the table which is “devices” in this case.

3.2	Open parenthesis to define the table columns including device ID, device name and price.

3.4	Define a suitable datatype for each column as follows:
●	The column device ID with integer datatype.
●	The price column with decimal datatype.
●	The device name with VARCHAR max 50 char limit.

3.5	Add a closing parenthesis and a semi-colon at the end of the SQL statement. The complete statement should replicate the following syntax:

CREATE TABLE devices (deviceID int, deviceName varchar(50), price decimal);

3.6	Execute the query by pressing Enter.

If you have followed all the steps correctly, you should now be able to access the devices table that was created inside the cm_mobiles database by typing:

SHOW tables;

3.7	Press Enter. 

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/2c48081a-aec1-4d6b-9944-08373b73aa4f)


To check the structure of the devices table, type the following SQL statement and press Enter:

SHOW columns FROM devices;

This displays all the devices table’s columns and data types.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/f55b7c9c-694b-4421-ad86-33a7d45021e5)



In this exercise, you have practiced how to define numeric datatypes in database. Here is an additional task for you to test your skills.

Additional task (optional)

Mr. Merkel wants to create another basic table in the database to store data about the stock of the devices including device ID, quantity available in the stock and total available cost of the quantity. This basic table is shown in the table below, with each column showing device ID, the quanity in stock and the total price. 

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/e40555d0-fbc3-4560-8816-c59465e09c0b)



Based on the table and information above, complete the following:

1.	Identify an appropriate table name to create, given the information provided. 

2.	Identify columns that should be available in this table and define them with the appropriate data types.

3.	Write the full SQL statement that creates the table and columns.

Solution: 

1: table name: Stock 

2: Device id INT

     Quantity INT 

     Total cost Decimal

3: CREATE TABLE stock (deviceID int, quantity int, totalPrice decimal);
