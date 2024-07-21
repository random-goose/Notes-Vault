# Normalization
DB Normalization is a process in DB Design that organizes tables of minimize redundancy and dependency.
The main goal is to ensure that data is logically stored to reduce the chance of data anomalies.
Goals:
1. **Eliminate Redundant Data**: Redundant data can lead to inconsistencies, normalization ensures that data is stored in only one place.
2. **Organize Data Efficiently**: It ensures that the database structure allows for efficient data retrieval and updates
3. **Ensure Data Dependencies**: This process ensures that only related data is stored in a table, which reduces the complexity of DB relationships.

## Normal Forms
The normalization process is typically divided into several normal forms, each with its own set of rules:

- **1NF: Atomicity** - Ensures that each column in a table contains atomic values, each column contains values of a single time.
- **2NF: Partial Dependency** - Builds on 1NF by removing subsets of data that applies to multiple rows and placing them in separate tables. This step eliminates partial dependencies.
- **3NF: Transitive Dependency** - Builds on 2NF by ensuring that non-key columns are not dependent on other non-key columns.
- **BCNF - Every determinant is candidate key**
- **4NF - Multi-values dependency**
- **5NF - Joint dependency**

## 1NF
Table should not contain any duplicate values - one cell: one value

| StudentID | StudentName | Courses          |
| --------- | ----------- | ---------------- |
| 1         | Alice       | Math, Science    |
| 2         | Bob         | English, History |

| StudentID | StudentName | Course  |
| --------- | ----------- | ------- |
| 1         | Alice       | Math    |
| 1         | Alice       | Science |
| 2         | Bob         | English |
| 2         | Bob         | History |

# 2NF
|StudentID|StudentName|Course|Instructor|
|---|---|---|---|
|1|Alice|Math|Dr. Smith|
|1|Alice|Science|Dr. Taylor|
|2|Bob|English|Dr. Jones|
|2|Bob|History|Dr. Brown|

**2NF Tables:**
**Table: Student**

| StudentID | StudentName |
| --------- | ----------- |
| 1         | Alice       |
| 2         | Bob         |
**Table: Course**

| CourseID | Course  | Instructor |
| -------- | ------- | ---------- |
| 1        | Math    | Dr. Smith  |
| 2        | English | Dr. Jones  |
| 3        | Science | Dr. Taylor |
| 4        | History | Dr. Brown  |
**Table: Enrollment**

| StudentID | CourseID |
| --------- | -------- |
| 1         | 1        |
| 1         | 3        |
| 2         | 2        |
| 2         | 4        |
