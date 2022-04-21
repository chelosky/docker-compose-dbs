# Microsoft SQL Server

SQL Server is a relational database management system, or RDBMS, developed and marketed by Microsoft. Similar to other RDBMS software, SQL Server is built on top of SQL, a standard programming language for interacting with relational databases. SQL Server is tied to Transact-SQL, or T-SQL, the Microsoft’s implementation of SQL that adds a set of proprietary programming constructs.

## HOW TO USE

### Execite the SQL Server instance

Build and Run the project with one of the follows commands (with docker-compose commands):

```bash
docker-compose -f docker-compose.yml up
# if you need the project execute in the background, use the -d, --detach option
docker-compose -f docker-compose.yml up -d
```
## Default Environment Variables

- Username: `sa`
- Password: `FirstIdeal1`
- Database: `master`
- Port: `1433`
- SQL Server Edition: `Developer`

## Environment Variables 

- ACCEPT_EULA
    - Confirms your acceptance of the End-User Licensing Agreement. (always Y)
- SA_PASSWORD
    - Is the database system administrator (userid = 'sa') password used to connect to SQL Server once the container is running. 
    - Important note: This password needs to include at least 8 characters of at least three of these four categories: uppercase letters, lowercase letters, numbers and non-alphanumeric symbols.
- MSSQL_PID 
    - Is the Product ID (PID) or Edition that the container will run with. Acceptable values: Developer, Express, Standard, Enterprise or EnterpriseCore

## References

-  [Official SQL Server Image](https://hub.docker.com/_/microsoft-mssql-server)
-  [Microsoft SQL Server Documentation](https://docs.microsoft.com/en-us/sql/linux/quickstart-install-connect-docker?view=sql-server-ver15&pivots=cs1-bash)