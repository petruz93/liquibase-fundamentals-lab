# Liquibase Fundamentals lab

Support repository for my course **Liquibase Fundamentals** at Ringmaster Academy.

## Prerequisites

### Required:
- [Liquibase](https://github.com/liquibase/liquibase/releases) installed on your machine
- Liquibase directory added to your system `PATH`
- A database server running locally (e.g., PostgreSQL, MySQL, H2, etc.)
- A database created for the exercises
- A changelog root file
- A `liquibase.properties` file in the root directory of every exercise with the following content:
  ```properties
  url=<string-connection-url>
  username=your_username
  password=your_password
  ```

### Optional:
- A simple project structure with [Spring Boot](https://start.spring.io/)+Java or [Node.js](https://nodejs.org/en/download)
- A conteinerized database using [Docker](https://www.docker.com/products/docker-desktop/)
- A database client (e.g., DBeaver, pgAdmin, MySQL Workbench) to visualize the database changes
