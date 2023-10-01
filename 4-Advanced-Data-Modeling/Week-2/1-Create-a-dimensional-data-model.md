# Introduction

Create a dimensional model for Global Super Store to help them make sense of their sales and profits.


# Scenario 

Global Super Store have experienced a decline in their profits in the last few years.

There are several factors that impacted their profits including:

Global instability around shipping and product costs.

New competitors appearing in different markets around the world.

Out of date products.

Emerging new technologies.

And the development of new products. 


Global Super Store needs to understand how these factors are affecting their sales and profits. They need to compare data amongst different customers, products, times and locations to understand the problem. 


# Instructions

You can create the dimensional model using any professional tool of your choice such as MySQL Workbench, StarUML and draw.io.


Step 1: Identify key information
You should already know that creating a dimensional model must start with identifying the business process you want to deal with. In this scenario, this is the sales process. 

To perform data modeling, you need to identify the grain, the dimensions and the measures that you must be used to build the dimensional model. 

This will help the Global Super Store to analyze the sales data in an appropriate way. In this part of the task, you should identify the following information:

Grain: Provide the granularity level required to build the dimensional data model.

Facts: Determine the key measures required in the model.

Dimensions: Identify the key entities to set a suitable context for the measures.


Step 2: Create a star schema
Once you have completed the first part of the task, carry out these next steps:

Create a Star Schema based on the dimensions and facts identified in the first part of the task. 

Create the dimensions and the fact tables. Include relevant attributes and data types in each table.

Define the primary and the foreign keys in the data model.


Step 3: Create a snowflake schema
Extend the Star Schema that you developed in the second part of the task by creating a suitable Snowflake Schema with a particular focus on the products dimension.


Conclusion
In this exercise you created a dimensional model for Global Super Store. You used an appropriate approach for dimensional data modeling. You designed a star schema, and created a snowflake schema.

# Solution

In this reading, you will receive step-by-step guidance on how to create a dimensional data model.
Below, you will find the complete solution followed by a breakdown of each step.


Breakdown of individual steps
Step 1: Identify key information 
Identify the grain: Global Super Store is an international company that has been operating for several years. So, they need to investigate their sales at the following levels of granularity:

Region, country and city.

Year, quarter, month, day or event levels.

Category, subcategory and items.

 

Identify the facts: Global Super Store must investigate all the measures that impact the sales including:

The buy and sale prices of all products.

The quantity sold of each product.

The shipping cost of each product. 

 

Identify the dimensions: Global Super Store must examine the measures against the following key dimensions:

Location.

Time.

Product.

And customers.

 

Step 2: Create a star schema
The following ER diagram illustrates a suitable Star schema for the Global Super Store dimensional model.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/d1fa469b-1467-42a7-9637-0107175fa8ae)

Step 3: Create a snowflake schema
The following ER diagram illustrates a suitable Snowflake schema for Global Super Store dimensional model.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/05c4c5b3-3804-41fd-b498-205a9c5fa186)
