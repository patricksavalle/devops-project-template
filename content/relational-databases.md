# Relational databases - best practices

> Content
> - [For CMS en blogging (publication) systems](#for-cms-en-blogging-publication-systems)

## For CMS en blogging (publication) systems

For systems that are read intensive and don't need referential integrity / data consistency on most queries, it is good practice to:

- Set the database-default to read-only mode. This will catch programming errors and some engines will do faster SELECT's
    ```
    -- MySQL / MariaDB schema creation example
    -- if data integrity is not critical for most queries, choose maximum performance
    SET GLOBAL TRANSACTION ISOLATION LEVEL READ UNCOMMITTED;
    ```

- Set the database-default to the least strict transaction isolation level. This will prevent locking and dramatically increase SELECT-speed
    ```
    -- MySQL / MariaDB schema creation example
    -- in a read intensive system, default to read only for security and speed
    SET GLOBAL TRANSACTION READ ONLY;
  
- Override only for queries that do need write-access and / or higher transaction isolation levels 
    ```
    -- MySQL / MariaDB example
    ...
    SET SESSION TRANSACTION READ WRITE;
    UPDATE table_x SET field_y=10;
    SET SESSION TRANSACTION READ ONLY;
    ...
    ```
     


