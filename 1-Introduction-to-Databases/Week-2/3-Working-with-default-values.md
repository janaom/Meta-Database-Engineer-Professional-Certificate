# Goal

The goal of this exercise is for you to learn how to work with default values in a database. The objective is to allow you to practice working with default values using the default constraint in SQL.

# Scenario 

Mr. Carl Merkel owns a small business that sells mobile devices called “CM Mobiles” in Harrow, London. He wants to create a database to store key information about customers' addresses including customer ID, street, postcode and town name. The list of addresses for current customers of CM Mobiles is listed in the address table below.
![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/1b805629-a48d-412f-8acf-738f7c7b6bef)


# Instructions

Create an SQL statement  with relevant attributes and constraints as follows:

1. Identify the column that requires default values.  

2. Write a complete SQL statement to create the address table with relevant constraints.

Please attempt the tasks before you continue so you can check and compare your answers with the solution.


Creating the table

Identify the column with default values.

Notice that the address table shows that most customers are living in Harrow area, which means CM Mobiles customers are coming mainly from this city.  

In this case, you can define a default value for the city column as “Harrow” when you create the address table.  

This would save Mr. Carl from having to enter “Harrow” repeatedly into the city field for each new customer record as it's filled automatically with the default value “Harrow”. Of course, this assumes that no other value was entered in the table.


Note: You need to have a database to create the table inside it. If you don’t have one yet, see below how to create the CM Mobiles database.


1. Type the following SQL statement inside the SQL terminal editor on the Coursera platform.
```SQL
CREATE DATABASE cm_devices;
```
2. Press Enter to execute the create database statement.

3. Make sure you select the database to use it by typing the following SQL statement and press enter.
```SQL
USE cm_devices;
```
![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/a982dcf8-a6e3-48ae-8649-2ad54659d23b)


4. Create a table

4.1 Write the SQL CREATE TABLE command followed by the name of the table, “address” in this case.

4.2 Open parenthesis to define the table’s columns including customer ID, street, postcode and town. Each column must be assigned a suitable data type as you learned in earlier videos and exercises.

4.3 Use the SQL “DEFAULT” keyword to declare the pre-set default value.

4.4 Once all required columns have been defined, add a closing parenthesis and a semi-colon at the end of the SQL statement as follows:
```SQL
CREATE TABLE address(id int not null, street varchar(255), postcode varchar(10), town varchar(30) default "Harrow");
```
The DEFAULT keyword used in this statement is followed by the default value “Harrow” for the town name column in the Address table. In this case, if Mr. Carl Merkel wants to insert data into this table, then there is no need to type “Harrow” for any customer who lives in this town as it will be inserted automatically.

5. Execute the query by pressing enter.

6. If you want to check the structure of the address table, type the following SQL statement and press Enter:
```SQL
SHOW columns FROM address;
```
This shows all the address table columns with data types and the default constraint “Harrow”.
![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/fb52b69f-61cf-4767-98dc-66c29f9fb647)


In this exercise, you have learned how to use the default constraint to enforce a specific default value, which is very useful to use for columns expecting to hold the same data. 


Here is an optional additional task for you to test your skills.

  

Additional task (optional)

Mr. Carl Merkel notices that most customers come from the same postcode i.e., “HA97DE”.  

You are required to write the SQL statement again to declare both the postcode and the town name with default values.

Remember to drop the address table before creating a new one.

To drop the table, simply type: 
```SQL
DROP TABLE Address;.   
```
# Solution: 
```SQL
CREATE TABLE Address (id int NOT NULL,  street VARCHAR(255), postcode VARCHAR(10) DEFAULT "HA97DE", town VARCHAR(30) DEFAULT "Harrow"); 
```
![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/40ae80d7-4b63-4f6a-b3ae-81610bb6ea8e)
