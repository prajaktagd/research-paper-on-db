# How to choose a database for your application?

## What is a database?

A database is an organized collection of structured information or data that is stored and managed in a computer system. It is designed to efficiently store, retrieve, and manipulate large amounts of data. It allows users and applications to access and work, while ensuring data integrity, consistency, and security. Databases are used in various domains and industries to store different types of data, such as customer information, financial records, inventory data, scientific data, and more.

Databases are managed by database management systems (DBMS), which provide the tools and functionality to create, modify, and retrieve data from the database. Common types of DBMS include relational database management systems (RDBMS) like MySQL, Oracle, and SQL Server, as well as non-relational or NoSQL databases like MongoDB and Cassandra.

## Evolution of database

The database started with a file-based system about 50 years ago. In the due time, it has gone through generations of evolution.

- Databases were first introduced in 1968 as flat-file-based databases.
- Then the Hierarchical Database came into existence and lasted until 1980. IBM’s first database, IMS (Information Management System) was based on this.
- Charles Bachman developed the first Network data model, called Integrated Data Store (IDS). It was introduced in the early 1960s and standardized in 1971.
- In 1970, the Relational Database was introduced.
- Today, it is the era of Relational Database and Database Management.

## Types of databases

The following are the types of databases categorized based on various factors:

### Model

**Relational database**

A relational database stores and provides access to data points that are related to one another. It is based on the relational model and use tables to store and organize data. In a relational database, each row in the table is a record with a unique ID called the key. The columns of the table hold attributes of the data, and each record usually has a value for each attribute, making it easy to establish the relationships among data points. Popular relational database management systems (RDBMS) include MySQL, Oracle, Microsoft SQL Server and PostgreSQL.

**Non-relational database**

The non-relational database or NoSQL (Not Only SQL) databases are non-relational databases that provide flexible data models and scalability. They are suitable for handling large volumes of unstructured or semi-structured data. However, unlike the relational database, there are no tables, rows, primary keys or foreign keys. Instead, the non-relational database uses a storage model optimized for specific requirements of the type of data being stored.

NoSQL databases can be classified into categories such as

- Document databases

  Document databases make it easier for developers to store and query data in a database by using the same document-model format they use in their application code. The flexible, semistructured, and hierarchical nature of documents and document databases allows them to evolve with applications’ needs. The document model works well with use cases such as catalogs, user profiles and content management systems where each document is unique and evolves over time. Document databases enable flexible indexing, powerful ad hoc queries and analytics over collections of documents. Widely used document databases are Amazon DocumentDB and MongoDB.

- Key-value stores

  A key-value database uses a simple key-value method to store data. A key-value database stores data as a collection of key-value pairs in which a key serves as a unique identifier. Both keys and values can be anything, ranging from simple objects to complex compound objects. Key-value databases are highly partitionable and allow horizontal scaling at scales that other types of databases cannot achieve. Redis and AmazonDynamo DB are some of the key-value store databases.

- Column-based databases

  A column-based database helps to store data in columns rather than rows. It is responsible for speeding up the time required to return a particular query. It also is responsible for greatly improving the disk I/O performance. It is helpful in data analytics and data warehousing. Also the major motive of column-based database is to effectively read and write data. Here are some examples for column-based database like Monet DB, Apache Cassandra, SAP Hana, Amazon Redshift.

- Graph databases

  A graph database's purpose is to make it easy to build and run applications that work with highly connected data sets. Typical use cases for a graph database include social networking, recommendation engines, fraud detection and knowledge graphs. Some of the examples of graph databases are Neo4j, DGraph and JanusGraph.

- In-memory databases

  In-memory databases are purpose-built databases that rely primarily on memory for data storage, in contrast to databases that store data on disk or SSDs. In-memory data stores are designed to enable minimal response times by eliminating the need to access disks. Because all data is stored and managed exclusively in main memory, in-memory databases risk losing data upon a process or server failure. In-memory databases can persist data on disks by storing each operation in a log or by taking snapshots.
  In-memory databases are ideal for applications that require microsecond response times or have large spikes in traffic such as gaming leaderboards, session stores, and real-time analytics. Following are some of the in-memory databases, SAP HANA, VoltDB and MemSQL.

**Object-oriented database**

An object-oriented database is a type of database that is based on the principles of object-oriented programming (OOP). In an object-oriented database, data is organized and stored as objects, which are self-contained units that contain both data and the operations or methods that can be performed on that data. This allows for the efficient representation and management of complex data structures and relationships. Popular object-oriented databases include ConceptBase, Db4o, ObjectDB, etc.

### Location

**Centralized**

A centralised database is a database in which the data required to complete all of your day-to-day business activities are located, stored and maintained in a single location. Multiple users are able to access the database and it's easier for them to get a complete view of the data due to its single location. Examples of a centralized database are a desktop or server CPU or mainframe computer that users access through a computer network such as a LAN or WAN.

**Distributed**

Distributed databases store information across different physical sites. The database resides on multiple CPUs on a single site or spread out across various locations. Due to the connections between the distributed databases, the information appears as a single database to end-users. Additionally, if one database fails, users can still access the system through other systems. Common examples of distributed databases include Apache Ignite, Apache Cassandra, Couchbase Server, etc.