# MySQL x Redis
a simple docker compose to up and running MySQL and Redis.

## How to import .sql file to MySQL

1. retrieve MySQL `<CONTAINER_ID>`

    ```bash
    docker ps
    ```

2. copy .sql file

    ```bash
    docker cp <path-to>/<file_name>.sql <CONTAINER_ID>:/<file_name>.sql
    ```

3. enter to inside running MySQL container

    ```bash
    docker exec -it <CONTAINER_NAMES> ./bin/bash
    ```

4. begin to import .sql file

    ```bash
    mysql -u<user_name> -p
    ```

    ```sql
    SHOW DATABASES;
    CREATE DATABASE <name_db>;
    USE <name_db>;
    source ./<file_name>.sql;
    ```

5. wait then check your data

    ```sql
    SHOW TABLES;
    ```
