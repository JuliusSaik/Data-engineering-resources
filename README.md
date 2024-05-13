# Data-engineering-resources
Simplified key concepts, main functions and overview of the workflow used for data engineering beginners. All of it in a readme file for easy access and memory.

## Main tools
1. Docker for easy image downloads and setups, also easier communication between databases and the scripts, exporting.
2. Databases like PostgreSQL, MySQL, MongoDB.
3. Python
4. Bash terminal for running Docker commands, acessing DBs etc.

## About Docker 
Docker packages different applications with their specific configurations and allows easy, precise downloads for each container. It's easier to install and set up different services like DBs with Docker.

### Key concepts
Docker works by creating a blueprint for your application with the `Dockerfile`, then creates a template as the image and later creates a container that installs all the neccessary libs.
From one image you can spawn multiple different containers with different configurations.

1. Docker compose - Used to define services and start containers from images. Easy way to set up containers, attach volumes, connect to networks and declare neccessary environment variables all at once in a `.yaml` file.
run `docker compose up` to execute.
2. Volumes - attach to databases to persist data even after shutting down the container. A volume is attached to the temporary `var/lib/data` path and is saved in the host file system.
3. Networks - connect different containers to the same network and allow communication between them.


### Main Functions:
Docker flags and commands in bash:
1. `-d` detach so terminal is not taken up, run it in the background
2. `docker exec [container name] [command] [args]` execute specific a command that a container has.
3. `docker ps, images, rm, rmi` - show the images/containers and remove them


### Workflow (for example setting up a PostgresSQL database)
1. Set up a `docker-compose.yaml` file and declare the services, postgres image and other variables. Specify a volume to `pgdata:var/lib/postgresql/data`
2. Run `docker compose up -d`. Docker will pull the postgres image and start a container (specified service from the compose file) that acts as the actual database with your specific configurations.
3. Run `docker -it exec [container_name] psql -U user -d [database name]` (-it means functional interactive terminal) to go into database and then write SQL from there.


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

## Setting up a 

