[<=== Back](../README.md)

# Mongo and Mongoose

## [NoSQL vs SQL](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

| SQL | NoSQL |
| --- | ----- |
| table-based | document-based: key-value pairs, graph databases, or wide-column stores |
| pre-defined schema | dynamic schema |
| scaled by increasing 'horse power' of the hardware | scaled by increasing the db's servers in the pool of resources to reduce the load |
| use structured query language for defining and manipulating data | syntax varies from database to database |
| better fit for complex query-intensive environment | better fit for large data sets |

**What kind of data is a good fit for an SQL database? Give a real world example.****

Complex, query-intensive environments.

Used on social media platforms, like Facebook, use SQL to store users' profile information and posts.

**What kind of data is a good fit a NoSQL database?Give a real world example.**

Large scale data sets.

Content management for companies which utilize multimedia content, storing large sets of diverse data.

**Which type of database is best for hierarchical data storage?**

NoSQL

**Which type of database is best for scalability?**

NoSQL. NoSQL can be scaled both vertially and horizontally.

## [SQL vs NoSQL](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y) (Video)

**What does SQL stand for?**

*Structured Query Language*

**What is a relational database?**

A database where sets of data are related to one another. eg, a separate table for each column of data.

**What type of structure does a relational database work with?**

Tables

**What is a ‘schema’?**

The layout of table data in a SQL database - defines the 'key' for each column of data.

**What is a NoSQL database?**

A database that can store a large quantity of data. There is no set schema, and it is very flexible. 

**How does it work?**

Inside of the database, there are collections of documents. Collections can store multiple documents. 

**What is inside of a Mongo database?**

Collections and documents (with data formatted similar to JSON)

**Which is more flexible - SQL or MongoDB? and why.**

MongoDB is more flexible because there is no set schema, and scaling is easier to do.

**What is the disadvantage of a NoSQL database?**

It is possible to have duplicate data. Needing to update data frequently can reduce performance. 

### Bookmark and Review

[mongoose api](https://mongoosejs.com/docs/api.html#Model)

[React Router](https://v5.reactrouter.com/web/api/BrowserRouter)