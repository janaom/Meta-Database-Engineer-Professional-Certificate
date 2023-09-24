Goal 

Introduce an example of a database schema to demonstrate how data can be organized and related in tables.


Objectives  

Understand how to design a database schema


The chinook database example 

This exercise uses the well-known “chinook sample” database, which is widely used for example relational database demos and testing purposes. Also, it has been implemented in Coursera platform, which is good to be familiar with as well.

However, you are going to focus only on some of the main tables introduced in this database to highlight how a database schema is designed, and not the entire chinook schema.


Database schema design 

Before you develop your actual database, you should design a relevant database schema to document the requirements and to propose an architecture of the database structure. To design a basic database schema, you need to apply the following steps:  

Step 1: Define the database purpose.  

Step 2: Identify the database tables including 

Tables attributes 

Attributes data types 

Primary key for each table  

Step 3: Create relationships between tables

 

Instructions 

Please attempt the following tasks before you continue, so that you can check and compare your answers with the solution. 

Task 1: Identify the database purposes.  

Task 2: Identify 6 main tables with a brief description and a primary key for each table.  

Task 3: Identify the relationships between the 6 main tables. 

Task 4: Create an entity relationship diagram of the 6 main tables. 

 

Note: This exercise can also be completed using a pencil and paper or any other suitable professional tool.


Task 1: Identify the database purpose 

The “chinook sample” database represents a fictitious digital media company that includes information about artists, albums, media tracks, invoices and customers. 

 

Task 2: Identify the database tables 

The chinook sample database has considered adequate normalization level and created 11 tables to store and relate data to avoid data redundancy. However, this exercise will only focus on 6 main tables, including some relevant attributes for each.  

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/88851c06-e93c-40f7-ba1a-bbdcd9e149ed)

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/264853d6-2c71-4925-96b5-46653750411d)

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/e4fec2a0-45c1-40ca-8f6c-0903a92da419)

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/bc9afbdf-ba17-41ba-92ad-97cc2121b5e0)

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/f2a55da1-43b7-4c5b-b706-33dfa8605680)


Task 3: Identify relationships between tables 

The chinook sample database defines the following relationships between the 6 stated tables:  

Each employee will support one or many customers.  

Each customer may have multiple invoices  

Each track belongs to one album. 

Each invoice relates to one track. 

Each track belongs to one album  

Each album may contain multiple tracks 

Each artist has one or multiple albums 


Task 4: Create entity relationship diagram 

The final diagram connects all tables by using the FOREIGN KEYS as illustrated in the following diagram. Remember this is just a customized part of the chinook database schema. If you want to see the entire diagram you can check Appendix A. 

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/b73aaf6d-b810-4abe-8987-34b306980d0c)


Additional task (optional)

You are required to extend the customized chinook schema by adding a new table called "location" that shows the city and the country the artist lives in. 


Solution 

Add a new table called location  

Add a foreign key “locationId” to the “Artists” table to connect it with the location table 

The new chinook customized schema must look like the following ER-diagram:

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/816a7668-509e-4d0d-9d68-aeebed6c4d2f)


Appendix A: the original Chinook database schema 

The following diagram is a blueprint of the chinook database schema that shows how data is organized and related in tables.  

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/ce4b9fff-4ea1-4e8c-844d-ac8d7cd9b84c)


