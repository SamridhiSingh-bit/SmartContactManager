# Smart Contact Manager

A Spring Boot web application for managing contacts. The current version includes Home and About pages rendered with Thymeleaf, a shared navbar/layout, and a MySQL-backed JPA setup.

## Requirements

- Java 21 or later
- MySQL

The project includes the Maven Wrapper, so a separate Maven installation is not required.

## Run locally

1. Create the database in MySQL:

   ```sql
   CREATE DATABASE smartcontact;
   ```

2. Set `DB_PASSWORD` to the password for the MySQL `root` account. In PowerShell, for the current terminal:

   ```powershell
   $env:DB_PASSWORD = "your-mysql-password"
   ```

3. Start the application from the backend directory:

   ```powershell
   
   ```

The application listens on port `8282`:

- Home: http://localhost:8282/home
- About: http://localhost:8282/about

## Project structure

```text
backend/
├── src/main/java/                 Application, controller, repository, and entities
├── src/main/resources/
│   ├── static/css/style.css       Navbar and page styles
│   ├── templates/                 Thymeleaf page templates
│   └── application.properties     Application and datasource configuration
├── src/test/                      Tests
├── mvnw
└── pom.xml
```

The datasource password is read from the `DB_PASSWORD` environment variable. Hibernate is configured to update the schema automatically during development.
