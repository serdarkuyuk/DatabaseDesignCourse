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


Normal key is made up key.

# Index
keys are in indexed for fast reach...
key is type of index
index speed up joins..
updating index is expensive.


## Clustered
is the data where the index is. (like a phonebook)
## Nonclustered
Data is not where the index is (like an index at the end of a book)
## Composite indexesÂ
index of two or more columns


## Look up tables
keys and membership...
Foreign constraints...
If there is an option.. look up is good idea.

* key is protect Integrity
* unique
* Improve functionality
* less work
* Allows for added complexity

### superkey
any number of columns that force every row to be unique
> user_id > made up
> username

### candidate key
least number of columns that force every row to be unique

### Primary key
username, email, column1+column2+columnN
every table has one. can be combination of two or more column

### Alternate Key
all the other candidate keys does not selected as Primary key
can be used index

### Surrogate key
User_id > has no world meaning

### Natural key
already stored in the db.
is an email...

### Foreign Key
it is a reference to primary key
NOT Null (cardinality) Required or not?
They can be empty... you can design to ...
can be change because it is reference

### Foreign key constraints
* FK constraints refers to the parent
MySQL
for parents
ON DELETE
ON UPDATE

for Child
RESTRICT (NO ACTION) can not change anything
CASCADE > if parent deleted all FK are also deleted
SET NULL > if parent is deleted all FK are assigned to null if foreign key is set to NOT NULL than this can not be executed.

## Categeory of keys
### Simple keys
One column

### Composite key
Multiple columns (first name + last name + email)

### Compound key
multiple columns but all columns are keys. (intermediotary)
combination of columns needs to be unique.

## Entity, EER Model, ER or ERD model
EER > Enhanced entity relationships model
ERD > Enhanced Relationships Diagrams

* Relation refer to a table

### Cardinality
relationship type between rows of one table with another table

 costumer table  <> credit card table

        -|-----------<---
Means one costumer have many cards

        ->------------|-
Means one cards have many costumer  

### Modality
means whether a child is required

costumer table  <> credit card table

       -|----------o-<- Can accept null charachters (zero or more)

       -|----------|-<- not null (one or more) every child has a parent

       -|----------o-|- (zero or more)

       -|----------|-|-  Not Null (one or more)  every child has a parent

# Normalization
Correcting them to integrity issues

## 1 NF (atomicity)
If a column has problem with multiple entries, create another table that refers to the  main table. PK is always unique, FK can repeat.

## 2 NF
get rid of partial dependencies. check out all columns and find out the Attributes that should belong to other tables.

## 3 NF  (Transitive dependency)
If a column is depend on another column. pull out the all columns that dependencies eachother and build a seperate table
