---
sidebar_position: 3
---

# Steps

- Following is the flow you would follow while using the package:

  - If you already have a database with triggers, procedures or functions, run the `generate` command to grab all of those queries as `.sql` files for you and put them in the specified folder.

  - Create parent folders for your sql files as specified in your config with and create the SQL objects with `.sql` files

  - If you did follow step 1, you **will have to remove the `_tableName` suffix** after the trigger file name(POSTGRES ONLY)

  - The `migrate` command that checks for the diff **requires your files to have the same name as that of the database object**. For example if you have a procedure named `hello_world`, you need to name the file as `hello_world.sql`. This creates a `migrationsDirectory` in your project root to house all those migrations.

  - After the migration is created, you can run the `up` command which would apply the migration. It would also create the table you specified for migrations via the `migrationsTable` property in the config.

  - If you want to revert the last run migration, simply run the `down` command

## SQL File Example

- The following is an example sql file:

  ```sql title="HelloWorld.sql"
  CREATE PROCEDURE HelloWorld
  AS
  BEGIN
      PRINT 'Hello, this is a simple procedure!';
  END;
  ```
