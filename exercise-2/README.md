# Exercise 2 - Duplicated author-id

This exercise will help you to understand what happens when two changesets are defined with the same `author` and `id` attributes.


## Steps:
1. Initialize the project folder like in the exercise-1 or create a new one.
2. Write two changesets in your changelog file with the same `author` and `id` attributes.
4. Run the `update` command to apply the changes:
   ```bash
   liquibase update
   ```
5. Observe the output and the database state. What happens? Why?
6. Try to solve the issue.
