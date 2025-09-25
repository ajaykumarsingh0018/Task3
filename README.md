# Task3
📘 README
🎯 Project Objective

The objective of this project is to learn how to extract data from one or more tables using SQL queries.
You will practice with DB Browser for SQLite or MySQL Workbench.

🛠 Tools Used

DB Browser for SQLite (works with .db files)

MySQL Workbench (for MySQL databases)

📂 Database Structure
1. Database

CollegeDB

2. Tables

Students

student_id (INT, Primary Key, Auto Increment)

first_name (VARCHAR)

last_name (VARCHAR)

email (VARCHAR, Unique)

enrollment_date (DATE)

Courses

course_id (INT, Primary Key, Auto Increment)

course_name (VARCHAR)

credits (INT)

student_id (INT, Foreign Key → Students.student_id)

📜 SQL Script Flow

Create Database

CREATE DATABASE CollegeDB;
USE CollegeDB;


Create Tables

CREATE TABLE Students (...);
CREATE TABLE Courses (...);


Insert Sample Data

INSERT INTO Students (...);
INSERT INTO Courses (...);


Run Queries

SELECT * and specific columns

WHERE, AND, OR, LIKE, BETWEEN

ORDER BY

LIMIT

JOIN

🔍 Example Queries

Get all students:

SELECT * FROM Students;


Students with Gmail IDs:

SELECT * FROM Students WHERE email LIKE '%@gmail.com';


Top 3 newest students:

SELECT * FROM Students ORDER BY enrollment_date DESC LIMIT 3;


Students with their courses:

SELECT s.first_name, s.last_name, c.course_name
FROM Students s
JOIN Courses c ON s.student_id = c.student_id;

✅ Outcome

By completing this project, you will:

Understand how to retrieve data from databases

Learn filtering using conditions (WHERE, AND, OR, LIKE, BETWEEN)

Practice sorting and limiting results

Perform joins across multiple tables
