# Just Tech News (Java)

Spring Boot web app where the tech community can share links, upvote posts, and discuss news in threaded comments.

## Stack
- Spring Boot 2.7 (Web, Data JPA, Thymeleaf)
- MySQL 8 with Spring Session JDBC
- BCrypt password hashing

## Run locally
1. Ensure Java 11+ and Maven (or `./mvnw`) are available.
2. Start MySQL and allow access to `jdbc:mysql://localhost:3306/just_tech_news_java_db`. Export `DB_PASSWORD` for the configured user (default username is `root`).
3. `./mvnw spring-boot:run`
4. Open http://localhost:8082 to browse the feed or log in to manage your dashboard.

## Routes at a glance
- Public feed at `/` plus authenticated dashboard at `/dashboard`.
- REST endpoints under `/api` for posts, users, comments, and votes.
- Sessions back user actions like upvoting and commenting; passwords are stored hashed.

## Testing
`./mvnw test` uses the same MySQL configuration. Provide a reachable database (or adjust `spring.datasource.*`) before running tests; otherwise they will fail to connect.

### Link to Heroku deployment
[Heroku link](https://cc-java-api-21.herokuapp.com/)

### Screenshot

![img](src/main/resources/static/image/Justtechnewjava.png)

### Author & Contact Info
Boyd Roberts

[Coleyrockin GitHub](https://github.com/coleyrockin)

[Coleyrockin@aol.com](mailto:Coleyrockin@aol.com)
