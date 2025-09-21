## Tables
In a relational database, a *table* is a collection of related data organized into a structured format of rows and columns. It's the primary and simplest way to store data.  

A single database can contain multiple tables, each storing data for a different entity (e.g., a Customers table, an Orders table, a Products table).

#### Why are Tables Important?
Tables are the building blocks of a relational database because they:
1. **Provide Structure:** The column definitions enforce a consistent structure for all data entered. Every record must fit the defined format.
2. **Organize Data:** They allow you to group related information together logically (e.g., all customer data in one table, all order data in another).
3. **Enable Relationships:** This is the "relational" part. Tables can be linked together using Primary Keys and Foreign Keys. For example, an Orders table can have a CustomerID column that links back to the Customers table, connecting an order to the customer who placed it.
4. **Facilitate Efficient Querying:** The structured format makes it easy to search, sort, filter, and manipulate data using SQL.

### Schema:
A *schema* is the blueprint or structure of a database. It defines how the data is organized, how the relationships between data are defined, and the rules that enforce data integrity.  

The schema doesn't contain the actual data itself. Instead, it defines:
- What tables exist. 
- What columns are in each table.
- The data type of each column.
- The rules (constraints) for the data. (e.g., CustomerID must be unique and not null—this is a primary key).
- The relationships between tables.

### Entity:
In the context of databases and data modeling, an *entity* is a real-world object, concept, or thing that can be distinctly identified and about which data can be stored. An entity is represented or implemented in a database as a table.  

Think of an entity as a noun (a person, place, thing, or event) that is important to your business or application and about which you need to store information.  

**Examples of entities:**
- **Person:** `Customer`, `Employee`, `Student`
- **Place:** `Store`, `Office`, `Warehouse`
- **Thing:** `Product`, `Machine`, `Book`
- **Event:** `Order`, `Sale`, `Appointment`, `Shipment`
