# SQL

* DDL > data definition language
* DML  > data manipulation language

**SQL keyword**
SELECT, FROM etc. should not be used

Null > no information, emptiness
anomalies > errors within data Integrity.
Integrity > to prevent anomalies

### Entity
user, tables for
### Attributes
name of user, address, password etc...


# Schemas

## Conceptual
general concepts...
how tables related

sales depends on user
child depends on parents

### Logical
Error...
how many people use it

### Phsical
specificel
which server
access data... form?
phsical programming...
testing...
security

# Database Design

* with no data integration issues
* update anomalies (two same information example address)
* should be one table

user table  comment table
if user deleted, delete all the comments

## Data Integrity

* Entity Integrity > uniqueness among tables
* Referential Integrity > keep the connections, two tables should be referencing right table
* Domain Integrity > column has the all expected values, characthers, numbers, setting rules of datatypes

two table should be relationships...

Entity user id... a key

## Data Types

* Char(20)

## Terms
* Tuple > a row in a table, all information about Entity
* Field > column (Attributes)
* Entry > row  (record, Tuple)
* Schema > drawn out structure of Database
* normalization > steps to follow to get best design
* naming convention > consistency of names (table, column etc)
* keys > make uniqueness within table

* views (custom views) taking data from db and illustrating in different ways that is how is actually stored (eg. viewing friends webpage in facebook)

### Atomic values
one thing. name, first name. should be one thing. not multiple things in to one column.
