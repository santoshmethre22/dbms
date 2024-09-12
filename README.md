# dbms
dbms notes
# DBMS and SQL Notes

## 1. Database and DBMS Overview
- **Database**: A structured collection of related data representing real-world aspects.
- **DBMS (Database Management System)**: Software for storing and retrieving users' data while ensuring appropriate security measures.

### Problems Solved by DBMS
1. **Data redundancy and inconsistency**
2. **Difficulty in accessing data**
3. **Data isolation – multiple files and formats**
4. **Integrity problems**
5. **Atomicity of updates**
6. **Concurrent access by multiple users**
7. **Security problems**

## 2. ER (Entity Relationship) Diagram
- A conceptual model representing the logical structure of a database using:
  - **Entity Sets**
  - **Attributes**
  - **Relationship Set**

### Types of Entity Sets
- **Strong Entity Set**: Contains sufficient attributes to uniquely identify its entities.
- **Weak Entity Set**: Lacks sufficient attributes for unique identification but contains a discriminator (partial key).

### Types of Relationships
- **Unary**: A relationship where only one entity set participates.
- **Binary**: A relationship where two entity sets participate.
- **Ternary**: A relationship where three entity sets participate.
- **N-ary**: A relationship where 'n' entity sets participate.

### Cardinality Constraints
- **One-to-One**: An entity in set A can be associated with at most one entity in set B.
- **One-to-Many**: An entity in set A can be associated with many entities in set B.
- **Many-to-One**: Multiple entities in set A can be associated with one entity in set B.
- **Many-to-Many**: Entities in set A can be associated with many entities in set B, and vice versa.

## 3. Relational Model

### Types of Keys
- **Super Key**: A set of attributes that can uniquely identify a tuple in the relation.
- **Candidate Key**: A minimal super key.
- **Primary Key**: A candidate key chosen to uniquely identify tuples.
- **Alternate Key**: Candidate keys not chosen as the primary key.
- **Foreign Key**: An attribute in one table that references the primary key of another table.
- **Composite Key**: A primary key that consists of multiple attributes.
- **Unique Key**: Similar to the primary key but allows one null value.

### Functional Dependency
- **Trivial Functional Dependency**: \( X \to Y \) is trivial if \( Y \subseteq X \).
- **Non-Trivial Functional Dependency**: \( X \to Y \) is non-trivial if \( Y \not\subseteq X \).

### Decomposition of a Relation
- **Lossless Decomposition**: No information is lost during decomposition.
- **Dependency Preservation**: All functional dependencies are preserved.

## 4. Normalization

### Normal Forms
- **1NF (First Normal Form)**: No multi-valued attributes; all attributes contain atomic values.
- **2NF (Second Normal Form)**: In 1NF and no partial dependency exists.
- **3NF (Third Normal Form)**: In 2NF and no transitive dependency exists.
- **BCNF (Boyce-Codd Normal Form)**: A stronger form of 3NF, ensuring that every non-trivial dependency has a super key on the left-hand side.

## 5. SQL

### Data Definition Language (DDL)
- **CREATE**: Defines a new database object (e.g., table, view, or index).
- **ALTER**: Modifies an existing database object.
- **DROP**: Deletes a database object.
- **TRUNCATE**: Deletes all rows from a table but keeps the structure.

### Data Manipulation Language (DML)
- **SELECT**: Queries data from a table.
- **INSERT**: Adds new data to a table.
- **UPDATE**: Modifies existing data in a table.
- **DELETE**: Removes data from a table.

### SQL Clauses
- **WHERE**: Filters records based on a condition.
- **ORDER BY**: Sorts results in ascending or descending order.
- **GROUP BY**: Groups rows that share a property.
- **HAVING**: Filters groups based on a condition.

### Aggregate Functions
- **MIN()**: Returns the smallest value.
- **MAX()**: Returns the largest value.
- **COUNT()**: Returns the number of rows.
- **AVG()**: Returns the average value.
- **SUM()**: Returns the total sum.

### SQL Joins
- **INNER JOIN**: Returns records with matching values in both tables.
- **LEFT JOIN**: Returns all records from the left table and matched records from the right table.
- **RIGHT JOIN**: Returns all records from the right table and matched records from the left table.
- **FULL OUTER JOIN**: Returns all records when there is a match in either table.

## 6. Transactions and ACID Properties

### Transaction States
1. **Active State**
2. **Partially Committed State**
3. **Committed State**
4. **Failed State**
5. **Aborted State**
6. **Terminated State**

### ACID Properties
- **Atomicity**: The transaction occurs entirely or not at all.
- **Consistency**: The database remains consistent before and after the transaction.
- **Isolation**: Multiple transactions do not interfere with each other.
- **Durability**: Once a transaction is committed, changes are permanent.

## 7. Schedules and Serializability

### Types of Schedules
- **Serial Schedules**: Transactions are executed one after the other.
- **Non-Serial Schedules**: Transactions are interleaved but can still be consistent.

### Serializability
- **Conflict Serializability**: Non-serial schedules that can be transformed into serial schedules by swapping non-conflicting operations.
- **View Serializability**: Non-serial schedules that produce the same results as a serial schedule.

## 8. Relational Algebra

### Basic Operators
- **σ (Selection)**: Selects rows based on a condition.
- **Π (Projection)**: Selects columns.
- **× (Cross Product)**: Combines two relations.
- **∪ (Union)**: Combines two relations without duplicates.
- **− (Difference)**: Returns rows in one relation but not in another.

### Extended Operators
- **∩ (Intersection)**: Returns rows present in both relations.
- **⋈ (Join)**: Combines rows from two tables based on a related column.

## 9. Indexing and File Structures

### Index Types
- **Primary Index**: Created on ordered data, based on the primary key.
- **Clustering Index**: Created on ordered non-key data.
- **Secondary Index**: Provides a secondary method of accessing data.

### B-Trees and B+ Trees
- **B-Trees**: Balanced tree data structure, allowing for efficient searches.
- **B+ Trees**: Similar to B-Trees but with better performance for range queries.

---


