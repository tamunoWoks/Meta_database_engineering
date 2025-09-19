## SQL
**SQL (Structured Query Language)** is the standard programming language used to communicate with and manipulate relational databases. You use SQL to:
- Ask questions about the data (queries).
- Add new data.
- Update existing data.
- Delete data.
- Create and modify the structure of the database itself (tables, views, etc.).  

It is the fundamental tool for anyone working with data, from analysts and developers to data scientists and administrators.

### SQL Dialects:
A "dialect" is a variant of SQL that is specific to a particular database management system (DBMS). While all SQL dialects are based on the same core standard (ANSI SQL), each vendor adds its own unique features, functions, and slight syntactic variations. The major dialects include:
- Microsoft SQL Server
- PostgreSQL
- Oracle Database
- MySQL

**The important thing to remember:** Core SQL commands like SELECT, FROM, WHERE, INSERT, UPDATE, and DELETE work almost identically across all dialects. The differences become more apparent with advanced functions, date manipulation, and procedural code.

### What is the Advantage of SQL?
SQL has remained the dominant language for data for over four decades for several powerful reasons:
- Declarative Nature
- Standardization and Universality
- Powerful Data Manipulation
- Ability to Handle Complex Relationships
- Security and Access Control

## DBMS (Database Management System)
A DBMS (Database Management System) is specialized software designed to create, manage, and interact with databases. In simpler terms, if data is the content of a library, the DBMS is the librarian, the indexing system, and the rules for checking out books, all rolled into one.

### Key Functions of a DBMS:
A DBMS doesn't just store data; it performs several critical jobs:
- **Data Management:** It provides a systematic way to create, retrieve, update, and delete data (often called CRUD operations).
- **Data Security:** It controls who can access what data through user accounts, permissions, and roles.
- **Data Integrity:** It enforces rules to ensure data is accurate and consistent (e.g., using primary keys, foreign keys, and data type validation).
- **Backup and Recovery:** It provides tools to back up data and restore it in case of a system failure, preventing data loss.
- **Concurrency Control:** It allows multiple users to access the database simultaneously without interfering with each other, ensuring that data remains consistent.
- **Data Abstraction:** It provides a simple interface for users and applications to interact with the data, hiding the complex underlying storage details.

### Types of DBMS with Examples:
DBMS can be categorized based on how they organize data. The primary models are:
1. **Relational DBMS (RDBMS):**  
This is the most common type. It organizes data into tables (rows and columns) and uses SQL for querying. Relationships between tables are enforced. Eg. MySQL, PostgreSQL, Microsoft SQL Server, Oracle Database, SQLite.
2. **NoSQL DBMS:**  
This is a broad category for databases that don't use the traditional table-based relational model. They are designed for specific data models like documents, key-value pairs, graphs, or wide columns. Eg. MongoDB, Redis, Apache Cassandra, Neo4j.
3. **NewSQL DBMS:**  
A modern class of DBMS that aims to provide the same scalable performance as NoSQL systems while maintaining the ACID guarantees and SQL interface of traditional RDBMS. Eg. Google Spanner, Cockroach DB.
4. **In-Memory DBMS:**  
A DBMS that primarily relies on main memory (RAM) for data storage, rather than disk. This makes data retrieval incredibly fast. Eg. Redis, MemSQL.

### CRUD Opearations:
CRUD operations are the four basic functions that any persistent storage application must be able to perform. They are the foundation of almost every interaction with a database.  
The acronym CRUD stands for:
- Create
- Read
- Update
- Delete.  

These operations map almost directly to the core commands in the SQL language and are fundamental to API design (like RESTful APIs) and any application that interacts with data. It maps directly to SQL commands (INSERT, SELECT, UPDATE, DELETE) and HTTP methods (POST, GET, PUT, DELETE).

### DDL (Data Definition Language):
DDL stands for Data Definition Language. It is a subset of SQL commands used to define, modify, and manage the structure of database objects, such as tables, indexes, and views. While other parts of SQL work with the data inside the tables, DDL is used to create and change the tables themselves—the blueprint or schema of the database.  

The most fundamental DDL commands are:
- `CREATE`
- `ALTER`
- `DROP`
- `TRUNCATE`
- `RENAME`

### DML (Data Manipulation Language)
DML stands for Data Manipulation Language. It is the subset of SQL commands used for managing, manipulating, and retrieving the data stored within the database structures created by DDL.  

DML operations are famously known as CRUD operations:
- Create (`INSERT`)
- Read (`SELECT`)
- Update (`UPDATE`)
- Delete (`DELETE`)

