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

Key components of a table include: schema, column (field), row (record), keys, constraints.

### Entity:
In the context of databases and data modeling, an *entity* is a real-world object, concept, or thing that can be distinctly identified and about which data can be stored. An entity is represented or implemented in a database as a table.  

Think of an entity as a noun (a person, place, thing, or event) that is important to your business or application and about which you need to store information.  

#### Examples of entities:
- **Person:** `Customer`, `Employee`, `Student`
- **Place:** `Store`, `Office`, `Warehouse`
- **Thing:** `Product`, `Machine`, `Book`
- **Event:** `Order`, `Sale`, `Appointment`, `Shipment`  

Each instance (or occurrence) of an entity becomes a record (or row) in the database table.
- The entity `Customer` is implemented as the `Customers` table.
- A specific customer, "Alice Smith", is a single row in that table.

#### Characteristics of an Entity:
1. **Attributes:** These are the properties or characteristics that describe the entity. In a database table, attributes become the columns.
    - For a `Product` entity, its attributes could be `ProductID`, `ProductName`, `Price`, and `Category`.
2. **Unique Identifier:** Every entity must have an attribute (or a set of attributes) that uniquely identifies each instance. This becomes the *primary key* in the table.
    - For a `Customer` entity, the unique identifier is often a `CustomerID`.

### Columns:
In a database table, a *column* defines a specific type of information or attribute that is stored for every record in that table. It represents a single, consistent category of data.  

Think of it like a header in a spreadsheet or a field on a form.

#### Key Characteristics of a Column:
1. **Name:** Every column must have a unique name within its table.
2. **Data Type:** This is the most important property. It defines the kind of data the column can hold.
3. **Constraints:** Optional rules that enforce data integrity and define relationships.

Columns are fundamental because they define the structure of the table, enforce data integrity, enable relationships and allow efficient querying.

### Rows:
In a database table, a *row* is a single, horizontal entry that represents a complete record of information. It contains a set of related data values, one for each column defined in the table.

A row is basically a unique horizontal entity in a table that represents and instance. In database theory, a row is formally called a **tuple**. In everyday language, it's often called a **record**.

#### The Role of Rows in a Relational Database:
Rows are crucial because they:
1. **Hold the Actual Data:** While columns define the structure, the rows contain the real, stored data. Without rows, a table is just an empty shell.
2. **Are the Unit of Operation:** When you Insert, Update, or Delete data (using DML commands), you typically do so one row at a time or on a set of rows.
3. **Are the Result of Queries:** When you execute a `SELECT` query, the results are returned as a set of rows.
