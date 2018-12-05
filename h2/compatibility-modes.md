# Compatibility Modes
H2 has several compatibility modes which makes it behave more like other DBs.  
These are set either:
1. in the JDBC string 
`jdbc:h2:~/test;MODE=<compatibility-mode>`
2. with the SQL statement `SET MODE <compatibility-mode>`

List of compatibility modes:

* DB2
* Derby
* HSQLDB 
* MS SQL
* MySQL 
* Oracle 
* PostgreSQL 
* Ignite 

See http://www.h2database.com/html/features.html#compatibility for details.