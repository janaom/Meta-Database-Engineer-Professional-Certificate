Lab Instructions

Mangata and Gallo is a jewelry store that specializes in special occasions like engagements, weddings and anniversaries. The jewelry company primarily operates online and has a small storefront in Austin, Texas with an atelier attached for browsing. The company has asked you to create a table in their database called 'Staff'. This table must contain the records of all staff members.

Note: Before you begin, make sure you know how to access 
MySQL environment
 

Prerequisites

To complete this lab, you need to have the Mangata and Gallo database so that you can create the 'Staff’ table inside it. If you don't have this database, complete the following steps to create it.

1: Create database
```
CREATE DATABASE Mangata_Gallo;
```
2: Use database
```
 USE Mangata_Gallo;
```

This activity has two main objectives:
Create the 'Staff' table in Mangata and Gallo database.

Make the necessary changes to the table structure.

Exercise Instructions
Please attempt the following tasks.

Task 1

Write a SQL statement that creates the Staff table with the following columns.

StaffID: INT

FullName: VARCHAR(100)

PhoneNumber: VARCHAR(10)

The table structure should be the same as the following screenshot (assuming that you have created and populated the table correctly.)

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/bfbeaa24-63ee-4f0d-88c8-cb413d7660f9)


Task 2

Write a SQL statement to apply the following constraints to the Staff table:

StaffID: INT NOT NULL and PRIMARY KEY

FullName: VARCHAR(100) and NOT NULL

PhoneNumber: INT NOT NULL

The expected output result should be the same as the following screenshot (assuming that you have created and populated the tables correctly.)

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/9e95c5e6-7745-456d-90e8-d20242851838)


Task 3

Write a SQL statement that adds a new column called 'Role' to the Staff table with the following constraints:

Role: VARCHAR(50) and NOT NULL

The expected output result should be the same as the following screenshot (assuming that you have created and populated the tables correctly.)

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/552c08a1-4ad2-4ae9-9b58-e8812f71be43)


Task 4

Write a SQL statement that drops the Phone Number column from the 'Staff' table.

The expected structure of the table after removing the Phone Number column should be the same as the following screenshot (assuming that you have created and populated the tables correctly.)


![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/ed104194-2d56-491e-98b2-e1feef3e2cb9)

Once you have completed these tasks, you can check and compare your answers with the solution in the reading "Exercise: Changing table structure (Exercise solution)".
