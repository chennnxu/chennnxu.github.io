---
layout: post
title:  PostgreSQL Note
# subtitle: A Pythonic Journey & Sessions Topic Modeling
cover-img: /assets/img/database.jpg
tags: [Database]
comments: true
---

For one project I am working on now about Software Heritage Graph Dataset, the data I need is huge up to 30+GB. To make the analysis more smoothly, I start learning PostgreSQL to help store, manipulate and retrieve data. This blog would be a summary for what I learn, basically the commands.

### To be continued..

```
connect database: psql \c DBNAME
quit database: \q
get help: help or \?(press q) or psql --help
list of databases: \l


create database: CREATE DATABASE NAME;
delete database: DROP DATABASE NAME;
describe database/table: \d or \d table name or \dt(just table)
create table: CREATE TABLE table_name (
    column name + data type + constraints if any,
    ... 
)
drop table: DROP TABLE NAME;

insert records into tables: INSERT INTO NAME (
    column name, ...
)
VALUES (value1, ...);
select all: SELECT * FROM NAME;
order by: ORDER BY column name (ASC/DESC);

Copying a Query Result Set: COPY ([Query]) TO '[File Name]' DELIMITER ',' CSV HEADER;

```

*Prefer use UPPERCASE syntax for SQL commands*