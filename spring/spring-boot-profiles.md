# Spring Boot Profiles
Spring Boot supports the concept of profiles.
What this does is load your `application.properties` based on your profile.
For instance we can run our program with
```sh
mvn spring-boot:run -Drun.jvmArguments="-Dspring.profiles.active=local"
```
which will then load our local profile and read from `application-local.properties`