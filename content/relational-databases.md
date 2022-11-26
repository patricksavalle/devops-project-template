**< [devops-project-template](../README.md)**

# Relational databases - best practices

> Content
> - [For CMS en blogging (publication) systems](#for-cms-en-blogging-publication-systems)

## Tips and hints

- [ ] Program referential integrity into the data model using foreign keys, not the server application  


- [ ] Program data model logic into the data model using stored procedures, not the server application


## For CMS en blogging (publication) systems

For systems that are read intensive and don't need absolute data consistency on most queries, it is good practice to:

- Set the database-default to read-only mode. This will catch programming errors and some engines will have better read performance
    ```
    -- MySQL / MariaDB schema creation example
    -- in a read intensive system, default to read only for security and speed
    SET GLOBAL TRANSACTION READ ONLY;
    ```

- Set the database-default to the least strict transaction isolation level. This will prevent locking and dramatically increase read performance
    ```
    -- MySQL / MariaDB schema creation example
    -- if data integrity is not critical for most queries, choose maximum performance
    SET GLOBAL TRANSACTION ISOLATION LEVEL READ UNCOMMITTED;
    ```

- Override only for queries that do need write-access and / or higher transaction isolation levels. 
  In a read intensive system these extra query-statements around write-statements won't be noticeable 
    ```
    -- MySQL / MariaDB example
    ...
    SET SESSION TRANSACTION READ WRITE;
    UPDATE table_x SET field_y=10;
    SET SESSION TRANSACTION READ ONLY;
    ...
    ```
     


