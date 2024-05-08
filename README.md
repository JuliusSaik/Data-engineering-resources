# Data-engineering-resources
Resources, main commands, code, concepts etc. used for data engineering. All of it in a readme file for easy access and memory.

## Main tools
1. Docker for easy image downloads and setups, also easier communication between databases and the scripts, exporting.
2. Database like PostgreSQL, mySQL, mongoDB.
3. Python

## About Docker 




## About databases
Databases are SQL or noSQL. SQL DBs are ACID - atomicity, consistency, isolation, durability.
Entire goal of databases is to effectively store information and minimize possible problems, later be able to effectively manipulate information and access it when needed.


### Relational Database management system (RDBMS):
1. MySQL
2. PostgreSQL
3. MSSQL
4. SQLite

Stores informations in tables with keys and values.
Not super scalable but very reliable because of ACID.

### Document store databases:
1. MarkLogic
2. MongoDB
3. ApacheCouchDB
4. 
Stores information in JSON with key value pairs.
Less rigid, scales better, has many functions but not ACID compliant.

### Graph databases:
1. OrientDB
2. Neo4J
3. ArangoDB
   
Connecting nodes(information) with edges(relationships to others).
More for relationships between data instead of particular data.

### Key-Value stores:
1. Redis
2. MongoDB
3. DynamoDB
4. Memcached
Runs entirely in system memory, is super fast. 

