# Exercise 4 - Rollback changesets

This exercise will help you to understand how rollbacks work in Liquibase and how to perform a change in a changeset that has already been executed.

## Steps:
1. Start from the result you get in the previous exercise (exercise-3).
2. Restore your changelog file to the state before you edited the changeset, getting back to the original changeset definition.
3. Write the rollback instructions for the changesets you have in your changelog file. You can use the `rollback` tag or the `rollback` attribute in the changeset.
4. Run the rollback command to revert the changes:
   ```bash
   liquibase rollback --tag=<tag>
   ```
   Replace `<tag>` with the tag you used in your changeset if you are rolling back to a specific point.
    1. Alternatively, you can use the `rollback-count` command to roll back a specific number of changesets:
        ```bash
        liquibase rollback-count --count=<number>
        ```
        Replace `<number>` with the number of changesets you want to roll back.
5. Edit the changeset in your changelog file to make a change (e.g., add a new column or modify an existing one).
6. Apply the changes.
