# File System v/s DBMS
## DDR AC IQ BRS

| Feature                 | File System                         | DBMS                                 |
| ----------------------- | ----------------------------------- | ------------------------------------ |
| **Definition**          | Manages individual files on storage | Manages Structured databases         |
| **Data Management**     | Individual Files                    | Structured databases with tables     |
| **Redundancy Control**  | High redudancy and inconsistency    | Reduces redundancy and inconsistency |
| **Data Integrity**      | Limited Support                     | Enforces rules                       |
| **Access Control**      | Basic permissions                   | Defines user roles                   |
| **Query Processing**    | Manual and Sequential               | SQL                                  |
| **Concurrency Control** | Limited or none                     | Mechanisms to hanfle concurrency     |
| **Backup and Recovery** | Manually Done                       | Automatable                          |
| **Data Relationships**  | No inherent support                 | Inherent support for relation        |
| **Scalability**         | Less scalable                       | Highly scalable                      |

# DBMS Languages

```mermaid
graph TD
    A[DBMS Languages] --> B[DDL]
    A --> C[DML]
    A --> D[DCL]
    A --> E[TCL]

    B --> B1[CREATE]
    B1 --> B2[ALTER]
    B2 --> B3[DROP]
    B3 --> B4[TRUNCATE]

    C --> C1[SELECT]
    C1 --> C2[INSERT]
    C2 --> C3[UPDATE]
    C3 --> C4[DELETE]

    D --> D1[GRANT]
    D1 --> D2[REVOKE]

    E --> E1[COMMIT]
    E1 --> E2[ROLLBACK]
    E2 --> E3[SAVEPOINT]
```
## Data Definition Language
DDL is used to define and manage database structures such as schemas, tables, and indices.
- **CREATE:** create new objects like tables or rows
- **ALTER:** Modify structure of existing db object
- **DROP:** Delete db objects
- **TRUNCATE:** Remove all records from the table, but keep the table

## Data Manipulation Language
DML is used to retrieve, insert, update and delete data in a database
- **SELECT:** used to retrieve data from a database
- **INSERT:** used to add new rows into a table
- **UPDATE:** Used to modify existing values in a table
- **DELETE:** Used to remove rows from a table

## Data Control Language
Used to control Access to data within a database
- **GRANT**
- **REVOKE**

## Transaction Control Language
Used to manage transactions and ensure data integrity
- **COMMIT:** Used to save all changes made in the current transaction
- **ROLLBACK:** Used to undo changes made in the current transaction
- **SAVEPOINT:** Used to set a savepoint in the middle of a transaction


# Structure / Architecture

# Types of DBMS
- Relational DBMS: An RDBMS stores data in tables with rows and columns, used SQL (Structured Query Language)
- Object-Oriented DBMS: Am OODBMS stores data as objects, which can be manipulated using object-oriented programming languages
- NoSQL DBMS: Stores data in non-relational data structures, such as key-value pairs
# Users
## DB Admin
- Is a person or team who defines the schema and controls the three levels of the database, they will then create a username and password to access the DB.
- They are also responsible for providing security to the DB, and allows only authorized personnel to access/modify the data
- They have privileges to perform all the languages, DML, DCL, TCL, DDL
- They maintain the system and perform repairs.
- The DBA account is also called the superuser account
- The responsibility of backup and recovery lies on the hands of the DMA.
## Naive End Users
- They are the unsophisticated users who don't have DBMS knowledge but are the people using the DBMS from their endpoint
## System Analyst
- A system analyst is a user who aanalyses the requirements of End users

## Sophisticated User
- They are the engineers, scientists, business analysts who are familiar with the Database and develop new tools or integrate the Database into their tools to perform their duties, they have access to Query the DB Directly

## DB Designers
- The users who design the structure of the Database which includes tables, indexes, views, and triggers.
- They control what data enters the Database and how the data attributes are related

## Application Programmers
- They are the software engineers who implement the DB into the backend of the deliverable application they are building
- They use various languages and frameworks to integrate the database into the backend programming such as Node.js

## Casual Users
- They are the ones who occasionally access the DB, but each time they access it, they require new information, like top level management

## Specialized Users
- Who write specialized database programs that do not fit into the traditional data-processing framework

![[DBMS.png]]

DBA SCHEMA DDL_COMPILER 
USERS QUERY QUERY_PROCESSOR 
APP DML COMPLIER
DATA_DICT    AUTH_CTRL
QUERY_OPT     CMD_PRC    INTEG_CHKR
SCHEDULER     TRXN_MGR
REC_MGR    BUFF_MGR
