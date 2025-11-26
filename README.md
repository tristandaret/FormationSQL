
# Formation SQL

This repository contains my self-taught SQL learning materials and slides. So far I have created LaTeX/Beamer lecture slides summarizing what I learned about relational databases and SQL. The main slides are in `LectureNotes/NotesSQL.tex`.

**Status:** Drafted notes and slides. Next I plan to build a small project to apply these concepts (simple sample database, queries, and a small Python data-access/analysis script).

**How to view the slides**:
- Build the PDF from the LaTeX source located at `LectureNotes/NotesSQL.tex` (e.g., run `pdflatex NotesSQL.tex` in the `LectureNotes` folder).

**Topics covered so far**

- **Commands Cheatsheet**: overview of common SQL commands and categories (DQL, DML, DDL).
- **Keys & Concepts**: Primary key, Foreign key, and general database key concepts.
- **Integrity Constraints**:
	- Entity integrity (PRIMARY KEY, NOT NULL)
	- Domain constraints (data types, NOT NULL, CHECK, UNIQUE, DEFAULT)
	- Referential integrity (FOREIGN KEY, cascade/SET NULL/RESTRICT behaviors)
- **SQL Statement Categories**: DDL (CREATE, ALTER, DROP, TRUNCATE, RENAME, MODIFY), DML (INSERT, UPDATE, DELETE, SET), DQL (SELECT and associated clauses), DCL (GRANT/REVOKE) and constraint checking modes (IMMEDIATE/DEFERRED where supported).
- **Data Query Language (DQL)**:
	- `SELECT` basics and `SELECT *` caveats
	- `WHERE` with logical operators (`AND`, `OR`, `NOT`)
	- Pattern matching with `LIKE`/wildcards and `ILIKE` (PostgreSQL)
	- Regex matching (`REGEXP`, `~`, `~*`) and performance considerations
	- Range selection with `BETWEEN`
	- Set selection with `IN` and use of subqueries (`NOT IN` caveats and `NOT EXISTS` recommendation)
	- Aggregation basics: `COUNT` and differences between `COUNT(*)` and `COUNT(column)`
	- `DISTINCT` for unique values and combinations
	- Result limiting / pagination: `LIMIT` and `OFFSET` (and `TOP` in some DBs)

- **Data Manipulation Language (DML)**:
	- `INSERT` single & multiple rows
	- `UPDATE` and the `SET` clause (warning about missing `WHERE`)
	- `DELETE` and differences vs `TRUNCATE`

- **Data Definition Language (DDL)**:
	- `CREATE TABLE` and datatype choices
	- `ALTER TABLE` operations: `ADD`, `DROP COLUMN`, `MODIFY`/`ALTER COLUMN`
	- `RENAME` table/column examples
	- `DROP` table/database and safety (`IF EXISTS`)
	- `TRUNCATE` behavior and caveats (fast, non-rollback in many DBs)
	- Column modification across DB engines (MySQL vs PostgreSQL syntax differences)

- **Constraints & Options**:
	- `NOT NULL` usage and rules
	- `PRIMARY KEY`, `FOREIGN KEY`, `UNIQUE`, `CHECK`, `DEFAULT` usage discussed in slides