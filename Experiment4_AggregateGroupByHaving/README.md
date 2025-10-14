# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
<img width="1063" height="645" alt="image" src="https://github.com/user-attachments/assets/51588d60-8a4e-4130-9e0e-7b5d590c58c4" />

```sql
SELECT InsuranceCompany,count(*) as TotalExpiredPatients
FROM Insurance
GROUP BY InsuranceCompany;
```

**Output:**
<img width="1196" height="800" alt="image" src="https://github.com/user-attachments/assets/93e63f0e-8d94-445c-9bd2-8e37d9a792f0" />

**Question 2**
---
<img width="1058" height="528" alt="image" src="https://github.com/user-attachments/assets/2fc6094d-1e91-444d-bd08-8283bdd5cc89" />

```sql
SELECT DoctorID , count(*) as TotalAppointments
FROM Appointments
GROUP BY DoctorID;
```

**Output:**
<img width="1207" height="688" alt="image" src="https://github.com/user-attachments/assets/ccb03ab5-e910-42c5-946c-1571ad54e3cf" />


**Question 3**
---
<img width="610" height="643" alt="image" src="https://github.com/user-attachments/assets/acff20d8-d030-4c3a-8183-b5fca9922722" />


```sql
SELECT DATE(AppointmentDateTime) AS AppointmentDate ,COUNT(*) AS TotalAppointments
FROM Appointments
GROUP BY AppointmentDate;
```

**Output:**

<img width="1207" height="717" alt="image" src="https://github.com/user-attachments/assets/3847de70-a95c-4bbe-b6b5-1b02dd3238b7" />


**Question 4**
---
<img width="1005" height="492" alt="image" src="https://github.com/user-attachments/assets/0e7e5ef1-cfc6-4450-a2c1-7385667a3819" />

```sql
SELECT COUNT(*) AS COUNT
FROM customer
WHERE city='Noida';
```

**Output:**

<img width="1208" height="372" alt="image" src="https://github.com/user-attachments/assets/344d14bd-e6be-43f0-a208-4d1a3aa59928" />


**Question 5**
---
<img width="750" height="463" alt="image" src="https://github.com/user-attachments/assets/8886f53f-a887-46f5-85fc-11c402cbd8bc" />


```sql
SELECT COUNT(*) as employees_count
FROM employee
where income > 50000;
```

**Output:**

![Output5](output.png)

**Question 6**
---
-- Paste Question 6 here

```sql
-- Paste your SQL code below for Question 6
```

**Output:**

<img width="1205" height="377" alt="image" src="https://github.com/user-attachments/assets/906c05d7-8535-4526-b70f-b633f9838070" />


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
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
