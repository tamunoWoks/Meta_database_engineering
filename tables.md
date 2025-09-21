## Tables
In a relational database, a *table* is a collection of related data organized into a structured format of rows and columns. It's the primary and simplest way to store data.  

A single database can contain multiple tables, each storing data for a different entity (e.g., a Customers table, an Orders table, a Products table).

### Why are Tables Important?
Tables are the building blocks of a relational database because they:
1. **Provide Structure:** The column definitions enforce a consistent structure for all data entered. Every record must fit the defined format.
2. **Organize Data:** They allow you to group related information together logically (e.g., all customer data in one table, all order data in another).
3. **Enable Relationships:** This is the "relational" part. Tables can be linked together using Primary Keys and Foreign Keys. For example, an Orders table can have a CustomerID column that links back to the Customers table, connecting an order to the customer who placed it.
4. **Facilitate Efficient Querying:** The structured format makes it easy to search, sort, filter, and manipulate data using SQL.
