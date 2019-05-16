# SQL Execution Order

A query in SQL will be executed in the following order:

1. `FROM` clause
2. `WHERE` clause
3. `GROUP BY` clause
4. `HAVING` clause
5. `SELECT` clause
6. `ORDER BY` clause

Hence aliases created in the `SELECT` clause can only be used in the `ORDER BY` clause.

(Note that Postgres allows the use of aliases in `GROUP BY` clauses but this might be problematic if a schema change creates a column with the same name as alias. Then the base column gets priority).