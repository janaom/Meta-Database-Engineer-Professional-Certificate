# Introduction

In this exercise you need to perform data analysis in Tableau to help Global Super Store understand their business. Use Tableau Desktop to complete this exercise.

The Global Super Store dataset is attached for you to download and use in this exercise. This file includes more than 51000 records of data about customers, orders and products.

[Worksheet](https://d3c33hcgiwev3.cloudfront.net/9GScrAa0RCarDNRf-oUe0g_452298fa013a423f82d683d99d8386e1_Worksheet.xlsx?Expires=1696291200&Signature=lBHEiQ2I5jaYrbPTO4zk4RlHitF2kmqFGY-vothVDWRmnyDfncjfH88BUfCmlsOc-81F13GVsVnkhNTzknKFowaaw926nf9QeMZi2qNYYAl3e6UVSNL2Pf~GusGCg21uYsVVhNeff4N3Aj9qTps0118TOlRHDK88YYJmEanbMI0_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

Create a new calculated field called Warranty based on 90 days from the order date. The warranty calculated field should be set as shown below in the following screenshot.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/8801f6d5-4c63-4a30-98d8-28dfe9c5ff44)


# Scenario

Global Super Store have collected large amounts of data. They now need to analyze this data to help understand their business activities and maximize their profits.


# Instructions

Complete the following steps to support the Global Super Store in performing data analytics in Tableau.


Step 1: Prepare the data set for analysis
In this first part of the task, you need to connect to the Global Super Store data set, then prepare it for data analysis by making sure that all fields including the Order date and the Ship date contain the correct data types.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/f2e9c402-6f1a-413f-8eb7-758ed2ab9c1f)


Step 2: Create a map chart
Global Super Store want to investigate their business performance in Africa. Create a map chart that shows sales in different countries in Africa. The map should show the sales in proportional sizes. If you rollover a country, you should be able to see the country name, quantity sold, and sales figure as shown below. 

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/0098383a-7038-480c-9acc-cc6837a6cbea)


Step 3: Create a bar chart
Global Super Store want to check the profits made in each country in Africa. However, they are only interested in data from countries where they have made at least $500 in profit. 

To help them identify this data, create a bar chart in Tableau called Profits in Africa. When you rollover a bar, you should be able to see the name of the country, the profits and the shipping cost, as shown below. 

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/0e1b7489-9440-4ffb-9bf6-43f612948765)


Next, develop a dashboard that includes the Sales in Africa map (created in the second part of the task), and the new worksheet Profits in Africa as shown below.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/83f03c98-b266-447b-8314-488af2788bcf)


Finally, make the dashboard interactive. When you click on a specific country in the map (such as Cote d'Ivoire) the information related to that country must be displayed in the bar chart.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/b18a24b4-d9cf-47d2-8ae2-b5e9c11a6b96)


Conclusion
In this exercise you performed data analysis in Tableau. You prepared the Global Super Store data for data analysis, analyzed the data with relevant charts, and created an interactive dashboard.

# Solution

In this reading, you will receive step-by-step guidance on how to complete the "Data analysis in Tableau" exercise.
Below, you will find a breakdown of each step.



Breakdown of individual steps
Step 1: Prepare the data set for analysis
Launch Tableau to open the connection page.

Under the connect tab on the left side, click on Microsoft Excel. This opens a dialog box that allows you to navigate to the Global Super Store Excel file in your computer.

Once you have located the file, select it and click on the Open button.

To fix the data type of the Order date and Ship date, go to the top area of each related column. Here, you’ll find ABC (In other words, the string). Each string instance should be changed to Date as shown below. 

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/b4fb53f0-093b-455b-8222-9ac6966972cb)

Next, create a new calculated field called Warranty based on 90 days from the order date:   

Select the small arrow in the orders date field. 

Click Create a calculated field and name the new field Warranty. 

In the Calculation Editor enter [Order Date] + 90 as shown below. 

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/181773dd-e118-4d66-85f2-3f90d40e1663)

The result should resemble the following screenshot:

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/7d4ab9bc-48d9-4f7e-b8f3-aa6d3cd28481)

Step 2: Create a map chart
Complete the following steps to create the Sales in Africa chart:

Double click Country field in the left Data pane. This action creates the world map with all countries.

Drag the Region field from the data pane and drop it onto the Filter shelf. In the General tab, select Africa. Click OK.

Drag the Sales field from the Data pane and drop it onto the Size mark.

Drag the Sales field from the Data pane and drop it onto the Color mark.

Drag the Quantity field from the Data pane and drop it onto the Detail mark. 

Provide a meaningful title for your view by calling it Sales in Africa. 


The following screenshot shows all the dimensions and measures you need to drag and drop in the view section to complete this task.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/09b9ac16-a0fe-45c9-90c7-18b72f4d92d0)

Step 3: Create a bar chart
Complete the following steps to create the Profits in Africa chart:

Drag the Country field from the Data pane and drop it onto the rows section. This action creates a table of data with all countries.

Drag the Region field from the data pane and drop it onto the Filter shelf. In the General tab, select Africa. Click OK.

Drag the Profits field from the Data pane and drop it onto the columns section.

Drag the Profits field from the Data pane and drop it onto the Filter shelf. Select the Least tab and type 500.

Drag the Country field from the Data pane and drop it onto the Color mark.

Drag the Shopping cost field from the Data pane and drop it onto the Detail mark. 

Click the Sorting option in the descending order icon to arrange bars by highest profit. 

Provide a meaningful title for your view, like Sales in Africa. 

The following screenshot shows all the dimensions and measures you need to drag and drop in the view section to complete this part of the task.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/238eddf8-13a4-4487-af67-e3d304545958)

Complete the following steps to develop a dashboard that includes the Sales in Africa map, and the new worksheet Profits in Africa:

Drag Sales in Africa map sheet from the sheets pane to the dashboard view. 

Drag Profits in Africa chart sheet from the sheets pane to the dashboard view, below the map. 

 

The following screenshot shows the two worksheets that you need to drag and drop in the view section of the dashboard.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/bf5cd9e3-245a-4150-8bdf-52e483d3403c)


Complete the following steps to make the dashboard interactive: 

To activate the interactivity feature of the dashboard, click on the Filter icon to activate the filtering process, as shown in the following screenshot. 

When you click on a specific country in the map, such as Cote d'Ivoire, the country related information will be displayed in the bar chart.

![image](https://github.com/janaom/Meta-Database-Engineer-Professional-Certificate/assets/83917694/64ebeae3-f58a-4f62-b608-2a4169b8b2db)




