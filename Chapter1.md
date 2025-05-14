# Drawbacks of Using File System to Store Data  

- **Data redundancy and inconsistency**  
  - Multiple file formats, duplication of information in different files.  
- **Difficulty in accessing data**  
  - Need to write a new program for each task.  
- **Data isolation**  
  - Data scattered in multiple file formats.  
- **Integrity problems**  
  - Integrity constraints (e.g., account balance > 0) are buried in program code rather than stated explicitly.  
  - Hard to add or modify constraints.  
- **Atomicity problems**  
  - Transactions (a sequence of operations treated as a single unit) may not complete properly.  
- **Concurrent access issues**  
  - Multiple users accessing data simultaneously can cause conflicts.  
- **Security problems**  
  - Lack of centralized access control.  

# Data Management  

- **Storage**  
- **Retrieval**  
- **Transaction** (A logical unit of work in a database)  
- **Audit**  
- **Archival**  

# Why Leave the File System?  

- Requires more manual operations.  
- Limited row capacity.  
- Maintaining consistency is difficult.  
- No built-in way to enforce constraints during concurrent processing.  
- System crashes can lead to severe data loss.  
- Cannot easily assign different permissions to users in a centralized way.  

# Levels of Abstraction  

- **Physical level:** Describes how data is stored (e.g., file structures, indexing).  
- **Logical level:** Describes data relationships (e.g., tables, fields, keys).  
- **View level:** Application-specific data presentation (hides complex details).  

# Schema and Instance  

- **Schema:** The structure/design of the database (like a blueprint).  
  - **Logical schema:** Defines tables, relationships, constraints.  
  - **Physical schema:** Describes storage (e.g., indexes, file organization).  
- **Instance:** The actual data stored in the database at a given time.  

# Physical Data Independence  

- Ability to change the physical storage (e.g., indexing, file structures) without affecting the logical schema.  

# DDL (Data Definition Language)  

- Used to define the database schema (e.g., `CREATE TABLE`, `ALTER TABLE`).  
- Generates table templates stored in the **data dictionary** (a metadata repository).  
- Data dictionary contains:  
  - Database schema  
  - Integrity constraints (rules to maintain data accuracy)  
  - Primary keys (unique identifiers for records)  
  - Authorization (access control rules)  

# DML (Data Manipulation Language)  

- Used to interact with data (e.g., `SELECT`, `INSERT`, `UPDATE`, `DELETE`).  

# Database Design  

- **Logical design:** Deciding table structures and relationships.  
  - **Business Decision:** What attributes (columns) to store.  
  - **Computer Science Decision:** How to organize tables efficiently.  
- **Approaches:**  
  - **Normalization theory:** Eliminates redundancy by decomposing tables.  
  - **Entity-Relationship (ER) Model:** Diagrams entities (objects) and their relationships.  

# Object-Relational Data Model  

- Extends relational databases to support complex data types (e.g., lists, objects).  
- Maintains SQL compatibility while allowing non-atomic values (e.g., storing arrays in a cell).  

# Query Processing  

1. **Parsing and translation** (Converts SQL to an executable form).  
2. **Optimization** (Finds the most efficient way to execute the query).  
3. **Evaluation** (Runs the query and retrieves results).  

# Transaction Management  

- A **transaction** is a sequence of operations (e.g., transferring money) treated as a single unit.  
- Ensures **ACID properties** (Atomicity, Consistency, Isolation, Durability).  

# XML (Extensible Markup Language)  

- A flexible markup language for data exchange.  
- Supports nested tags and custom structures.  
- Widely used in web services and data interchange.  

# Database Engine  

- Core component that processes queries and manages data.  

# Storage Manager  

- Acts as an intermediary between the database files and application queries.  

# Database Architectures  

- **Centralized:** Single-server system.  
- **Client-Server:** Separates user interfaces from the database.  
- **Parallel:** Uses multiple processors for performance.  
- **Distributed:** Data spread across multiple locations.  
- **Cloud:** Hosted on remote servers (e.g., AWS, Azure).  

# Database Users  

- **Naive User:** Interacts via applications (e.g., ATM users).  
- **Application Programmer:** Writes code to access the database.  
- **Analyst:** Uses query tools for reports.  
- **Database Administrator (DBA):** Manages security, backups, and performance.  

# Relational Model  

- Stores data in tables (like spreadsheets).  
- **Atomic values:** Each cell contains a single, indivisible value.  

# Object-Relational Model  

- Extends relational databases with support for complex data types (e.g., JSON, arrays).  
- Maintains SQL querying while allowing richer data structures.  

---
