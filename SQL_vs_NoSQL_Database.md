
Explore key differences between SQL and NoSQL databases and learn which type of database is best for various use cases.


SQL is a decades-old method for accessing relational databases, and most who work with databases are familiar with it. As unstructured data, amounts of storage and processing power and types of analytics have changed over the years, however, we’ve seen different database technologies become available that are a better fit for newer types of use cases. These databases are commonly called NoSQL.

SQL and NoSQL differ in whether they are relational (SQL) or non-relational (NoSQL), whether their schemas are predefined or dynamic, how they scale, the type of data they include and whether they are more fit for multi-row transactions or unstructured data.

What is a SQL database?


SQL, which stands for “Structured Query Language,” is the programming language that’s been widely used in managing data in relational database management systems (RDBMS) since the 1970s. In the early years, when storage was expensive, SQL databases focused on reducing data duplication.

Fast-forward to today, and SQL is still widely used for querying relational databases, where data is stored in rows and tables that are linked in various ways. One table record may link to one other or to many others, or many table records may be related to many records in another table. These relational databases, which offer fast data storage and recovery, can handle great amounts of data and complex SQL queries.

What is a NoSQL database?


NoSQL is a non-relational database, meaning it allows different structures than a SQL database (not rows and columns) and more flexibility to use a format that best fits the data. The term “NoSQL” was not coined until the early 2000s. It doesn’t mean the systems don’t use SQL, as NoSQL databases do sometimes support some SQL commands. More accurately, “NoSQL” is sometimes defined as “not only SQL.”

To lay the groundwork, see the following video from Jamil Spain:


How SQL works


SQL databases are valuable in handling structured data, or data that has relationships between its variables and entities.

Scalability

In general, SQL databases can scale vertically, meaning you can increase the load on a server by migrating to a larger server that adds more CPU, RAM or SSD capability. While vertical scalability is used most frequently, SQL databases can also scale horizontally through sharding or partitioning logic, although that’s not well-supported.

Structure

SQL database schema organizes data in relational, tabular ways, using tables with columns or attributes and rows of records. Because SQL works with such a strictly predefined schema, it requires organizing and structuring data before starting with the SQL database.

Properties

RDBMS, which use SQL, must exhibit four properties, known by the acronym ACID. These ensure that transactions are processed successfully and that the SQL database has a high level of reliability:

Atomicity: All transactions must succeed or fail completely and cannot be left partially complete, even in the case of system failure.

Consistency: The database must follow rules that validate and prevent corruption at every step.

Isolation: Concurrent transactions cannot affect each other.

Durability: Transactions are final, and even system failure cannot “roll back” a complete transaction.

Support

Because SQL databases have a long history now, they have huge communities, and many examples of their stable codebases online. There are many experts available to support SQL and programming relational data.

Examples of SQL databases

Db2
MySQL
PostgreSQL
YugabyteDB
CockroachDB
Oracle Database
Microsoft SQL Server
Azure SQL Database
How NoSQL works
Unlike SQL, NoSQL systems allow you to work with different data structures within a database. Because they allow a dynamic schema for unstructured data, there’s less need to pre-plan and pre-organize data, and it’s easier to make modifications. NoSQL databases allow you to add new attributes and fields, as well as use varied syntax across databases.

Scalability

NoSQL databases scale better horizontally, which means one can add additional servers or nodes as needed to increase load.

Structure

NoSQL databases are not relational, so they don’t solely store data in rows and tables. Instead, they generally fall into one of four types of structures:

Column-oriented, where data is stored in cells grouped in a virtually unlimited number of columns rather than rows.
Key-value stores, which use an associative array (also known as a dictionary or map) as their data model. This model represents data as a collection of key-value pairs.
Document stores, which use documents to hold and encode data in standard formats, including XML, YAML, JSON (JavaScript Object Notation) and BSON. A benefit is that documents within a single database can have different data types.
Graph databases, which represent data on a graph that shows how different sets of data relate to each other. Neo4j, RedisGraph (a graph module built into Redis) and OrientDB are examples of graph databases.
Properties
While SQL calls for ACID properties, NoSQL follows the CAP theory (although some NoSQL databases — such as IBM’s DB2, MongoDB, AWS’s DynamoDB and Apache’s CouchDB — can also integrate and follow ACID rules).

The CAP theorem says that distributed data systems allow a trade-off that can guarantee only two of the following three properties (which form the acronym CAP) at any one time:

Consistency: Every request receives either the most recent result or an error. MongoDB is an example of a strongly consistent system, whereas others such as Cassandra offer eventual consistency.
Availability: Every request has a non-error result.
Partition tolerance: Any delays or losses between nodes do not interrupt the system operation.
Support
While NoSQL has quickly been adopted, it has smaller user communities and, therefore, less support. NoSQL users do benefit from open-source systems, as opposed to the many SQL languages that are proprietary.

Examples of NoSQL databases

Redis
FaunaDB
CouchDB
MongoDB
Cassandra
Elasticsearch
BigTable
Neo4j
HBase
When to use SQL vs NoSQL

When to use SQL

SQL is a good choice when working with related data. Relational databases are efficient, flexible and easily accessed by any application. A benefit of a relational database is that when one user updates a specific record, every instance of the database automatically refreshes, and that information is provided in real-time.

SQL and a relational database make it easy to handle a great deal of information, scale as necessary and allow flexible access to data — only needing to update data once instead of changing multiple files, for instance. It’s also best for assessing data integrity. Since each piece of information is stored in a single place, there’s no problem with former versions confusing the picture.

Most of the big tech companies use SQL, including Uber, Netflix and Airbnb. Even major companies like Google, Facebook and Amazon, which build their own database systems, use SQL to query and analyze data.

When to use NoSQL

While SQL is valued for ensuring data validity, NoSQL is good when it’s more important that the availability of big data is fast. It’s also a good choice when a company will need to scale because of changing requirements. NoSQL is easy-to-use, flexible and offers high performance.

NoSQL is also a good choice when there are large amounts of (or ever-changing) data sets or when working with flexible data models or needs that don't fit into a relational model. When working with large amounts of unstructured data, document databases (e.g., CouchDB, MongoDB, and Amazon DocumentDB) are a good fit. For quick access to a key-value store without strong integrity guarantees, Redis may be the best choice. When a complex or flexible search across a lot of data is needed, Elastic Search is a good choice.

Scalability is a significant benefit of NoSQL databases. Unlike with SQL, their built-in sharding and high availability requirements allow horizontal scaling. Furthermore, NoSQL databases like Cassandra, developed by Facebook, handle massive amounts of data spread across many servers, having no single points of failure and providing maximum availability.

Other big companies that use NoSQL systems because they are dependent on large volumes of data not suited to a relational database include Amazon, Google and Netflix. In general, the more extensive the dataset, the more likely that NoSQL is a better choice.
