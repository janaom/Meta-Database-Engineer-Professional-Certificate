Goal

In this exercise, you will learn how to practice table creation in a database from scratch. The objective of the exercise is to build a table in a database for the given scenario. You’ll then review the solution to check and compare your design and implementation of the table.  

Scenario

Mr. Erik Anderson has created a new football club for kids under 16 years old. He needs to create a table to store the players’ basic personal data including identity number, name and age.

Instructions

Please attempt the tasks below before you continue, so you can check and compare your answers with the solution.

Task 1: Create a database called football club.

Task 2: Create a table to store the data as follows:

Identify a suitable table name to store the players’ personal data. 

Identify the table attributes and data types.

Write a SQL statement to create the table.


Task 1: Create your database

1. You cannot build tables if there is no relevant database available to create tables within. Therefore, let’s create a new database for Mr. Anderson’s data by typing the following SQL statement inside the SQL code editor in Coursera platform as displayed below.
```
CREATE DATABASE football_club
```
2. Press enter to execute the create football club database.

3. Make sure you select the database to use by typing the following SQL statement and pressing Enter:
```
USE football_club; 
```
![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/99a39125-2f83-4a72-9cbc-5a5c2b84d4de)


Task 2: Create your table

1. Write a SQL statement that contains the CREATE TABLE command followed by the name of the table. Players is a suitable name in this case.

2. Open parenthesis to define the table's columns:  

●	Player ID

●	Player name

●	Player age

3. Assign each column a suitable data type. In this case, you can choose the following suitable data types:

●	player ID: INT

●	player name: VARCHAR(50)

●	player age: INT

4. Once all the required columns have been defined, add a closing parenthesis and a semi-colon at the end of the SQL statement as follows:
```
CREATE TABLE players (playerID int, playerName varchar(50), age int);
```
5. Press Enter to execute the SQL statement.

The image below displays the output after executing the CREATE TABLE players statement.       
![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/44d32f83-ed82-4417-90fa-e90f5b15ed29)


If you have followed all the steps correctly, you should now see the players table created inside the football_club database by typing the following show tables statement:
```
SHOW tables;
```
6. Press Enter to retreive the players table inside the football club database.  There may be more tables present if you have already created other tables within this database. 

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/42b37324-4043-4061-8d84-bdd306a92a1b)



In this exercise, you have practiced how to create a basic table inside a database. Here is an optional additional task for you to complete.


Additional task (optional)

Mr. Anderson wants to create another table to record information about the games the team will play, including the gameID, the score of each game and the dates they’re played on. Your task is to create this table for the football club.


Solution

Write the following SQL statement and press Enter to execute it:
```
CREATE TABLE games(gameID INT, gameDate DATE, score INT);
```
