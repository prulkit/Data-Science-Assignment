Q1. What is a database? Differentiate between SQL and NoSQL databases.

Q2. What is DDL? Explain why CREATE, DROP, ALTER, and TRUNCATE are used with an example.

Q3. What is DML? Explain INSERT, UPDATE, and DELETE with an example.

Q4. What is DQL? Explain SELECT with an example.

Q5. Explain Primary Key and Foreign Key.

Q6. Write a python code to connect MySQL to python. Explain the cursor() and execute() method.

Q7. Give the order of execution of SQL clauses in an SQL query.

## Ans1
A database is an organized collection of structured information, or data, typically stored electronically in a computer system. A database is usually controlled by a database management system (DBMS).


### SQL

RELATIONAL DATABASE MANAGEMENT SYSTEM (RDBMS).	

These databases have fixed or static or predefined schema.	

These databases are not suited for hierarchical data storage.	

These databases are best suited for complex queries.

Vertically Scalable.	

Follows ACID property.	

Examples: MySQL, PostgreSQL, Oracle, MS-SQL Server, etc.	




### NoSQL

Non-relational or distributed database system.

They have dynamic schema.

These databases are best suited for hierarchical data storage.

These databases are not so good for complex queries.

Horizontally scalable.

Follows CAP(consistency, availability, partition tolerance).

Examples: MongoDB, GraphQL, HBase, Neo4j, Cassandra, etc.
## Ans 2
Data Definition Language(DDL) is a subset of SQL and a part of DBMS(Database Management System). DDL consist of Commands to commands like CREATE, ALTER, TRUNCATE and DROP. These commands are used to create or modify the tables in SQL

CREATE :
This command is used to create a new table in SQL. The user has to give information like table name, column names, and their datatypes.

Exa:
CREATE TABLE Student_info
(
College_Id number(2),
College_name varchar(30),
Branch varchar(10)
);

ALTER :
This command is used to add, delete or change columns in the existing table. The user needs to know the existing table name and can do add, delete or modify tasks easily.

Exa:
ALTER TABLE Student_info
ADD CGPA number

TRUNCATE :
This command is used to remove all rows from the table, but the structure of the table still exists.

Exa:
TRUNCATE TABLE Student_info;

DROP :
This command is used to remove an existing table along with its structure from the Database.

Exa: 
DROP TABLE Student_info;

## Ans 3
The data manipulation language statements are used to retrieve, add, delete, and modify the data that is stored in the objects of database. The keywords or statements that are associated with the data manipulation language are: SELECT INSERT, UPDATE and DELETE. These are the primary statements of data manipulation language (DML) and are used widely
INSERT Command
To add data to a table the INSERT command is used. The syntax of the INSERT command is given below:

INSERT into table-name values (data, data …)

Update Command:
To update a table or row or column in the table we use the update command. The syntax of update command is given below:

Update table-name set column-name = value where condition;

Delete Command
To delete a table row or some data from a table in the database the delete command is used. The syntax of delete command is as follows:

DELETE from table-name;

Select command
Select command is used to retrieve data from the database.The syntax for the select command is as follows:

SELECT * from <table_name>;
## Ans 4
DQL is a portion of a SQL statement that allows you to get and organise data from a database. You can use the SELECT command to extract data from a database in order to perform actions on it. It is the same as the projection operation in relational algebra. The result of a SELECT statement on a table or collection of tables is compiled into a new temporary table, which is subsequently displayed or received by a program,

Example

SELECT Stu_Name FROM Student WHERE Phone = 9039462908;

## Ans 5
The primary key is an attribute or a set of attributes that uniquely identify a specific instance of an entity. Every entity in the data model must have a primary key whose values uniquely identify instances of the entity.

To qualify as a primary key for an entity, an attribute must have the following properties:

It must have a non-null value for each instance of the entity
The value must be unique for each instance of an entity
The values must not change or become null during the life of each entity instance.



A foreign key is an attribute that completes a relationship by identifying the parent entity. Foreign keys provide a method for maintaining integrity in the data (called referential integrity) and for navigating between different instances of an entity. Every relationship in the model must be supported by a foreign key.
## Ans 6

The MySQLCursor of mysql-connector-python (and similar libraries) is used to execute statements to communicate with the MySQL database.

Using the methods of it you can execute SQL statements, fetch data from the result sets, call procedures.

You can create Cursor object using the cursor() method of the Connection object/class.

Example
import mysql.connector

#establishing the connection
conn = mysql.connector.connect(
   user='root', password='password', host='127.0.0.1', database='mydb'
)
#Creating a cursor object using the cursor() method
cursor = conn.cursor()


## Ans 7

Order of Execution
SQL queries adhere to a specific order when evaluating clauses, similar to how mathematical operations adhere to PEMDAS or BIDMAS.

From the eyes of the user, queries begin from the first clause and end at the last clause. However, queries aren’t actually read from top to bottom when carried out.

The order in which the clauses in queries are executed is as follows:

1. FROM/JOIN: The FROM and/or JOIN clauses are executed first to determine the data of interest.

2. WHERE: The WHERE clause is executed to filter out records that do not meet the constraints.

3. GROUP BY: The GROUP BY clause is executed to group the data based on the values in one or more columns.

4. HAVING: The HAVING clause is executed to remove the created grouped records that don’t meet the constraints.

5. SELECT: The SELECT clause is executed to derive all desired columns and expressions.

6. ORDER BY: The ORDER BY clause is executed to sort the derived values in ascending or descending order.

7. LIMIT/OFFSET: Finally, the LIMIT and/or OFFSET clauses are executed to keep or skip a specified number of rows.




```python

```
