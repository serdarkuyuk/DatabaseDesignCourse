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
* Domain Integrity > column has the all expected values, charechters, numbers, setting rules of datatypes

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
* Atomic values > one thing. name, first name. should be one thing. not multiple things in to one column.

## Relationships

### One2One > 1:1
husband - wife, two entity have one to one relationships
person - SSN, two entity can have one assignment
### One2Multiple 1:N
User have multiple Comments
one user have many comments
### Many2Many  M:N
Multiple Class have multiple students

## Design  
> One2One - each Entity should have the others id
> One2Multiple - multiple entity will have one's id

Primary Key > parents
Foreign Key > child

> M:N - create an intermediotary table

a middle table (Child) combine two tables (Parent). a Foreign key will be there
1:M <-> N:1

## Binary Relationships


## Keys
* unique
* never changing
* never null

Natural key is an email...
Normal key is made up key.

## Index
keys are in indexed for fast reach...
key is type of index

## Look up tables
keys and membership...
Foreign constraints...

* key is protect Integrity
* unique
* Improve functionality
* less work
* Allows for added complexity
