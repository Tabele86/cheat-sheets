# PostgreSQL

## Docs
* [pgAdmin](https://www.pgadmin.org/docs/pgadmin4/latest/index.html)

## Cheat-sheet

* psql -U postgres

* CREATE DATABASE ___

> \c ___

* SELECT * FROM ___;
> (* = all)

* INSERT INTO ___(a, b, c) VALUES (''.'','');

* CREATE TABLE ___();
- Example:
> CREATE TABLE login(
	ID serial NOT NULL PRIMARY KEY,
	secret VARCHAR (100) NOT NULL,
	name text UNIQUE NOT NULL
);

* ALTER TABLE table_name ADD column datatype;

* UPDATE table_name
SET some_column = some_value
WHERE some_column = some_value;

* (to add multiple changes use OR)
- Example:
> UPDATE users SET score = 100 WHERE name='john' OR name='sally';

* LIKE (allows us to add a condition)
- Example:
> SELECT * FROM users WHERE name LIKE 'A%';

> (%=anything after/before)

> SELECT * FROM users WHERE name LIKE '%y';

* ORDER BY(descending or ascending)
> SELECT * FROM users ORDER BY name DESC;
> 
> SELECT * FROM users ORDER BY name ASC;
* MATH
> SELECT AVG(some_column) FROM table_name;

> SELECT SUM(some_column) FROM table_name;

> SELECT COUNT(some_column) FROM table_name;
