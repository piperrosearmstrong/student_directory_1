# Students Table Design Recipe 

## 1. Extract nouns from the user stories or specification

As a coach
So I can get to know all students
I want to see a list of students' names.

As a coach
So I can get to know all students
I want to see a list of students' cohorts.

Nouns:

name, cohort

## 2. Infer the Table Name and Columns

| Record                | Properties          |
| --------------------- | ------------------  |
| student               | name, cohort

Name of the table (always plural): `students` 

Column names: `pupil_name`, `cohort`

## 3. Decide the column types.

id: SERIAL
pupil_name: text
cohort: text

## 4. Write the SQL.

CREATE TABLE students (
  id SERIAL PRIMARY KEY,
  pupil_name text,
  cohort text
);

## 5. Create the table.

psql -h 127.0.0.1 database_name < albums_table.sql

