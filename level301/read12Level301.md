# this is read12 from 301
# Mongo and Mongoose:
![img](https://miro.medium.com/max/527/1*Ipg_guKJO2MwacQ_3amxGw.jpeg)

# SQL vs NoSQL Database Differences Explained with few Example DB :
Most of you are already familiar with SQL database, and have a good knowledge on either MySQL, Oracle, or other SQL databases. In the last several years, NoSQL database is getting widely adopted to solve various business problems.It is helpful to understand the difference between SQL and NoSQL database, and some of available NoSQL database that you can play around with.

# SQL vs NoSQL: High-Level Differences :
   * SQL databases are primarily called as Relational Databases (RDBMS); whereas NoSQL database are primarily called as non-relational or distributed database.
   * SQL databases are table based databases whereas NoSQL databases are document based, key-value pairs, graph databases or wide-column stores. This means that SQL databases represent data in form of tables which consists of n number of rows of data whereas NoSQL databases are the collection of key-value pair, documents, graph databases or wide-column stores which do not have standard schema definitions which it needs to adhered to.
   * SQL databases have predefined schema whereas NoSQL databases have dynamic schema for unstructured data.
   * QL databases are vertically scalable whereas the NoSQL databases are horizontally scalable. SQL databases are scaled by increasing the horse-power of the hardware. NoSQL databases are scaled by increasing the databases servers in the pool of resources to reduce the load.
   * SQL databases uses SQL ( structured query language ) for defining and manipulating the data, which is very powerful. In NoSQL database, queries are focused on collection of documents. Sometimes it is also called as UnQL (Unstructured Query Language). The syntax of using UnQL varies from database to database.
   * SQL database examples: MySql, Oracle, Sqlite, Postgres and MS-SQL. NoSQL database examples: MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb.
   
  1. For complex queries :
          SQL databases are good fit for the complex query intensive environment whereas NoSQL databases are not good fit for complex queries. On a high-level, NoSQL don’t have standard interfaces to perform complex queries, and the queries themselves in NoSQL are not as powerful as SQL query language.
  2.  For the type of data to be stored :
          SQL databases are not best fit for hierarchical data storage. But, NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data. NoSQL database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose.
  3. For scalability: 
       In most typical situations, SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server. On the other hand, NoSQL databases are horizontally scalable. You can just add few more servers easily in your NoSQL database infrastructure to handle the large traffic.
  4. For high transactional based application: 
       SQL databases are best fit for heavy duty transactional type applications, as it is more stable and promises the atomicity as well as integrity of the data. While you can use NoSQL for transactions purpose, it is still not comparable and sable enough in high load and for complex transactional applications.
  5. For properties:    
       SQL databases emphasizes on ACID properties ( Atomicity, Consistency, Isolation and Durability) whereas the NoSQL database follows the Brewers CAP theorem Consistency, Availability and Partition tolerance. 
  6. For DB types: 
        On a high-level, we can classify SQL databases as either open-source or close-sourced from commercial vendors. NoSQL databases can be classified on the basis of way of storing data as graph databases, key-value store databases, document store databases, column store database and XML databases.


# SQL Database Examples :
  1. MySQL Community Edition:is very popular open-source database. It is generally been stacked with apache and PHP, although it can be also stacked with nginx and server side javascripting using Node js. The following are some of MySQL benefits and strengths:
     * Replication.
     * Sharding.
     * Memcached as a NoSQL API to MySQL
     * Maturity
     * Wide range of Platforms and Languages
     * Cost effectiveness

  2. MS-SQL Server Express Edition :It is a powerful and user friendly database which has good stability, reliability and scalability with support from Microsoft. The following are some of MS-SQL benefits and strengths:
     * Integrated Development Environment
     * Disaster Recovery
     * Cloud back-up: Microsoft also provides cloud storage when you perform a cloud-backup of your database.

  3. Oracle Express Edition :It is a limited edition of Oracle Enterprise Edition server with certain limitations. This database is free for development and deployment. The following are some of Oracle benefits and strengths: 
     * Easy to Upgrade
     * Wide platform support
     * Scalability

# NoSQL Database Examples :
 1. MongoDB :Mongodb is one of the most popular document based NoSQL database as it stores data in JSON like documents. It is non-relational database with dynamic schema. It has been developed by the founders of DoubleClick, written in C++ and is currently being used by some big companies like The New York Times, Craigslist, MTV Networks. The following are some of MongoDB benefits and strengths:
   * Speed
   * Scalability
   * Manageable
   * Dynamic Schema

2. CouchDB:is also a document based NoSQL database. It stores data in form of JSON documents. The following are some of CouchDB benefits and strengths:
   * Schema-less
   * HTTP query
   * Conflict Resolution
   * Easy Replication

3. Redis :is another Open Source NoSQL database which is mainly used because of its lightening speed. It is written in ANSI C language. The following are some of Redis benefits and strengths:
   * Data structures
   * Redis as Cache    
   * Very fast

# Mongoose():
options «Object» see Mongoose#set() docs
Mongoose constructor.
The exports object of the mongoose module is an instance of this class. Most apps will only use this one instance.   
     
# Mongoose.prototype.CastError() Parameters:
1. type «String» The name of the type
2. value «Any» The value that failed to cast
3. path «String» The path a.b.c in the doc where this cast error occurred
4. [reason] «Error» The original error that was thrown

# Mongoose.prototype.connect() :
1. uri(s) «String»
2. [options] «Object» passed down to the MongoDB driver's connect() function, except for 4 mongoose-specific options :
    * [options.bufferCommands=true] «Boolean» Mongoose specific option. Set to false to disable buffering on all models associated with this connection.
    * options.bufferTimeoutMS=true] «Number» Mongoose specific option. If bufferCommands is true, Mongoose will throw an error after bufferTimeoutMS if the operation is still buffered.
    * [options.dbName] «String» The name of the database we want to use. If not provided, use database name from connection string.
    * [options.user] «String» username for authentication, equivalent to options.auth.user. Maintained for backwards compatibility.
    * [options.pass] «String» password for authentication, equivalent to options.auth.password. Maintained for backwards compatibility.
    *[options.poolSize=5] «Number» The maximum number of sockets the MongoDB driver will keep open for this connection. By default, poolSize is 5. Keep in mind that, as of MongoDB 3.4, MongoDB only allows one operation per socket at a time, so you may want to increase this if you find you have a few slow queries that are blocking faster queries from proceeding. See Slow Trains in MongoDB and Node.js.
    * [options.useUnifiedTopology=false] «Boolean» False by default. Set to true to opt in to the MongoDB driver's replica set and sharded cluster monitoring engine.
    * [options.family=0] «Number» Passed transparently to Node.js' dns.lookup() function. May be either 0, 4, or 6. 4 means use IPv4 only, 6 means use IPv6 only, 0 means try both.
    * [options.autoCreate=false] «Boolean» Set to true to make Mongoose automatically call createCollection() on every model created on this connection.

 # Mongoose.prototype.deleteModel():
 name «String|RegExp» if string, the name of the model to remove. If regexp, removes all models whose name matches the regexp..«Mongoose» this
Removes the model named name from the default connection, if it exists. You can use this function to clean up any models you created in your tests to prevent OverwriteModelErrors.Equivalent to mongoose.connection.deleteModel(name).     
# Mongoose.prototype.disconnect() :
[callback] «Function» called after all connection close, or when first error occurred.
Returns:
«Promise» resolves when all connections are closed, or rejects with the first error that occurred.
Runs .close() on all connections in parallel.

# Mongoose.prototype.driver :
Object with get() and set() containing the underlying driver this Mongoose instance uses to communicate with the database. A driver is a Mongoose-specific interface that defines functions like find().

# Mongoose.prototype.model() :
  * name «String|Function» model name or class extending Model
  * [schema] «Schema» the schema to use.
  * [collection] «String» name (optional, inferred from model name)
  * [skipInit] «Boolean|Object» whether to skip initialization (defaults to false). If an object, treated as options.

 «Model» The model associated with name. Mongoose will create the model if it doesn't already exist.
Defines a model or retrieves it.Models defined on the mongoose instance are available to all connection created by the same mongoose instance.
If you call mongoose.model() with twice the same name but a different schema, you will get an OverwriteModelError. If you call mongoose.model() with the same name and same schema, you'll get the same schema back. 

# Aggregate.prototype.replaceRoot() :
the «String|Object» field or document which will become the new root document
Returns:
«Aggregate»:Appends a new $replaceRoot operator to this aggregate pipeline.
Note that the $replaceRoot operator requires field strings to start with '$'. If you are passing in a string Mongoose will prepend '$' if the specified field doesn't start '$'. If you are passing in an object the strings in your expression will not be altered.

# Aggregate.prototype.sample() :
Parameters:size «Number» number of random documents to pick
Returns:«Aggregate»
Appends new custom $sample operator to this aggregate pipeline.



                            




