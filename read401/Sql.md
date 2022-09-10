
## What is Structured Query Language (SQL)?

Structured Query Language (SQL) is a standardized programming language that is used to manage relational databases and perform various operations on the data in them. Initially created in the 1970s, SQL is regularly used not only by database administrators, but also by developers writing data integration scripts and data analysts looking to set up and run analytical queries.


## SQL commands are divided into several different types, including the following:

Data Definition Language (DDL) commands are also called data definition commands because they are used to define data tables.
Data Manipulation Language (DML) commands are used to manipulate data in existing tables by adding, changing or removing data. Unlike DDL commands that define how data is stored, DML commands operate in the tables defined with DDL commands.
Data Query Language consists of just one command, SELECT, used to get specific data from tables. This command is sometimes grouped with the DML commands.
Data Control Language commands are used to grant or revoke user access privileges.
Transaction Control Language commands are used to change the state of some data -- for example, to COMMIT transaction changes or to ROLLBACK transaction changes.

SQL SELECT. The SELECT command is used to get some or all data in a table.
SQL CREATE. The CREATE command is used to create a new SQL database or SQL table. Most versions of SQL create a new database by creating a new directory, in which tables and other database objects are stored as files.
SQL DELETE. The DELETE command removes rows from a named table. 
SQL INSERT INTO. The INSERT INTO command is used to add records into a database table.
SQL UPDATE. The UPDATE command is used to make changes to rows or records in a specific table.

## What's the difference between SQL  and NoSQL?
SQL, which stands for “Structured Query Language,” is the programming language that’s been widely used in managing data in relational database management systems (RDBMS) since the 1970s. In the early years, when storage was expensive, SQL databases focused on reducing data duplication.

Fast-forward to today, and SQL is still widely used for querying relational databases, where data is stored in rows and tables that are linked in various ways. One table record may link to one other or to many others, or many table records may be related to many records in another table. These relational databases, which offer fast data storage and recovery, can handle great amounts of data and complex SQL queries.

## Sequelize
Sequelize is a Node.js-based Object Relational Mapper that makes it easy to work with MySQL, MariaDB, SQLite, PostgreSQL databases, and more. An Object Relational Mapper performs functions like handling database records by representing the data as objects. Sequelize has a powerful migration mechanism that can transform existing database schemas into new versions. Overall, Sequelize provides excellent support for database synchronization, eager loading, associations, transactions, and database migrations while reducing development time and preventing SQL injections.


## How to use it with Node js ?
INSTALL DEPENDENCIES

npm install sequelize sqlite3
DEFINE MODELS

import { Sequelize, Model, DataTypes } from 'sequelize';

const sequelize = new Sequelize('sqlite::memory:');
const User = sequelize.define('User', {
  username: DataTypes.STRING,
  birthday: DataTypes.DATE,
});

PERSIST AND QUERY

const jane = await User.create({
  username: 'janedoe',
  birthday: new Date(1980, 6, 20),
});

const users = await User.findAll();



## What Does (ORM) Mean?
Object-relational mapping (ORM) is a programming technique in which a metadata descriptor is used to connect object code to a relational database. Object code is written in object-oriented programming (OOP) languages such as Java or C#. ORM converts data between type systems that are unable to coexist within relational databases and OOP languages.


## How does ORM work?
ORMs create a model of the object-oriented program with a high-level of abstraction. In other words, it makes a level of logic without the underlying details of the code. Mapping describes the relationship between an object and the data without knowing how the data is structured. The model can then be used to connect the application with the SQL code needed to manage data activities. This “plumbing” type of code does not have to be rewritten, saving the developer a tremendous amount of time.

database schema defines how data is organized within a relational database; this is inclusive of logical constraints such as, table names, fields, data types, and the relationships between these entities.

WRRC :
The request/response cycle traces how a user's request flows through the app.
Understanding the request/response cycle is helpful to figure out which files to edit when developing an app
(and where to look when things aren't working).



Which 3 things had you heard about previously and now have better clarity on?
SQL , WRRC , CRUD system.

Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
SQL queries , Sequelize , Middlewares

What are you most excited about trying to implement or see how it works?
The Sequelize and ORM .

Resources :
[SQL database](https://www.techtarget.com/searchdatamanagement/definition/SQL)
[Sequelize](https://sequelize.org/)
[ORM](https://www.techopedia.com/definition/24200/object-relational-mapping--orm)
[CRUD system](https://zellwk.com/blog/crud-express-mongodb/)
[altexsoft](https://www.altexsoft.com/blog/object-relational-mapping/)