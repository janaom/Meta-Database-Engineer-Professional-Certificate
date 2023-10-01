# Introduction

In this exercise you'll design a simplified logical relational database model for Mangata and Gallo.


# Scenario

Mangata and Gallo (M&G) has built an ad hoc database system to store data about their customers, products, orders and delivery status in one large table as shown below.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/203abe7c-4f19-4200-b982-2c0e76376917)

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/89366924-6e8d-4377-85ed-2ceaf561a6c5)



This database is difficult to manage and includes loads of redundant data. M&G need you to help them create a proper database model for a simplified and logical relational database.


Instructions
You can create the required relational data model using any database modeling tool of your choice such as staruml.io or draw.io. 


Step 1: Create a conceptual model
Create a conceptual model to support M&G’s online ordering system. 

The model should consider the entities listed in the M&G big table. 

All entities must be connected using meaningful labels.


Step 2: Create a logical ER diagram
Based on the conceptual model that you developed in the first task, create a logical ER diagram as follows:

Translate each entity in the conceptual diagram into a table with relevant attributes (Feel free to add attributes that do not exist in the table).

Specify the primary key of each table.

Create a multiplicity relationship between the tables.

Define relevant constraints such as NOT NULL and foreign keys.


Step 3: Review your diagram
Review the logical ER diagram, and make sure that your data model conforms to the first normal form by applying the data atomicity rule.


Conclusion
In this exercise you practiced designing a database model. You created a high-level conceptual data model, designed a logical ER diagram and applied relevant normalization forms.

# Solution

In this reading, you will receive step-by-step guidance on how to complete the "Design a database model for this scenario" exercise. Below, you will find a breakdown of each step.

 

Breakdown of individual steps
Step 1: Create a conceptual model
A conceptual data model diagram that includes the four entities and relationships outlined in the diagram below is sufficient. However, you may have only three entities at this stage. You can add the Delivery status entity in the third task. You can also use different names to those listed (such as customers instead of clients) once you are using meaningful names.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/9d562bdd-3984-410b-8098-bc58ec9a270c)

Step 2: Create a logical ER diagram
 Your tables must resemble those outlined in the diagram as follows:

Each table must possess relevant attributes.

All primary keys must be specified as required.

There must be multiplicity relationship between tables like those outlined.

All relevant constraints must be defined, including NOT NULL and foreign keys.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/37b7b78c-1fd0-40ec-bea2-228f39675f5f)

Step 3: Review your diagram
Some clients could have multiple delivery addresses. Storing more than one address in the address column inside the Clients table violates the first normal form. Therefore, to apply data atomicity, you must create an Address table and relate it to the delivery table as shown below.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/691298d7-7cfc-4fdf-8651-e8dd0c51a851)



