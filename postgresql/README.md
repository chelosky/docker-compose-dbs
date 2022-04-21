# PostgreSQL

PostgreSQL, often simply "Postgres", is an object-relational database management system (ORDBMS) with an emphasis on extensibility and standards-compliance. As a database server, its primary function is to store data, securely and supporting best practices, and retrieve it later, as requested by other software applications, be it those on the same computer or those running on another computer across a network (including the Internet). It can handle workloads ranging from small single-machine applications to large Internet-facing applications with many concurrent users. Recent versions also provide replication of the database itself for security and scalability.

## HOW TO USE

### Execite the postgres instance

Build and Run the project with one of the follows commands (with docker-compose commands):

```bash
docker-compose -f docker-compose.yml up
# if you need the project execute in the background, use the -d, --detach option
docker-compose -f docker-compose.yml up -d
```
## Default Environment Variables

- Username: `admin`
- Password: `passpass`
- Database: `sylphrena`
- Port: `5432`

## Environment Variables 

The PostgreSQL image uses several environment variables which are easy to miss. The only variable required is POSTGRES_PASSWORD, the rest are optional.

- POSTGRES_PASSWORD 
    - This environment variable sets the superuser password for PostgreSQL. The default superuser is defined by the POSTGRES_USER environment variable.
- POSTGRES_USER
    - This optional environment variable is used in conjunction with POSTGRES_PASSWORD to set a user and its password. This variable will create the specified user with superuser power and a database with the same name. If it is not specified, then the default user of postgres will be used.
- POSTGRES_DB
    - This optional environment variable can be used to define a different name for the default database that is created when the image is first started. If it is not specified, then the value of POSTGRES_USER will be used.

`Note`: The PostgreSQL image uses several others environment variables, you can find them in the follow link: https://hub.docker.com/_/postgres

## References

-  [Official Postgres Image](https://hub.docker.com/_/postgres)
-  [PostgreSQL Documentation](https://www.postgresql.org/docs/)