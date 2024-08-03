# Students-Database-SQL
# Student Database Management System

This repository contains an SQL-based project for a Student Database Management System. The project manages relationships between students, courses, enrollments, and grades. The deliverables include the execution of multiple SQL queries related to the student database management system.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Setup](#setup)
- [Usage](#usage)
- [SQL Queries](#sql-queries)
- [ER Diagram](#er-diagram)
- [Screenshots](#screenshots)

## Features

- Manage relationships between students, courses, enrollments, and grades
- Execution of multiple SQL queries
- Comprehensive project report including ER diagram, constraints, keys, relationships, and metadata

## Technologies Used

- SQL
- Relational Database Management System (RDBMS)


## Setup

1. Clone the repository:

    bash
    git clone (https://github.com/Soumita-2018/Students-Database-SQL).git
    cd Student-Database-SQL
    

2. Ensure that an RDBMS (e.g., MySQL, PostgreSQL) is installed and running on your machine.

3. Create the necessary database and run the SQL scripts in the sql directory in the following order:
    - create_tables.sql
    - insert_data.sql

## Usage

1. Open your preferred SQL client and connect to your database.

2. Execute the queries in the queries.sql file to interact with the student database management system.

## SQL Queries

Some example SQL queries included in the project:

- Display all students enrolled in a particular course:

    
    SELECT s.student_id, s.student_name
    FROM students s
    JOIN enrollments e ON s.student_id = e.student_id
    WHERE e.course_id = 'COURSE_ID';
    

- Calculate the average grade for a course:

    
    SELECT course_id, AVG(grade) AS average_grade
    FROM enrollments
    WHERE course_id = 'COURSE_ID'
    GROUP BY course_id;
    

- Other queries for retrieving and manipulating data related to students, courses, enrollments, and grades.

## ER Diagram

The ER Diagram including constraints, keys, relationships, and metadata is described in the project explanation PDF (Project_Report.pdf) located in the resources directory.

![ER Diagram](resources/ER_Diagram.png)

## Screenshots

### Example Query Execution

![Query Execution](screenshots/query_execution.png)

---

Feel free to contribute to the project by forking the repository and submitting pull requests. For any issues or feature requests, please open an issue in the repository.

---

Happy Querying!
