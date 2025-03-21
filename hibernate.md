##Hibernate Framework
======================
```

This framework is an ORM(Object Relational Mapping) tool
It is a lightweight framework 
It will perform database related operation for our application 
It calls JDBC API internally to perform database related operations
It will perrform following tasks:
1) Loading driver class 
2) Creating connection object 
3) Creating statement objects
4) Creating SQL queries
5) Executing SQL queries
etc.

Hibernate is implementation of JPA (Java Persistence API) 

________________________________________

How to use hibernate in java project ?
________________________________________

1) Create maven project
2) Configure dependencies in pom.xml
3) Create persistence or model class 
4) Create HBM file 
5) Create CFG file
6) Create repository class

Step1:
What is maven?
It is one the build tool
Build tools are very useful tools for developer
It helps developer in application development such as
1) Creating directory structure of the project
2) Downloading project dependencies (external jar files) and adding them into project
3) Compiling source code of the project
4) creating partial unit testing code 
etc

Step2: 
Configure dependencies in pom.xml
______________________________________
Required dependencies added such as
1) Hibernate- core
2) Mysql-connector

Step3:
Creating persistent class 
_________________________________
Object of this model class will be saved/persisted by hibernate into database table.
Persisting object means saving sates of the object into table as a record 
This class must be java POJO class
POJO stands for plain old java Object
POJO class must have:
1) private instance variables
2) No-arguement constructor/non-parameterzied constructor
3) Getter and setter

Step4:
Create HBM file 
____________________
This must be an xml file
In this file you will have to map persistent class with database 
table
Instance variables of this class will be mapped with columns of the table 
Keep this file in scr folder


Step5:
Create CFG file
____________________
This must be an xml file 
In this file we need to configure following information
1) HBM2DDL auto property
2) Show-sql property
3) Dialect property
4) Database connection information (driver class name, url, username, password)
5) hbm file name 
etc
This file in scr folder

Step6:
Create repository class
________________________
This is also known as Dao class
In thia class you will have to write code to perform database operation.
You need to create following objects and call methods
1) Object of SessionFactory interface
2) Object of Session interface 
3) Object of Transaction interface
etc.
Object of SessionFactory interface keeps information of both cfg and hbm file
DDL operation will be performed by SessionFactory interface 
Object of Session interface will be created by 
openSession() method of SessionFactory interface
call methods of session interface to perform CRUD operation
(persisting object, deleting object, getting object , etc)




```