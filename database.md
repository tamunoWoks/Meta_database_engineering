### Database
A database is a form of electronic storage in which data is organized and held systematically to make it more manageable, efficient and secure.

### Database tasks:
- Store data
- Form data relationships
- Filter data
- Search data
- Perform CRUD operations

### Data:
At its core, data is a collection of raw, unorganized facts and details. These facts can be anything—numbers, words, observations, measurements, symbols, or even just descriptions of things.  

Think of it as the basic building blocks of information. By itself, a single piece of data might not mean much. It needs to be processed, organized, and structured to become useful.

Data is stored systematically, and these are the characteristics of systematic data:
- Identifiable features or attributes.
- Stored in entities eg. Tables

### Types of Database Systems:
1. **Object-Oriented Databases:** Data stored in form of objects.
2. **Graph Databases:** Data stored in form of nodes.
3. **Document Databases:** Data stored as JSON objects.
   
Databases are hosted:
- Dedicated machine on site.
- Cloud hosting.

### Cloud Hosting:
Cloud hosting in relation to databases means leveraging the infrastructure and services of a cloud provider like Amazon Web Services, Google Cloud, or Microsoft Azure to run your database instead of on your own physical hardware in a server room.  

It transforms a database from a piece of software you must maintain into a managed utility that you simply use, allowing developers to focus on building applications rather than managing hardware and software.

### Primary Key:
A *primary key* is a special field in a database table that uniquely identifies each record in that table. Its main job is to ensure data integrity by preventing duplicate records and providing a reliable way to find, reference, and link specific pieces of data.

#### Key Characteristics of a Primary Key:
For a field (or set of fields) to be a primary key, it must adhere to three strict rules:
- **UNIQUE:** No two rows can have the same primary key value. This ensures each record is distinct.
- **NOT NULL:** The primary key field must always have a value. It cannot be empty or unknown (NULL).
- **STABLE:** The value should ideally never change. Changing a primary key can be complex and cause problems in other parts of the database that reference it.

### Foreign Key:
A *foreign key* is a field (or collection of fields) in one table that uniquely identifies a row in another table. It is a column in one table that points to the primary key in another table. This link establishes a relationship between the two tables.

### Types of Databases:
### Relational Databases (SQL Databases):
This is the most traditional and common type. They organize data into tables (like spreadsheets) made of rows and columns.
- **Core Concept:** Data is structured and follows a pre-defined schema (a blueprint of how the data is organized, including tables, columns, data types, and relationships). They use SQL (Structured Query Language) to manage and query the data.
- **Strength:** ACID Compliance (Atomicity, Consistency, Isolation, Durability). This guarantees that database transactions are processed reliably and ensures data integrity. Excellent for complex queries and managing relationships between data points (e.g., customers and their orders).
- **Weakness:** The rigid schema can make them less flexible if your data structure needs to change frequently. They can also be difficult to scale horizontally (across multiple servers).
- **Best For:** Applications where data integrity and relationships are critical. Examples: accounting systems, customer relationship management (CRM) software, e-commerce transaction systems.
- **Examples:** MySQL, PostgreSQL, Microsoft SQL Server, Oracle Database, SQLite.
