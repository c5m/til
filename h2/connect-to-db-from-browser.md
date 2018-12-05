# Connect to DB Through Browser
When using Spring Boot use the following jdbc string:

```
spring.datasource.url= jdbc:h2:mem:testDB;DB_CLOSE_DELAY=-1;DB_CLOSE_ON_EXIT=FALSE;
```

And then in the H2 console make sure the connect string is:
```
jdbc:h2:mem:testDB
```
Otherwise you won't see any data.

The flag `DB_CLOSE_DELAY=-1` ensures other processes can connect to H2.