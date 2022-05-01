# MySQL

MySQL is the world's most popular open source database. With its proven performance, reliability and ease-of-use, MySQL has become the leading database choice for web-based applications, covering the entire range from personal projects and websites, via e-commerce and information services, all the way to high profile web properties including Facebook, Twitter, YouTube, Yahoo! and many more.

## HOW TO USE

### Execute the MySQL instance

Build and Run the project with one of the follows commands (with docker-compose commands):

```bash
docker-compose -f docker-compose.yml up
# if you need the project execute in the background, use the -d, --detach option
docker-compose -f docker-compose.yml up -d
```
## Default Environment Variables

- Root User: `root`
- Root Password: `password`
- Username: `shallan`
- Password: `pattern`
- Database: `roshar`
- Port: `3306`

## Environment Variables 

The MySQL image uses several environment variables which are easy to miss. The only variable required is MYSQL_ROOT_PASSWORD, the rest are optional.

- MYSQL_ROOT_PASSWORD 
    - This variable is mandatory and specifies the password that will be set for the MySQL root superuser account.
- MYSQL_DATABASE
    - This variable is optional and allows you to specify the name of a database to be created on image startup. If a user/password was supplied (see below) then that user will be granted superuser access (corresponding to GRANT ALL) to this database.
- MYSQL_USER and MYSQL_PASSWORD
    - These variables are optional, used in conjunction to create a new user and to set that user's password. This user will be granted superuser permissions (see above) for the database specified by the MYSQL_DATABASE variable. Both variables are required for a user to be created. Do note that there is no need to use this mechanism to create the root superuser, that user gets created by default with the password specified by the MYSQL_ROOT_PASSWORD variable.
- MYSQL_ALLOW_EMPTY_PASSWORD
    - This is an optional variable. Set to a non-empty value, like yes, to allow the container to be started with a blank password for the root user. NOTE: Setting this variable to yes is not recommended unless you really know what you are doing, since this will leave your MySQL instance completely unprotected, allowing anyone to gain complete superuser access.
- MYSQL_RANDOM_ROOT_PASSWORD
    - This is an optional variable. Set to a non-empty value, like yes, to generate a random initial password for the root user (using pwgen). The generated root password will be printed to stdout (GENERATED ROOT PASSWORD: .....).
- MYSQL_ONETIME_PASSWORD
    - Sets root (not the user specified in MYSQL_USER!) user as expired once init is complete, forcing a password change on first login. Any non-empty value will activate this setting. NOTE: This feature is supported on MySQL 5.6+ only. Using this option on MySQL 5.5 will throw an appropriate error during initialization.
- MYSQL_INITDB_SKIP_TZINFO
    - By default, the entrypoint script automatically loads the timezone data needed for the CONVERT_TZ() function. If it is not needed, any non-empty value disables timezone loading.

`Note`: The MySQL image uses several others environment variables, you can find them in the follow link: https://hub.docker.com/_/mysql

## References

-  [Official MySQL Image](https://hub.docker.com/_/mysql)
