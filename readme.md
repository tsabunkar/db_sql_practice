# Database

- DB is a colllection of data (ex - phonebook) but DB Should also provide methods for accessing and manipulating that data
- The data relating to each other by nature, e.g., a product belonged to a product category and associated with multiple tags. Therefore, we use the term relational database.
- DBMS ( Database Management System) :-

  Web Application ----> DBMS ----> Database

- Generally our application talks/Give commands/queries to DBMS, which in-turn queries to Database
- Commonly, Database is referred as both DBMS and Actual DB
- PostgreSQL, Oracle database, MySQL, SQLite, etc are not technically DB, but its actually Database Management System DBMS but in common we refer it as Database
- Thus a database is a structured set of computerized data with an accessible interface

---

# MySQL v/s SQL

- SQL : Structured Query Language
  - SQL is the 'Language' we use to 'talk' to our database
  - It is the way we interact or access, update or delete the data from the DB

ex- Find all users, Find all users who are 18 years old, Add a new user with username 'Tejas', Delete every single user

- MySQL : is the 3rd party RDBMS vendor which provides the Database management system, This data can be accessed using SQL language
- Working with MySQL is primarly working with SQL
- SELECT \* FROM Users WHERE Age >= 18 ----> MySQL Database
  SELECT \* FROM Users WHERE Age >= 18 ----> PostgreSQL Database
- SQL have standards, where all the DBMS vendor should follow. Thus we can think SQL as Theory/standards where as, MySQL is DBMS Vendor which implement SQL Standards

---

NOTE

- Onces learned SQL its pretty easy to switch from one DB to another DB that uses SQL
- What makes DBMS Unique are the features they offer, not the Language (i.e- SQL)
- MySQL is open source software backed by Oracle.

---

# SQL

- SQL – the language of the relational database
- SQL is the standardized language used to access the database.
- ANSI/SQL defines the SQL standard.

- SQL contains 3 parts:

  - Data definition language includes statements that help you define the database and its objects, e.g., tables, views, triggers, stored procedures, etc.
  - Data manipulation language contains statements that allow you to update and query data.
  - Data control language allows you to grant the permissions to a user to access specific data in the database.

---

# DB Server :

- One database server can have multiple databases- for ex- In mysql db server we can have sys db, practice db, company db, etc

---

# TABLES

- DB is just bunch of tables (In relational databases)
- Tables : A collection of related data held in a structured format within a db
- Tables consist of rows and column:
  - Column : headers/Meta-data [Information of Data]
  - Rows : The actual data (Each object)
- Table name should be plural not singular, for ex - employees, tweets, etc

---

# DataTypes

- Numeric Type :
  - INT
  - SMALLINT
  - TINYINT
  - MEDIUMINT
  - BIGINT
  - DECIMAL
  - NUMERIC
  - FLOAT
  - DOUBLE
  - BIT
- String Type :
  - CHAR
  - VARCHAR (A Variable length String)
  - BINARY
  - VARBINARY
  - BLOB
  - TINYBLOB
  - MEDIUMBLOB
  - LONGBLOB
  - TEXT
  - TINYTEXT
  - MEDIUMTEXT
  - LONGTEXT
  - ENUM
- Date Types :
  - DATE
  - DATETIME
  - TIMESTAMP
  - TIME
  - YEAR
- varchar(100) : If we specifiy the column with datatype as varchar(100) which means limiting the number of characters to be 100, if we go beyond the 100 chars then only from 1st character to 100th character string would be stored

---

# NULL

- NUll : The value is not known
- Null does not means zero
- INSERT INTO table_name() VALUES(); ==> Will insert NULL
- How to prevent NULL a particular column ?
  - We need to specifiy the column as NOT NULL
  - CREATE TABLE cat2
    (
    name VARCHAR (100) NOT NULL
    );
- If the column is null, then even though we dont provide the value: We get error - Field 'name' doesn't have a default value
  - INSERT INTO cat2() VALUES();

---

# DEFAULT

- Set the default values/ fallback values
- CREATE TABLE cat3
  (
  name VARCHAR (100) DEFAULT 'unnamed',
  age INT DEFAULT 99
  );

  INSERT INTO cat3() VALUES();

- CREATE TABLE cat4
  (
  name VARCHAR (100) NOT NULL DEFAULT 'unnamed',
  age INT NOT NULL DEFAULT 99
  ); ==> We are writing not null bcoz - We could still manually make a record as null by specifing explicitly NULL ex-
  INSERT INTO cat3 (name, age) VALUES ('Gosh', NULL)

---

# Key

- To remove the identical data, To make data unique ==> Column should be made as Primary Key
- For ex- emailID column, Mobile number, UUID, or some type of unique identifiers etc
- Primary Key ==> A unique identifier on ROW
- To Generate the ID Automatically:- AUTO_INCREMENT

---

# Read

- SELECT \* FROM table_name -> star means "Give me all columns"
- SELECT Expression : Specific columns we want to show/project

---

# Update

- Thumb rule : Try selecting data before you UPDATE
- There is no undo for update onces it is done, so it better to confirm/view before what we are updating

---

# WHERE

- The WHERE clause, is used to filter the row/data
- Thus WHERE is used to Get specific data
- ex- SELECT \* FROM cats WHERE age =4;
  SELECT \* FROM cats WHERE name ='Egg';
- By default WHERE caluse value is CASE INCENSITIVE, which means-

---

# AGGREGATE

Aggregate functions are builtin function in mysql which will allow us to aggregate/combine data
like avg, count, groupby, etc

---
