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

## Types of Databases:
### Relational Databases (SQL Databases):
This is the most traditional and common type. They organize data into tables (like spreadsheets) made of rows and columns.
- **Core Concept:** Data is structured and follows a pre-defined schema (a blueprint of how the data is organized, including tables, columns, data types, and relationships). They use SQL (Structured Query Language) to manage and query the data.
- **Strength:** ACID Compliance (Atomicity, Consistency, Isolation, Durability). This guarantees that database transactions are processed reliably and ensures data integrity. Excellent for complex queries and managing relationships between data points (e.g., customers and their orders).
- **Weakness:** The rigid schema can make them less flexible if your data structure needs to change frequently. They can also be difficult to scale horizontally (across multiple servers).
- **Best For:** Applications where data integrity and relationships are critical. Examples: accounting systems, customer relationship management (CRM) software, e-commerce transaction systems.
- **Examples:** MySQL, PostgreSQL, Microsoft SQL Server, Oracle Database, SQLite.

### Non-Relational Databases (NoSQL Databases)
This is a broad category that includes any database that doesn't use the traditional table-based relational model. They are often more flexible and designed for large-scale, rapidly changing data.  

They are further divided into several types:
1. **Object-Oriented Databases:** Data stored in form of objects.
2. **Graph Databases:** Data stored in form of nodes.
3. **Document Databases:** Data stored as JSON objects.
4. **Key-Value Databases:** Each item is stored as a key (a unique identifier) paired with its value (the data itself).
5. **Column-Family (Wide-Column) Databases:** Store data in tables, rows, and dynamic columns, but unlike relational DBs, each row is not required to have the same columns. Data is stored by column rather than by row, which is very efficient for querying specific fields across massive datasets.
6. **Time-Series Databases (TSDB):** Optimized for storing and querying data points that are time-stamped, like sensor readings, stock prices, or application metrics.

## Big Data
**"Big Data"** is a term that describes datasets that are so large, complex, and fast-growing that traditional data processing tools (like a single relational database) can no longer capture, store, manage, or analyze them effectively.

It's not just about having a lot of data. It's about data that has passed a certain threshold of volume, speed, and complexity that requires new tools and approaches.

### The Core of Big Data:
The concept is best understood through its defining characteristics, often called the V's of Big Data.
1. **Volume:** The sheer amount of data.
This is the most obvious characteristic. We're talking about terabytes, petabytes, and even exabytes of data. Eg. Years of stock market tick data, all the videos on YouTube, terabytes of logs from a web server farm.
2. **Velocity:** The speed at which new data is generated and the pace at which it must be processed.
Data often streams in continuously and must be analyzed in near-real-time. Eg. Twitter feeds, financial trading systems, real-time sensor data from IoT devices, live traffic updates in Google Maps.
3. **Variety:** The different types and formats of data.  
Big Data is rarely neat and structured. It comes in all forms:
- **Structured:** Traditional rows and columns (e.g., spreadsheets, SQL tables).
- **Unstructured:** No pre-defined format (e.g., emails, social media posts, videos, photos, audio recordings).
- **Semi-structured:** Has some organizational properties (e.g., JSON, XML, log files).  
**Example:** A company's data might include structured sales records, unstructured customer service emails, and semi-structured website clickstream logs.
