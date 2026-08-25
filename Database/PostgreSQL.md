# Content
- PostgreSQL is an open-source, object-relational database management system known for advanced SQL support, extensibility, data integrity, concurrency, and reliability
- [Connect]()

## Basic Commands
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
