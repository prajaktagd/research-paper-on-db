# Criteria for choosing the right database

Consider the following criteria for choosing the right database technology for your service:

### Query Patterns

The way of fetching the data is one of the main ways to find the best database for a particular use case. Some of the databases that can be used for fetching the data are listed below :

- **Key-value store :** Key-value store is used to fetch the data using key.
- **Wide-column databases :** Sometimes one or more fields are used to fetch the data, then wide-column databases can be used.
- **Document or relational database :** There might a requirement to query using many different fields, then document or relational database can be used.
- **Search engines :** In case of a fuzzy search query capabilities or free text search, search engines can be used.

---

### Consistency

Is strong consistency required (read after write, especially when you switch writes to a different data-center) or eventual consistency is OK?

In case you need to read your data right after your write it (i.e. strong consistency) than a Relational database (e.g. MySQL, PostgreSQL) is usually more suited than a Document Database (e.g.MongoDB, CouchDB), especially in case of multi-data-center scenario.

---

### Storage Capacity

How much storage capacity is needed?

Most database systems are limited by the amount of space on disk (e.g. MySQL) or struggle with performance as amount of Nodes and Shards grows into the hundreds (e.g. Elasticsearch).

When infinite storage is needed this is where cloud solutions shine. Object Storage Services like S3 and GCS will allow you to store as much data as you like with the handy option of multiple tiers, so you pay less for data that is rarely retrieved.

---

### Performance

What is the needed throughput and latency?

All databases performance degrades as the amount of read/write throughput traffic increases. This is the time when optimizations such as re-indexing and re-sharding of your data come in handy.

In case you have very high traffic and require very low latency, Cloud providers solutions like Amazon’s DynamoDB and Google’s Bigtable could be just what you need. As long as your service is deployed on the same data center as the database, you can enjoy latencies that are under 10ms. The downside is of-course the $ cost.

---

### Maturity and Stability

If you choose self-hosted deployment, How much experience does your DBA team have with this technology, how mature is it?

Choosing the most trendy, powerful, and fully featured database to self-host maybe tempting, but as long as your organization doesn’t have experience with this database, you may end up regretting it.

Setup, configuration and fine tuning of databases is a lengthy and risky ordeal. Sometimes choosing the “old” organization self-hosted work-horse will pay bigger dividends in the long term when it comes to production stability.

---

### Cost

If you choose a managed cloud solution, What are the costs? What are its limitations?

The payment model for managed cloud solutions is usually proportional to the read/write traffic. Make sure to read the finer print for each managed solution and make sure that it is cost-effective for your specific read/write usage patterns.

---

### Concurrency

Data concurrency is the ability to allow multiple users to affect multiple transaction within a database. Simply, data concurrency allows multiple users to access data all at the same time.

The ability to offer concurrency is unique to databases. Almost all databases deal with concurrency the same way, with the general principle being that the unsaved changed data is held in a type of temporary log or file. Once the data is saved, it is then written into the database’s physical storage in place of the original data.

There are two type of database concurrency used in businesses daily:

- **Simultaneous Access To Data** – This kind of concurrency is important because it’s all about multiple users accessing data at the same time without causing inconsistencies.

- **Coexistent Query Workload** – This type of concurrency is a fundamental measure of system performance. Businesses use the term “concurrency” to measure how many units of work are co-executing actively and simultaneously progressing at the same time.

For example, when one user is changing data but has not yet saved (committed) that data, then the database should not allow other users who query the same data to view the changed, unsaved data. Instead the user should only view the original data.

---

### Load

Estimated the load is often treated as a server sizing exercise before installing production database. Unfortunately, many databases can't handle thousands of queries because of scaling issues.

Database load measures the level of activity in the database. For that measurement there will be question like - How is the database performing? And this can be measured by different units.

There are few units that helps measuring the load a database can take:

- **Queries Per Second (QPS)** - This unit refers to how many queries the database can execute in a given period of time? The kind of queries is not same all the time, it can be simple from some user or complex from another user. In the real world, database load fluctuates. The focus is to compare performances between different set of configuration over a different period of time with different query mix.

- **Transactions Per Second (TPS)** - This unit refers to how many transactions an user can execute in a given time period? But this units also contains same sets of issues as QPS. There will be different sets of transactions on different period of time, so calculating transactions may work a given period of time but actually hards to compare the result over time.

- **Latency** - This unit refers to a different perspective of the database. There can be questions like - would user like to be ok to improve QPS by 30%, if user would have to wait twice as long for a given query to complete? User needs to keep in mind that for most of the cases, databases are using one CPU core for one query. There are some situations where multiple queries can process parallely in one core but that's actually a rare case. The fastest we can run the queries the more queries we can run. So, In one hand we are minimizing the query execution time and on the other hand we are maximizing the total throughput. That way we can handle more number of user or workload in less amount time.

---

### Data Localization

Data Localization is the act of storing the on any physical device that is present within the borders of a specific country where the data was generated. Free flow of digital data which could impact government operations in a region is restricted by the government. This attempt of providing security for data across borders encourages **Data Localization**. One of the fundamental precepts of Data Localization is state data must be localized accessible within a geographical limits of a country because it is a important resource in terms of today's digital world.
Data Localization is the act of storing the data on any physical device that is present within the borders of a specific country where the data was generated. Free flow of digital data which could impact government operations in a region is restricted by the government. This attempt of providing security for data across borders encourages **data localization**. One of the fundamental precepts of data localization is state data must be localized accessible within a geographical limits of a country because it is a important resource in terms of today's digital world.

While some arguments support Data Localization, some feel that Data Localization could serious harmful consequences to citizens and economics.

There are effects of Data Localization, depending on the context in which it is used. Some of those effects, generally advantages and challenges to be consider:

- **Data Security** - Data Localization can enhance the security of data by keeping it within the borders of a particular country. This is particularly important to handle sensitive information.

- **Economic considerations** - Data Localization can provide economic benefits, which helps on economic growth of a particular country.

- **Improved Performance** - Data Localization can improve the performance of online applications and websites, by keeping data closer to users.

- **Cost** - One of the main challenge in Data Localization is Cosy, which includes of building or renting data centers, as well as cost of complying with multiple laws and regulations.

- **Limited Access** - Data Localization can limit access to data as it may not be accessible to users outside the country or region in which it is stored.

- **Complexity** - It can also be complex to implement as it involves transferring data between different locations.

---

### API Compatibility

API compatibility of database refers to the ability of different versions of a database to interact with each other using a consistent set of **Application Programming Interfaces**(APIs). API Compatibility ensures that applications built in one version can seamlessly migrate with another version without significant modifications. The level of the API Compatibility can vary depending on the specific database management system(DBMS) being used. Some databases like MySQL and PostgreSQL, have well-defined and widely adopted APIs which are supported by various programming languages and frameworks.

On the other hand, proprietary databases with unique features may have their own APIs that are specific to that particular system. In such cases compatibility may be limited to the applications developed for that database.

To ensure API Compatibility, it is important to consider factor like version of the database software, language and framework being used. It is beneficial to consider the documentation and resources provided by the database to understand the APIs and its compatibility.

---

### Integration with outside data

Integration with outside data refers to the process of bringing data from multiple source together across an organization to provide a complete, accurate and up-to-date applications and business processes. It includes data replication, ingestion and transformation to combine different type of data to be stored in a target place such as a data warehouse or data lake-house.

The most important thing to consider is what system you need to integrate together? Make sure that the database management system can be integrated with other tools and services also within the project. There are different technologies in the market that have different connectors to integrate with other technologies.

There are generally 5 approaches to integrate data with other services: ETL, ELT, Data Streaming, Application Integration and Data Virtualization. Following are the primary approaches to integrate data with external services:

- **ETL** - It is a traditional type of data-pipeline which converts raw data to match the target system via extract, transform and load. Data is transform in a staging area before it is loaded into the target place. This allows for fast and accurate data analysis in the target system and is most appropriate for small datasets which requires complex transformations.

- **ELT** - This is also a data pipeline that supports immediately load and transformation of data within target system. This approach is more appropriate when datasets are large and timeliness is important, since loading is quite quicker.

- **Data Streaming** - Instead of loading data into a new target system, Data Streaming provides continuous flowing of data from source to target.

- **Application Integration** - Application Integration allows separate applications to work together by moving or syncing data between them. The most typical use case to support operational needs such as ensuring data to the systems. The Application Integration must provide consistency between the data sets. Mostly the applications have their APIs for transactions of data, which helps automation tools to maintain integration efficiently.

- **Data Virtualization** - Like Data Streaming, Data Virtualizations also delivers data in time, but only when it is requested by a user or application. This can unified view of data and makes data available on demand by combining data from different systems. Both Virtualizations and Streaming support transactional systems built for high performance queries.

For Example, if there is a big analytics job running in **Apache Spark** then probably user want to limit themselves to external systems that can easily connect to Apache Spark.

---

### Read Only Databases

Databases whose architecture or data is not required to be updated should be considered to be set as Read Only Database. Once a database is changed to Read Only Database, nothing will change in the database. So based on that, certain changes should be made to optimize the performance of a Read Only Database. The facts to be consider is:

* Statistics will not be automatically updated (nor required) and user would not be able to update statistics of Read Only database
* **Read Only** Database will not shrink automatically or manually
* User will not be able to create indexes
* User will not be able to defragment indexes of a Read Only Database
* Read Only Databases will not allow user to add any extended properties on any of its objects
* Permissions may not be edited and users may not be added or removed from a Read ONly Database

So, it is required to complete such tasks before someone set the database to Read Only mode. And there will be some factsto consider while working with a backup of a Read Only Database, those are as follows:

* User can create any type of backup (full, differential, log) of a Database in Read Only state. However considering the Read Only state user may want to have a different backup plan than that of a Read Write database. Consider using simple recovery mode along with only full backups
* A full backup of a Read Only Database would be recovered as a Read Only Database. Recovered database may be changed to Read Write mode later
* A full backup of a Read Write Database over a Read Only Database would make the target database Read Write , so user may need to change the state of the database again

Along with these there are some performance benefits of Read Only state, those are:

* As there are no data modifications in Read Only state, Database servers would not have to bother with locks
* User can create additional indexes to optimize data retrieval without worrying about degradation of data modifications and index maintenance
* User can copy data and log files of a Read Only database while the database is online

Even after the precautions, preconsiderations and preparations, if there is a need to change the mode from Read Only to Read Write, it can be performed using different database tools.
