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

<img width="1205" height="377" alt="image" src="https://github.com/user-attachments/assets/906c05d7-8535-4526-b70f-b633f9838070" />


**Question 6**
---
<img width="587" height="482" alt="image" src="https://github.com/user-attachments/assets/901010fb-5817-40b1-856e-74f41d8a8bc2" />


```sql
SELECT MAX(purch_amt) AS MAXIMUM
FROM orders;
```

**Output:**
<img width="842" height="365" alt="image" src="https://github.com/user-attachments/assets/f389d01d-4453-47a9-b1e0-ee76e0647f86" />


**Question 7**
---
<img width="746" height="535" alt="image" src="https://github.com/user-attachments/assets/0c29ffe8-67d1-4448-8b1f-df107be52f80" />


```sql
SELECT name as fruit_name, MIN(inventory) AS lowest_quantity
FROM fruits;
```

**Output:**

<img width="848" height="365" alt="image" src="https://github.com/user-attachments/assets/dcf7e145-fecf-4680-9715-4cb6a73dc557" />


**Question 8**
---

```sql
SELECT age,MAX(income)
FROM employee
GROUP BY age
HAVING income>2000000;
```

**Output:**

<img width="841" height="422" alt="image" src="https://github.com/user-attachments/assets/8f846514-212c-4fad-adce-0bd83e1c5220" />


**Question 9**
---
<img width="848" height="530" alt="image" src="https://github.com/user-attachments/assets/2397ef2b-d255-4545-873c-47334fccbdad" />


```sql
SELECT jdate,MIN(workhour)
FROM employee1
GROUP BY jdate
HAVING MIN(workhour)<10;
```

**Output:**

<img width="836" height="496" alt="image" src="https://github.com/user-attachments/assets/f54441dd-4364-407a-8100-8d8ba73e6a55" />


**Question 10**
---
<img width="842" height="532" alt="image" src="https://github.com/user-attachments/assets/a22b37ad-d102-4c5d-9887-9000f0bd0819" />

```sql
SELECT jdate, MAX(workhour)
FROM employee1
GROUP BY jdate
HAVING MAX(workhour)>12;
```

**Output:**

<img width="840" height="447" alt="image" src="https://github.com/user-attachments/assets/a64fc0f0-949b-459c-8780-08ee8ad347ca" />

## GRADE
<img width="1322" height="57" alt="image" src="https://github.com/user-attachments/assets/b19b1bbf-bff8-495f-99f3-fe2498a4c113" />


## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
