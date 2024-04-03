# Docker Compose for MySQL and phpMyAdmin

This repository contains a Docker Compose file that sets up a MySQL server and a phpMyAdmin interface for database management.

## Services

### MySQL

The MySQL server is based on the `mysql:8.0.36` image. The server is configured with a custom command to set the authentication plugin, character set, collation, and other parameters. The MySQL data is stored in a Docker volume named `mysql`.

### phpMyAdmin

The phpMyAdmin interface is based on the `phpmyadmin/phpmyadmin` image. It depends on the MySQL service and will only start once the MySQL service is healthy.

## Environment Variables

You need to set the following environment variables in your environment or in an `.env` file:

- `MYSQL_USER`: The MySQL username.
- `MYSQL_PASSWORD`: The password for the MySQL user.
- `MYSQL_ROOT_PASSWORD`: The password for the MySQL root user.
- `MYSQL_PORT`: The host port that maps to the MySQL server port 3306.
- `PHPMYADMIN_PORT`: The host port that maps to the phpMyAdmin port 80.

## Usage

To start the services, run the following command in the same directory as the `docker-compose.yml` file:

```bash
docker-compose up -d
```

To stop the services, run the following command:
```bash
docker-compose down
```
Please replace the environment variable values with your actual values. Remember not to commit sensitive data like passwords to your version control system.