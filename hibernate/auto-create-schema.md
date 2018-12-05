# Hibernate Auto Create Schema
To have hibernate auto create schema based on annotations do:
```
spring.jpa.hibernate.ddl-auto=create
```
The list of possible options are
(https://stackoverflow.com/a/1689769/3929657)

- **validate**: validate the schema, makes no changes to the database.
- **update**: update the schema.
- **create**: creates the schema, destroying previous data.
- **create-drop**: drop the schema when the SessionFactory is closed explicitly, typically when the application is stopped.

To have a naming strategy for columns
that prefers embedded underscores to mixed case names use
```
spring.jpa.hibernate.naming.implicit-strategy=org.hibernate.boot.model.naming.ImplicitNamingStrategyJpaCompliantImpl
```