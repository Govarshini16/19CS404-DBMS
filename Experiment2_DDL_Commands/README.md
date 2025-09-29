# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**
--
--<img width="1033" height="367" alt="image" src="https://github.com/user-attachments/assets/00851fb2-d38b-476a-a516-d1bd3c7053f6" />


```sql
INSERT INTO Products (Name,Category,Price, Stock)
VALUES
('Smartphone',  'Electronics',  800,150),
('Headphones','Accessories' , 200,300);
```

**Output:**

<img width="1201" height="417" alt="image" src="https://github.com/user-attachments/assets/b5a90d04-5b19-478b-a8e0-14fd4553ad16" />
<img width="1206" height="406" alt="image" src="https://github.com/user-attachments/assets/45cd28d9-236a-47cb-8e92-78915105212b" />


**Question 2**
---
-- <img width="1182" height="268" alt="image" src="https://github.com/user-attachments/assets/c45aa240-981b-415c-9f8d-0a7c045cdd05" />


```sql
INSERT INTO Books(ISBN ,Title,Author,Publisher, Year)
VALUES('978-1234567890',  'Data Science Essentials',  'Jane Doe','TechBooks',2024);
```

**Output:**
<img width="1216" height="310" alt="image" src="https://github.com/user-attachments/assets/a006a753-fca0-4f6a-9865-4169973af04f" />
<img width="1203" height="310" alt="image" src="https://github.com/user-attachments/assets/01d1b6da-1b06-4481-81c9-841a9092f55b" />


**Question 3**
---<img width="1041" height="587" alt="image" src="https://github.com/user-attachments/assets/de19a6f5-236b-44ec-a969-595bdabd2bdc" />

--
```sql
ALTER TABLE Student_detailS ADD COLUMN  Mobilenumber number;
```

**Output:**
<img width="1208" height="420" alt="image" src="https://github.com/user-attachments/assets/72735fe7-a3bf-447c-8286-c8b85af17d82" />

<img width="1203" height="433" alt="image" src="https://github.com/user-attachments/assets/7825e8bf-dd5a-4073-b392-b31cead5597e" />


**Question 4**
---
-- <img width="1202" height="352" alt="image" src="https://github.com/user-attachments/assets/b4a917da-260a-4553-a69d-8a5ee7959255" />


```sql
create table Attendance (
AttendanceID  INTEGER  primary key,
EmployeeID INTEGER,
AttendanceDate  DATE,
Status  TEXT check(status in('Present', 'Absent', 'Leave')),
foreign key (EmployeeID) references Employees(EmployeeID)
);
```

**Output:**

<img width="1198" height="363" alt="image" src="https://github.com/user-attachments/assets/13a3812b-a302-4330-8c78-23f8971ffb07" />
<img width="1210" height="347" alt="image" src="https://github.com/user-attachments/assets/9552b7f8-73cb-42eb-92ae-ab89520c8de3" />



**Question 5**
---
<img width="1176" height="338" alt="image" src="https://github.com/user-attachments/assets/172590c2-0185-41ee-92b0-f5cf592bb69c" />

```sql
alter table employee ADD COLUMN first_name varchar(50);
alter table employee ADD COLUMN last_name varchar(50);
```

**Output:**
<img width="1200" height="391" alt="image" src="https://github.com/user-attachments/assets/b4309e7b-42d1-43d9-8ac4-656a0f77d2ab" />
<img width="1200" height="372" alt="image" src="https://github.com/user-attachments/assets/0512412d-67f5-4200-977f-a2dccc90a8cb" />


**Question 6**
---
-- Paste Question 6 here

```sql
-- Paste your SQL code below for Question 6
```

**Output:**

![Output6](output.png)

**Question 7**
---
-- Paste Question 7 here

```sql
-- Paste your SQL code below for Question 7
```

**Output:**

![Output7](output.png)

**Question 8**
---
-- Paste Question 8 here

```sql
-- Paste your SQL code below for Question 8
```

**Output:**

![Output8](output.png)

**Question 9**
---
-- Paste Question 9 here

```sql
-- Paste your SQL code below for Question 9
```

**Output:**

![Output9](output.png)

**Question 10**
---
-- Paste Question 10 here

```sql
-- Paste your SQL code below for Question 10
```

**Output:**

![Output10](output.png)


## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
