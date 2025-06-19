# Exercise 6 - Rollback in production

What happens when you need to roll back changes in a production environment?

After your application has been released in production, you may find that you need to revert some changes due to bugs or other issues. This is where the rollback functionality of Liquibase becomes crucial.
Because it is likely that your database has already begun to be filled with data of the users. <br>
If you roll back changes that involve the structure of the database, you could <u>**lose data**</u> that has been added.

What can you do to perform a rollback in production without losing data?

## Steps:
1. Set up the exercise by taking the current exercise folder (exercise-6).
2. Apply the changes.
3. Perform rollbacks until you reach the point where you undo the creation of the `company` table.
4. Make some changes to the `company` table, such as merging the `address1` and `address2` columns into a single `address` column.
5. Run the `liquibase update` command to apply the changes.
6. What do you observe? What happens to the data in the `company` table?
7. Can you find a way to perform the rollback without losing data? If so, how?

## Hint & Caveats:
When you perform a rollback in Liquibase, it will revert the database schema to the state it was in at the time of the specified change set. If you have made changes to the structure of a table (like dropping a column or changing its type), and then you roll back to a previous state, Liquibase will attempt to restore the table to that previous state.
However, if the rollback involves dropping a column that contains data, that data will be lost.
This is because Liquibase does not automatically preserve data when rolling back structural changes.

There are several ways to prevent data loss when in production.

- One way is to use the `preConditions` tag in your changelog file to check if data exists within tables or columns that you are about to drop or modify. If data exists, you can skip the changes or handle them differently.
- Another way is to create a backup of your database before performing any rollbacks. This way, you can restore the data if something goes wrong. <br>
   The problem with this approach is that it requires additional storage, management of backups, can be time-consuming, and may require a lot of testing to ensure that the backup and restore process works correctly. <br>
   Essentially, it may not be feasible or recommended for any reason by your company.

# Proposed Solution:
You can replace the rollback action making a new changeset and a new Change Type, or a custom SQL script, that merges the `address1` and `address2` columns into a single `address` column.

<u>**Remember:**</u> <br>
Rollbacks in production should be handled with care, and it's essential to have a strategy in place to prevent data loss. Always test your rollback procedures in a staging environment before applying them in production. ;)
