# Sports Equipment Rental System – Relational Database Design

A relational database project developed for the Database Systems coursework. The project models the end-to-end operations of a multi-branch sports equipment rental business, covering conceptual design, schema normalization, integrity constraints, and query optimization using Oracle SQL.

## Features & Implementation

- **Relational Schema Design:** Designed an Entity-Relationship (ER) model and conceptual diagrams spanning 10 tables, normalized to Third Normal Form (3NF) to eliminate redundancy.
- **Complex Relationships:** Implemented a ternary associative relationship (`detalii`) linking contracts, equipment, and staff members, alongside recursive hierarchies for product categories and subcategories.
- **Data Integrity:** Enforced referential integrity via primary and foreign key constraints, unique email constraints, and validation rules (`CHECK` constraints for prices and discount rates).
- **Advanced SQL Queries:** Wrote complex data retrieval queries featuring correlated subqueries (`WHERE NOT EXISTS`), multi-table `LEFT OUTER JOIN` chains, and CTEs (`WITH` clauses).
- **Views & Query Optimization:** Implemented updatable SQL views (`V_VALOARE_INCHIRIERE`) for calculating rental costs, and optimized execution by filtering datasets early before expensive join operations.

## Tech Stack

- **RDBMS:** Oracle Database
- **Language:** Oracle SQL (DDL, DML, DQL)
- **Modeling:** Entity-Relationship Diagrams (ERD), Conceptual Data Diagrams

## Database Entities

- `client` – Customer personal details and contact info
- `angajat` – Staff members and their functional roles
- `locatie` – Physical rental centers and branches
- `categorie` – Equipment categories supporting parent-child hierarchy
- `echipament` – Sports gear inventory items linked to locations and categories
- `fisa_tehnica` – Inspection history and maintenance state
- `inchiriere` – Rental transactions handling pickup, return, and discounts
- `detalii` – Ternary associative table mapping rented items to verifying employees
- `reducere` – Promotional campaigns and discount percentages
- `plata` – Payment transaction tracking per rental contract
