# Criteria for choosing the right database

Consider the following criteria for choosing the right database technology for your service:

### Query Patterns
How complex are your query patterns? Do you just need retrieval by key, or also by various other parameters? Do you also need fuzzy search on the data?

How you are going to fetch your data is one of the main ways to find the best database for your use case. If you are going to fetch data by key, then all you need is a key-value store (e.g. DynamoDB, Redis, S3, GCS).

In case you mostly fetch via key, but sometimes you also need to fetch by one or two other fields, then Wide-Column DBs (e.g.DynamoDB, Cassandra) may be right for you.

On the other hand if you will require to query by many different fields you can choose either Relational DB (e.g.MySQL, PostgreSQL) or Document DB (e.g.MongoDB, CouchDB, MySQL, PostgreSQ). Note that Document DBs don’t support well queries that require joining data from multiple documents.

Finally, in case you are looking for fuzzy search query capabilities (free text search), then search engines like Elasticsearch and Solr are the best fit.

### Consistency
Is strong consistency required (read after write, especially when you switch writes to a different data-center) or eventual consistency is OK?

In case you need to read your data right after your write it (i.e. strong consistency) than a Relational database (e.g. MySQL, PostgreSQL) is usually more suited than a Document Database (e.g.MongoDB, CouchDB), especially in case of multi-data-center scenario.

### Storage Capacity
How much storage capacity is needed?

Most database systems are limited by the amount of space on disk (e.g. MySQL) or struggle with performance as amount of Nodes and Shards grows into the hundreds (e.g. Elasticsearch).

When infinite storage is needed this is where cloud solutions shine. Object Storage Services like S3 and GCS will allow you to store as much data as you like with the handy option is multiple tiers, so you pay less for data that is rarely retrieved.

### Performance
What is the needed throughput and latency?

All databases performance degrades as the amount of read/write throughput traffic increases. This is the time when optimizations such as re-indexing and re-sharding of your data come in handy.

In case you have very high traffic and require very low latency, Cloud providers solutions like Amazon’s DynamoDB and Google’s Bigtable could be just what you need. As long as your service is deployed on the same data center as the database, you can enjoy latencies that are under 10ms. The downside is of-course the $ cost.

### Maturity and Stability
If you choose self-hosted deployment, How much experience does your DBA team have with this technology, how mature is it?

Choosing the most trendy, powerful, and fully featured database to self-host maybe tempting, but as long as your orgainization doesn’t have experience with this database, you may end up regretting it.

Setup, configuration and fine tuning of databases is a lengthy and risky ordeal. Sometimes choosing the “old” organization self-hosted work-horse will pay bigger dividends in the long term when it comes to production stability.

### Cost
If you choose a managed cloud solution, What are the costs? What are its limitations?

The payment model for managed cloud solutions is usually proportional to the read/write traffic. Make sure to read the finer print for each managed solution and make sure that it is cost-effective for your specific read/write usage patterns.