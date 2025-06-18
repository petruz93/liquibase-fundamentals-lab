# Exercise 5 - Rollback Test Cycle

This exercise will help you to understand how to test rollback functionality and the best practices for managing rollback life cycle in Liquibase.

## Steps:
1. Setup the exercise by taking the current exercise folder (exercise-5).
2. Apply the changes.
3. Before rolling back, check your rollback instructions running the following command:
   ```bash
   liquibase rollback-count-sql --count=<number>
   ```
4. If you don't get any errors, you can proceed with the rollback. Use the `rollback-count` command to revert the changes:
   ```bash
   liquibase rollback-count --count=<number>
   ```
5. Run again `liquibase update` to reapply the changes without modifying the changelog file. This will help you to ensure that the rollback and reapply cycle works as expected.
6. What results do you get?
7. If everything works as expected, your rollback instructions are correct. Well done!!
