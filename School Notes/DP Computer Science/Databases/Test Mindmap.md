---

mindmap-plugin: basic

---

# Haha Databases
---
#### Definitions
Database
- Structured set of data held in a computer
- Organized collection of structured information/data

Information System
- Organized system for a collection, organization, storage, and communication of info
- Group of components that interact to produce info
	- Hardware
	- Software
	- Data
	- People
	- Network
	- Process
- Databases are a component within an info system

#### Why databases?
- Size of data - if large data set, bad efficiency. AKA doesnt scale up well
- Ease of updating data - (maybe an older concept) bad for collaborative data processing
- Accuracy - Human errors (Spelling, date, quantity)
- Security - Cant maintain privacy for sensitive info (banking, healthcare)
- Redundancy - Managing copies of data is hard for humans
- Incomplete data - Data integrity is threatened as there is no validation process

#### Types of Databases
- Relational Databases
- Object-oriented Databases
- Distributed Databases
- Data Warehouses
- NoSQL Databases
- Graph Databases
- OLTP Databases
- Open Source Databases
- Cloud Databases
- Multimodel Databases
- Document/JSON Databases
- Self-driving Databases

#### Database Management System (DBMS)
- A software package that abstracts a database.
- Provides
	- Centralized view of data that can be accessed in many ways
	- Security
	- Data Integrity
	- Concurrency
	- Uniform Administrative Procedures
	- Performance Monitoring
	- Backup
	- Recovery
#### Transactions
- Work performed within a DBMS against a database. Treated independently.
- Provide
	- Reliable units of work that allow correct recovery.
	- Isolation between programs accessing a database concurrently.
- Ideal properties (ACID)
	- Atomicity (transaction completes at once or not at all)
	- Consistency (before and after, prevents corruption)
	- Isolation (multiple can occur independently)
	- Durability (changes occur despite system failure)
- Implementing ACID
	- Locking method
		- Transactions prevent other transactions from accessing the data it is accessing
		- Uses two-phase locking: Expanding Phase/Shrinking Phase
	- Multiversioning
		- Database provides each transaction with unmodified version of data
#### Basic Transactions
- CRUD - Create, Read, Update, Delete
- CREATE - Inserting new data into a database with what is already defined
- READ - Access data in database
- UPDATE - Modify data that exists in database
- DELETE - Remove data from database
#### Validation & Verification
- Verification - Ensure user does not make a mistake when inputting data, done on copies
- Validation - Ensure data is valid, that it conforms to data requirements, done on the og doc
- Validation Methods:
	- Type - only take in specific data types
	- Presence - Requires users to enter data on required fields (contrast with optional)
	- Unique Identifier - Check that only one exist
	- Range Check - Domain Restriction check (like the OutOfRangeException)
	- Format - Like types, but specific. E.g. License Plate numbers
	- Restricted Choice - Like a dropdown. Eg. days of the week
		- Benefits: Faster data entry (Select>Type), Accurate (PICNIC)
#### DBMS Functions
- Provide Security
	- Access Control (authorization)
	- Database auditing (ensure authorization)
	- Authentication (Provide identity)
	- Encryption (Encoding)
	- Integrity Control (Maintenance of accuracy & consistency of data)
	- Backups (Copies stored elsewhere)
	- Application Security (Dealing with vulnerabilities)
- Self-describing nature
	- Data + Metadata (Describes the data, information about the data)
- Insulation between programs and data abstraction
	- Changes in structure will affect connected programs
	- With DBMS, changes will be in DBMS, not in connected programs
- Support of Multiple Views of data
	- A view is a subset of the database.
	- Different users have different views of the system
- Sharing data & multiuser transaction processing
	- Many users can access the same database at the same time
- Control of data redundancy
	- Data item stored in only one place
- Data Sharing
	- Users access same data
	- Applications access same data
	- Generate more data from same data
- Enforcement of integrity constraints
	- Constraints like data type, format
- Restriction of unauthorized access
	- ReadOnly
	- Read/Write
	- User roles
	- Application roles
- Data Independence
	- Data&Metadata separated from applications
	- Changes to data schema are transparent to applications
- Transaction processing
	- Consitent interface
	- Atomic operations
	- Rollback
- Backup & recovery
	- Incorrect transactions
	- Hardware Failure
	- Software Errors
	- Data Corruption
	- User Error
	- Power Interruption

#### Data Modelling
- Describe:
	- Data type
	- Relationship between items
	- Constraints

#### Schema
- Overall description of a database, often in the form of ERDs (entity relationship diagram)
- External Schema: Multiple
- Multiple subschema: Display multiple external views of data
- Conceptual Schema: Only one. Includes data items, relationships, constraints, in ERD
- Physical Schema: Only one
##### Conceptual Model
- Defines what the system contains
- Created by stakeholders and data architects
- Organize, scope, define business concepts and rules
##### Logical Model
- Defines how the system should be implemented
- Created by data architects and business analysts
- Develop technical map of rules and data structures
##### Physical Model
- Define how system should be implemented using a specific DBMS system
- Created by DBA and developers
- Actual implementation of database

#### Key Terms
- Table - collection of rows. Usually has a name, all the rows have the same shape.
- Record - Collection of column values. Every row has the same shape.
- Field - Smallest unit of storage in a relational database. Every column has a name and data type. Columns are grouped into rows, which are grouped into tables.
- Primary Key - Attribute(s) that uniquely identifies a row/record in a relation
- Secondary Key - Combination(s) of fields that is basis for retrieval. Non unique. One key may refer to many records.
- Foreign Key - Attribute(s) in a relation whose value matchesa primary key in another relation. Created in dependent table, refers parent table.
- Candidate Key - Combinations of fields that are not used as primary keys
- Composite Primary Key - Primary key with two or more attributes
- Join - Combination of tables into a single view.

#### Issues with redundancy
- Redundancy - duplicaton of data
- Insertion Anomaly: Cant insert record without inserting unrelated data
- Update Anomaly: Updating a data may require updating many records
- Deletion Anomaly: Deleting data may require deletion in many locations

#### Referential Integrity
- Integrity and usability of relationship by establishing rules/constraints
- To establish RI
	- Create primary key in parent table & foreign in dependent
	- Define what actions are allowed when data is added/modified
- Rules
	- Insert - What happens when inserting a value into foreign key column without corresponding primary key value in parent table.
	- Update - Controls data modification so foreign value cant be updated to value that doesnt correspond to primary value
	- Delete - What happens when deleting a row from parent table

#### Database Administrator (DBA)
- Duties
	- Installing/upgrading database applicaton
	- Modifying database structure
	- Control/monitor user access
	- Plan for backup/recovery of database

#### Database Recovery
Causes for errors:
- User error
- Statement Failure
- Process Failure
- Network Failure
- Database Instance Failure
- Media Failure