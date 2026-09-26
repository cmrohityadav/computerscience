# Content
- PostgreSQL is an open-source, object-relational database management system known for advanced SQL support, extensibility, data integrity, concurrency, and reliability
- [Basic Terminal Commands](#basic-terminal-commands)
- [Connect]()
- [Database](#Database)
- [schema](#schema)
- [Tables](#tables)
- []()


## Basic Terminal Commands
### connect
```bash
psql -h HOST -p 5432 -U USERNAME -d DATABASE_NAME

psql -h localhost -p 5432 -U postgres -d mydatabase

# Agar PostgreSQL same machine par installed hai
psql -U postgres

# Specific database
psql -U postgres -d mydatabase

```

### check all db
```bash
\l
```
### Database connect/change karo
```bash
\c mydatabase
```

### Database create
## 3. psql / Terminal Commands

- \d       → table structure
- \du      → users/roles
- \dn      → schemas
- \dv      → views
- \df      → functions
- \?       → psql commands
- \h       → SQL help
```bash
CREATE DATABASE mydatabase;
```

### Database delete
```bash
DROP DATABASE mydatabase;
```
### Tables dekho
```bash
\dt
```
### Table structure dekho
```bash
\d users;
```
### PostgreSQL se bahar niklo
```bash
\q
```

## Database
- CREATE DATABASE
- ALTER DATABASE
- DROP DATABASE
- Database naming
- Database connection

## Schema
- It is namespace area that live inside a database
- Schema ko database ke andar folder samjho
- Schema ka kaam mainly database objects(tables, etc) ko organize aur namespace dena hai
```
Database = poora office
│
├── HR Schema = HR department
│   ├── employees table
│   └── salaries table
│
├── Sales Schema = Sales department
│   ├── customers table
│   └── orders table
│
└── Finance Schema = Finance department
    └── payments table

```
- CREATE SCHEMA
```sql
CREATE SCHEMA IF NOT EXISTS store;

SELECT schema_name FROM information_schema.schemata WHERE schema_name='store';

```
- **ALTER SCHEMA**
- Existing schema ko modify/rename karta hai.
```sql
ALTER SCHEMA store RENAME TO sales;
```
- **DROP SCHEMA**
- Schema ko delete karta hai
```sql
DROP SCHEMA IF EXISTS store;
-- Important: Schema ke andar objects (tables, views, etc.) hain to normal DROP SCHEMA fail ho sakta hai.


-- Schema aur uske saare objects delete karne ke liye:
DROP SCHEMA store CASCADE;
```
- **public schema**
- PostgreSQL database mein normally ek default schema hota hai: public

- **schema.table**
- ek hi db me 2 same naam table ho skte isliye
```sql
SELECT * FROM store.products; SELECT * FROM admin.products;
```

## Tables
### CREATE TABLE
- NEW Table Banna
```sql
CREATE TABLE IF NOT EXISTS store.categories(
id INTEGER,
name TEXT
);

CREATE TABLE IF NOT EXISTS store.products(
id INTEGER,
category_id INTEGER,
name TEXT,
price NUMERIC
);
```
28:12
### ALTER TABLE
```sql

```
### DROP TABLE
```sql

```
### RENAME
```sql

```
### ADD COLUMN
```sql

```
### DROP COLUMN
```sql

```
### ALTER COLUMN
```sql

```


## 7. Data Types
- INTEGER
- BIGINT
- NUMERIC / DECIMAL
- REAL / DOUBLE PRECISION
- VARCHAR
- TEXT
- BOOLEAN
- DATE
- TIME
- TIMESTAMP
- TIMESTAMPTZ
- UUID
- JSON / JSONB
- ARRAY

## 8. CRUD
### INSERT
### SELECT
### UPDATE
### DELETE

## 9. SELECT Deep Dive
- WHERE
- DISTINCT
- ORDER BY
- LIMIT
- OFFSET
- aliases
- expressions
- NULL
- IS NULL
- IS NOT NULL

## 10. Operators
- =, !=, <>, >, <, >=, <=
- AND
- OR
- NOT
- IN
- BETWEEN
- LIKE
- ILIKE
- ANY
- ALL

## 11. Functions
### String Functions
### Numeric Functions
### Date/Time Functions
### NULL Functions
- COALESCE
- NULLIF

## 12. Aggregate Functions
- COUNT
- SUM
- AVG
- MIN
- MAX

## 13. GROUP BY / HAVING
- GROUP BY
- HAVING
- WHERE vs HAVING

## 14. Constraints
- PRIMARY KEY
- FOREIGN KEY
- UNIQUE
- NOT NULL
- CHECK
- DEFAULT

## 15. Relationships
- One-to-One
- One-to-Many
- Many-to-Many
- Junction/Join Table

## 16. JOINS
- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- FULL JOIN
- CROSS JOIN
- SELF JOIN

## 17. Subqueries
- Scalar subquery
- IN subquery
- EXISTS
- Correlated subquery

## 18. CTE
- WITH
- Multiple CTEs
- Recursive CTE

## 19. Set Operations
- UNION
- UNION ALL
- INTERSECT
- EXCEPT

## 20. Views
- CREATE VIEW
- ALTER VIEW
- DROP VIEW
- Materialized View

## 21. Indexes
- Why indexes?
- CREATE INDEX
- DROP INDEX
- B-tree
- Hash
- GIN
- GiST
- Composite indexes
- Partial indexes
- Index usage

## 22. Transactions
- BEGIN
- COMMIT
- ROLLBACK
- SAVEPOINT

## 23. ACID
- Atomicity
- Consistency
- Isolation
- Durability

## 24. Concurrency
- Locks
- Row locks
- MVCC
- Isolation Levels
- Deadlocks

## 25. Roles & Permissions
- CREATE ROLE
- CREATE USER
- GRANT
- REVOKE
- Role inheritance
- Ownership

## 26. PostgreSQL Advanced
- Sequences
- SERIAL / IDENTITY
- ENUM
- UUID
- JSONB
- Arrays
- Full-text search
- Window Functions
- FILTER
- UPSERT
- RETURNING

## 27. Functions & Procedures
- CREATE FUNCTION
- Parameters
- RETURN
- CREATE PROCEDURE
- PL/pgSQL basics

## 28. Triggers
- Trigger kya hai?
- BEFORE / AFTER
- INSERT / UPDATE / DELETE
- Trigger Function

## 29. Performance
- EXPLAIN
- EXPLAIN ANALYZE
- Query optimization
- Index optimization
- Sequential Scan
- Index Scan
- Query planning

## 30. Backup & Restore
- pg_dump
- pg_restore
- pg_dumpall
- Backup strategies

## 31. PostgreSQL with Applications
- Node.js
- Python
- Java
- Connection Pooling
- Prepared Statements
- ORM basics

## 32. Real-World Database Design
- Normalization
- 1NF / 2NF / 3NF
- Denormalization
- Naming conventions
- Schema design
- Soft delete
- Audit columns

## 33. Common Interview Questions
- WHERE vs HAVING
- DELETE vs TRUNCATE vs DROP
- PRIMARY KEY vs UNIQUE
- INNER vs LEFT JOIN
- VARCHAR vs TEXT
- UNION vs UNION ALL
- EXISTS vs IN
- Index kya hai?
- ACID kya hai?
- MVCC kya hai?
- Normalization kya hai?