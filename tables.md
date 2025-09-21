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

### Data Types:
In a database, a *data type* is an attribute that specifies the type of data that a column can hold. It defines the possible values for that column and the operations that can be performed on them.  

Data types are crucial because they:
- Ensure data integrity (you can't put a name in a price field).
- Optimize storage space (a number is stored more efficiently than text).
- Enable proper operations and calculations (you can add two numbers, but adding two phone numbers as text doesn't make sense).

Data types can be grouped into several categories. Here are the most common ones you will encounter:
#### 1. Numeric Types:
For storing numbers. 

| Data Type | Description | Example |
| :--- | :--- | :--- |
| **`INT` / `INTEGER`** | Whole numbers, positive or negative. | `42`, `-7`, `15000` |
| **`DECIMAL(p, s)`** | Exact numbers with fixed precision and scale. Essential for financial data. `p` is total digits, `s` is digits after the decimal. | `12345.67` is `DECIMAL(7,2)` |
| **`NUMERIC(p, s)`** | Functionally identical to `DECIMAL`. | `999.99` is `NUMERIC(5,2)` |
| **`FLOAT` / `REAL`** | Approximate numerical, floating-point numbers. Use for scientific data. | `3.14159`, `2.5e10` |
| **`SMALLINT`** | Smaller range integer. Uses less space. | `-32768` to `+32767` |
| **`BIGINT`** | Larger range integer. Uses more space. | `-2^63` to `2^63-1` |

#### 2. Character/String Types:
For storing text.

| Data Type | Description | Example |
| :--- | :--- | :--- |
| **`CHAR(n)`** | Fixed-length character string. Padded with spaces. | `'ABC '` (for `CHAR(5)`) |
| **`VARCHAR(n)`** | **Most common.** Variable-length string. `n` is max length. | `'Hello'` (for `VARCHAR(100)`) |
| **`TEXT`** | For very long strings of variable length. | A long article or description. |

#### 3. Date and Time Types:
For storing temporal data.

| Data Type | Description | Example |
| :--- | :--- | :--- |
| **`DATE`** | Stores a date (year, month, day). | `'2023-10-27'` |
| **`TIME`** | Stores a time (hours, minutes, seconds). | `'14:30:00'` |
| **`DATETIME`** | Stores both a date and a time. | `'2023-10-27 14:30:00'` |
| **`TIMESTAMP`** | Often timezone-aware. Stores date and time. | `'2023-10-27 14:30:00 UTC'` |
| **`INTERVAL`** | Represents a span of time. | `'2 days'`, `'5 hours'` |

#### 4. Boolean Type:
For storing true/false values.

| Data Type | Description | Example |
| :--- | :--- | :--- |
| **`BOOLEAN`** | Represents a logical state. | `TRUE`, `FALSE`, `1`, `0` |

#### 5. Binary Types:
For storing raw bytes (e.g., images, files).

| Data Type | Description | Example |
| :--- | :--- | :--- |
| **`BLOB`** | Binary Large Object. For large binary data. | Image files, PDF documents |
| **`BINARY(n)`** | Fixed-length binary data. | `0x4A6F686E` |
| **`VARBINARY(n)`** | Variable-length binary data. | `0x4A6F686E` |

#### 6. Specialized Types:

| Data Type | Description | Example |
| :--- | :--- | :--- |
| **`JSON`** | Native support for storing and querying JSON data. | `{"name": "John", "age": 30}` |
| **`XML`** | Stores XML data. | `<user><name>John</name></user>` |
| **`UUID`** | Universally Unique Identifier. | `a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11` |
| **`ENUM`** | A list of predefined string values. | `ENUM('Small', 'Medium', 'Large')` |

#### Note:
- **Precision matters**: Choose the smallest data type that fits your needs for better performance
- **VARCHAR vs CHAR**: Use VARCHAR for variable-length data, CHAR for fixed-length data
- **Database variations**: Specific implementations may vary between SQL systems (MySQL, PostgreSQL, SQL Server, etc.)

### Domain:
In the context of databases and data modeling, a *domain* refers to the set of all possible valid values that a column (attribute) can contain. It defines the fundamental type of data and the constraints that apply to it.  

Think of it as a formal definition of "what kind of information can go here" and "what rules it must follow."
