# database replication

Database replication involves copying, transferring, or integrating data from one database in a server or computer to another, eventually creating a distributed database. Replication allows users to access the same information, which improves consistency, reliability, and performance. Data replication can either happen once or it can be a continuous process. The result is one or more distributed databases, where users have access to the same information across all database nodes. The original database is called the "Publisher." The replicated database is called the "Subscriber."

## Data Replication Types

**1. Transactional Replication**

The distributed database management system(DDBMS) replicates changes (or "transactions") made to the original database on the receiving database in a sequence in near-real-time. Users on the replicated database(s) experience changes made to the original database almost instantly. 

**2. Snapshot Replication**

The DDBMS captures a "snapshot" of data from the original database and overwrites it on the receiving database via the same server. 

**3. Merge Replication**

The DDBMS merges data from two or more databases and combines it into a new receiving database. 
