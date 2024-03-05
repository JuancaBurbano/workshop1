# Readme about the Workshop1 

## Introduction 

For this project we used a data source provided by the teacher where the context of this was a csv of data with different types of information. This csv was used for all the work, where we had to make a connection to a database manager using the python programming language. This would also involve creating a database and a table to store the data source information.

This was not a cleaning process since the data source was ready to be used at the beginning of the process.

The status of this project is finished, all the points that were requested have been done, through a jupyter notebook, and a visualization in POWER Bi.

## Content of the project

This project contains 3 files in itself, very simple each one for the easy elaboration and implementation of the project.
1. Workshop.ypynb: A jupyter notebook in which all the process for the connection to the database manager, the creation of the database and the tables as such, as well as the injection of the data to these tables (tables in general because later we will show a process that involves creating a new table).
2. candidates.csv: This file is our data source, a CSV type, where we store all our data separated by commas.
3. credentials.json : This is a file that you must manage yourselves when running the code, since for security reasons I can not provide my credentials to access the database, and an error would occur since they are not the same credentials with your database, later you will be shown the process so you can run this without any problem.

As a bonus when inserting the data to the tables, a new file called candidates2.csv will be created, which contains the information for the second table.

## Instalation and configuration

The commands to download this project are the basic ones...

- Create a folder where you will store the project
- Open it with your favorite (code manager) in this case we will use Visual Studio Code.
- Create a new terminal
- Do a git commit https://github.com/JuancaBurbano/workshop1

And ready you have the project, now you must run it, for this to happen without any problem this is what you should do...

The first thing to do is to go to the workshop.ipynb notebook which contains the information necessary for that functions. This notebook is explained step by step in each cell how to apply the code, likewise in this readme I will also provide you with this information.

- Install the libraries: The first cell that appears in the notebook is about the libraries that we are going to use in this project (You must run this cell).
- Create your credentials.json file: As the name suggests, you must create this file "credentials.json", it will have the following information...
```
{
    "host" : "localhost",
    "user" : "",
    "password" : "",
    "database" : ""  
}

```

Fill in the json information with yours, but do not put anything in the database yet, because we have not created it yet.

- This project has MySQL as database manager, so if you don't have it yet, download it and do the installation process, you can download it through the following link: (https://dev.mysql.com/downloads/installer/) 


- Continuing, already having the database manager we are going to proceed to the connection. The following code cell, makes the connection bringing the json that we have as credentials to use those "credentials" at the moment of making the connection.
(Run the cell)

- Now that we have the connection to the manager, let's create the database with which we will work and the main table, to run this code cell you should not configure anything, just run it, you would be left with a database called workshopdb1 and with the table candidates, with the corresponding columns.
(Run the cell)

- After the previous step and after having created the database, we can now configure it in credentials.json.

```
{
    "host" : "localhost",
    "user" : "",
    "password" : "",
    "database" : "workshopdb1"  
}

```
This should be the json, clearly in user and password, your credentials, after having configured the json again, save it and go to the notebook, you can run the next cell without problem.
(Run the cell)

- We already have the connection to the manager, we have already created the database, and we already have the table with data, we will proceed to make an EDA to this table that we have left, for the following EDA cells you should not make any configuration, just run the cells and you can see the conclusions reached by doing the Exploratory Data Analysis.

- Creation of the new table: After having finished the EDA we are asked to create a new table where the candidates that in the columns TechnicalviewScore and CodeChallengeScore are greater than 7, a new column will be created in this new table that approves the candidate in binary numbers 0 and 1. Where 1 means that if I applied and 0 means that I did not. Then we run without any problem the cells that verify the candidates with these results.
(Run the cell)

- We add the table: We do the same process as when creating the first table, it is done automatically with the .cursor so you only have to run the cell to create this new table in the database.
(Run the cell)

- Creation of candidates2.csv: We import this new dataframe that was left with the new column to a csv that later we will load to the new table.
(Run the cell)

- We import the data: The last cell that we have left is the import of the data to our new table, because as at the beginning we imported the csv candidates to the table, we relizamos the same process for the second table, you only have to run the cell that already the process becomes automatic.
(Run the cell)

## Functional tests

In the previous point we showed the step by step of how to run this project, this will show the tests and outputs that are performed at the time of running the project.

The graphical samples are available in the following document or also in the report: (https://docs.google.com/document/d/1uYlP_68EkMxUuMG5akHnbwSeNw25LtWMjek6rTcp234/edit?usp=sharing)
 
## Conclusiones


