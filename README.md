# Database-Management-SQL-fictional-shipping-business
## Royal Anchor Shipping Database Design
This repository contains the design and implementation of a relational database system for the fictional business: Royal Anchor Shipping (RAC). The database supports global shipping operations, cargo tracking, container booking, crew assignments, and scheduling. The design has been executed based on a detailed Entity Relationship Diagram (ERD) and is backed by SQL queries that reflect business rules, operational constraints, and multiplicity relationships.

Contents
1. Entity-Relationship Diagram (ERD)
The ERD outlines the core entities and relationships within the RAC system, including vessels, containers, crew, bookings, cargo types, ports, and employees.

Entities include:

Port, Vessel, Container, Crew, Booking, Schedule, Route, Cargo Type, and Customer.

Attributes for each entity are clearly defined with primary and foreign keys (e.g., Port ID, Vessel IMO Number, Crew ID).

Multiplicity Constraints:

Relationships such as "one-to-many" (Vessel to Crew, Booking to Cargo) and "many-to-one" (Booking to Container) are defined.

2. SQL Table Definitions
SQL code is provided to implement the tables for the RAC database, following the design specifications from the ERD.

Tables include constraints like primary keys (PK) and foreign keys (FK) to enforce referential integrity.

3. Data Validation and Multiplicity
Data entries have been validated using SQL queries to ensure they follow the business rules defined by the ERD.

A Multiplicity Summary is provided to demonstrate the relationships and confirm data integrity, including:

Vessel to Crew (1 → *)

Booking to Cargo (1 → *)

ContainerType to Container (1 → *)

Booking to Container (* → 1)

Vessel to Schedule (1 → *)

Schedule to Port (1 → *)

Customer to Booking (1 → *)

4. SQL Queries
A set of SQL queries to retrieve data from the RAC database, including:

List All Crew Members on a Vessel: Retrieves crew details, roles, and departments.

Show Customers Who Made Multiple Bookings: Identifies frequent customers and their booking patterns.

Validate One-to-One Booking-to-Container Pairing: Ensures each booking is linked to a single container.

Find Container Types Used Multiple Times: Identifies container types frequently used and displays their specifications.

Detailed Booking View Including Vessel, Route, and Crew Assigned: Provides a comprehensive view of each booking's logistics.

Employee Overview with Role Categorisation and Vessel Assignment: Lists employees, their roles, and assigned vessels.

5. Database Setup and Usage
To replicate the database:

SQL Table Definitions: Use the provided SQL scripts to create tables and relationships.

Test Data: Insert sample data into the tables to test relationships and constraints.

Queries: Use the provided queries to fetch and validate data according to business rules.

Prerequisites: Ensure you have access to an SQL database (e.g., MySQL, PostgreSQL, SQLite) for running the provided scripts.

6. Evaluation and Lessons Learned
The project successfully models the operations of Royal Anchor Shipping, ensuring that data integrity and constraints are maintained through the use of relational design.

Challenges encountered include handling constraint violations and clarifying relationships between certain tables.

Future Improvements:

Test data insertion in smaller chunks to avoid constraint violations.

Standardise naming conventions for easier querying and data retrieval.

Implement auto-generation of keys and sequences for smoother data entry.

Installation
To set up the RAC database on your system:

Install SQL Database: Make sure you have a database engine like MySQL, PostgreSQL, or SQLite installed.

Run SQL Scripts: Use the provided SQL table definition scripts to create the database and tables.

Insert Data: Insert sample test data using the SQL INSERT queries.

Run Queries: Execute the provided SQL queries to validate the relationships and data integrity.

Dependencies
SQL Database (MySQL, PostgreSQL, or SQLite): The database engine required to run the provided SQL scripts.

SQL Client: Any SQL client tool (e.g., MySQL Workbench, pgAdmin, DBeaver) can be used to run the queries.

Conclusion
This project successfully models the logistics, booking, crew, and cargo management for the Royal Anchor Shipping system. The relational database design follows sound principles of data integrity, referential constraints, and operational needs, ensuring a robust foundation for shipping operations.
