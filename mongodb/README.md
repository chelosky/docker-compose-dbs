# MongoDB

MongoDB is a free and open-source cross-platform document-oriented database program. Classified as a NoSQL database program, MongoDB uses JSON-like documents with schemata. MongoDB is developed by MongoDB Inc., and is published under a combination of the Server Side Public License and the Apache License.

First developed by the software company 10gen (now MongoDB Inc.) in October 2007 as a component of a planned platform as a service product, the company shifted to an open source development model in 2009, with 10gen offering commercial support and other services. Since then, MongoDB has been adopted as backend software by a number of major websites and services, including MetLife, Barclays, ADP, UPS, Viacom, and the New York Times, among others. MongoDB is the most popular NoSQL database system.

## HOW TO USE

### Execute the mongo instance

Build and Run the project with one of the follows commands (with docker-compose commands):

```bash
docker-compose -f docker-compose.yml up
# if you need the project execute in the background, use the -d, --detach option
docker-compose -f docker-compose.yml up -d
```
## Default Environment Variables

- Username: `admin`
- Password: `passpass`
- Database: `adolin`
- Port: `27017`
- Connection String: `mongodb://admin:passpass@localhost:27017`

## Environment Variables 

The MongoDB image uses several environment variables which are easy to miss.

- MONGO_INITDB_ROOT_USERNAME and MONGO_INITDB_ROOT_PASSWORD 
    - These variables, used in conjunction, create a new user and set that user's password. This user is created in the admin authentication database and given the role of root, which is a "superuser" role.
- MONGO_INITDB_DATABASE
    - This variable allows you to specify the name of a database to be used for creation scripts in /docker-entrypoint-initdb.d/*.js (see Initializing a fresh instance below). MongoDB is fundamentally designed for "create on first use", so if you do not insert data with your JavaScript files, then no database is created.

`Note`: The MongoDB image uses several others environment variables, you can find them in the follow link: https://hub.docker.com/_/mongo

## References

-  [Official MongoDB Image](https://hub.docker.com/_/mongo)