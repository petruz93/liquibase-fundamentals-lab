# Exercise 1 - Hello Liquibase

This exercise will help you to get started with Liquibase.

You will create the minimal configuration for a connection profile, a simple database schema and apply it using Liquibase.

## Steps:
1. From an empty directory, initialize a new Liquibase project:
   ```bash
   liquibase init project
   ```
2. Initialize and run a simple H2 database: 
   ```bash
   liquibase init start-h2
   ```
3. Fill your `changelog` and `liquibase.properties` files
4. Run the `update` command to apply the changes:
   ```bash
   liquibase update
   ```

## Goal:
You should get a working Liquibase project with a simple H2 database and a changelog very similar to the structure of this exercise folder.
