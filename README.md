# JIRA RUSH

I was given a tutorial assignment to fix bugs in the finished code, make changes and add functionality according to the terms.

- What I did in this project.
  - Deleted social media: vk, yandex.
  - Output sensitive information to a separate property file:
      - login
      - database password
      - identifiers for OAuth registration/authorization
      - mail settings
  - Reworked the testing so that all tests are executed in the test container.
  - Wrote tests for all public methods of the _ProfileRestController_ controller.
  - Added new functionality: adding tags to a task (REST API + implementation on the service).
  - Wrote a Dockerfile for the primary server.
  - Write a docker-compose file to run the server container along with the database and nginx.
  - Added localization for _mails_ email templates and _index.html_ start page.

### Stack of technologies used in the project

- Spring Boot
- Spring JPA
- Hibernate
- PostgreSQL
- Liquibase
- Spring Security
- Spring MVC
- Thymeleaf
- jQuery
- Swagger
- Caffeine
- Mapstruct
- Spring Test
- JUnit
- Test Container
- Docker

### Run the project

- Clone the project to your computer.
- Start the database server locally (PostgreSQL). I recommend doing this through docker.

Relevant command:
```
  docker run --name JiraRuch -p 5432:5432 -e POSTGRES_USER=jira -e POSTGRES_PASSWORD=JiraRush -d postgres
```

- Build the application: `mvn clean install`.
- Start the Spring Boot application `JiraRushApplication`
- To “see” how the application works you need to execute the `data.sql` script from `resources/data4dev`

Connecting to DB
```
  url: jdbc:postgresql://localhost:5432/jira
  username: jira
  password: JiraRush
```

### To log in without registration, you can use one of the following accounts:
| Role     | ADMIN           | USER            |
|----------|-----------------|-----------------|
| Login    | admin@gmail.com | user@gmail.com  |
| Password | admin           | password        |
