# Data-engineering-resources
Resources, main commands, code, concepts etc. used for data engineering. All of it in a readme file for easy access and memory.

## Main tools
1. Docker for easy image downloads and setups, also easier communication between databases and the scripts, exporting.
2. Database like PostgreSQL, mySQL, mongoDB.
3. Python

## About Docker 

Docker packages different applications with their specific configurations and allows easy, precise downloads for each container. It's easier to install and set up different services like DBs with Docker.

### Basic working
Creates a blueprint for your application with the Dockerfile, then creates a template as the image and later creates a container that installs all neccessary libs.

### Main Commands:
1. -d detach so terminal is not taken up, run it in the background
2. -p 80:80 bind the 80 port to the containers port so you can access it and publish. (standard to use the same port)
3. docker ps, images, rm, rmi - show the images/containers and remove them
4. 

### Creating a Dockefile (what you would have to do locally but in commands)
1. `FROM node:19-alpine` start with the base image (Usually your programming language) 
2. `COPY src /app/` copy the directories and files into container
3. `WORKDIR /app` go into the created directory to work there
4. `RUN npm install` Installing neccessary libs
5. `CMD ["node", "server.js"]` starts the actual application with specific file in working directory


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

