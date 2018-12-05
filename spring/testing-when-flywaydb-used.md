# Testing when Flyway dependency used
(taken from: https://www.ivonet.nl/2016/08/16/spring-boot-with-flyway-and-how-to-get-your-tests-working/)

#### Challenge
You have a spring boot application with flyway migration scripts for a MySQL database. Now your tests are failing because you don’t have the database available during unit testing and flyway is complaining.

#### Solution
Use an in memory H2 database in MySql mode.

#### How
Create a file called `flyway_init.sql` in `src/test/resources` with the following content
```SQL
CREATE SCHEMA IF NOT EXISTS "public";
```
create an `application.yml` file in `src/test/resources` with the following flyway config:
```yaml
spring:
  datasource:
    url: jdbc:h2:mem:DBNAME;MODE=MySQL
    username: sa
    password:
    driver-class-name: org.h2.Driver
flyway:
  url: "jdbc:h2:mem:DBNAME;MODE=MySQL;INIT=RUNSCRIPT FROM 'classpath:flyway_init.sql'"
  user: sa
  password:
  baseline-on-migrate: true
```
Add a test dependency on h2 to the `pom.xml`
```XML
<dependency>
    <groupId>com.h2database</groupId>
    <artifactId>h2</artifactId>
    <version>1.4.183</version>
    <scope>test</scope>
</dependency>
```