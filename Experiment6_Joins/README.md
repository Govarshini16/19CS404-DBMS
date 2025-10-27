# Experiment 6: Joins

## AIM
To study and implement different types of joins.

## THEORY

SQL Joins are used to combine records from two or more tables based on a related column.

### 1. INNER JOIN
Returns records with matching values in both tables.

**Syntax:**
```sql
SELECT columns
FROM table1
INNER JOIN table2
ON table1.column = table2.column;
```

### 2. LEFT JOIN
Returns all records from the left table, and matched records from the right.

**Syntax:**

```sql
SELECT columns
FROM table1
LEFT JOIN table2
ON table1.column = table2.column;
```
### 3. RIGHT JOIN
Returns all records from the right table, and matched records from the left.

**Syntax:**

```sql
SELECT columns
FROM table1
RIGHT JOIN table2
ON table1.column = table2.column;
```
### 4. FULL OUTER JOIN
Returns all records when there is a match in either left or right table.

**Syntax:**

```sql
SELECT columns
FROM table1
FULL OUTER JOIN table2
ON table1.column = table2.column;
```

**Question 1**
--
<img width="1282" height="837" alt="image" src="https://github.com/user-attachments/assets/06ac49df-8b67-484e-afce-f99933e4a530" />


```sql
select c.cust_name,c.city,c.grade,s.name as Salesman,s.city
from customer c
join salesman s on c.salesman_id = s.salesman_id
where grade < 300
order by c.customer_id asc;
```

**Output:**

<img width="1313" height="662" alt="image" src="https://github.com/user-attachments/assets/47252d3e-1176-4f44-a1ba-1f85a277519e" />

**Question 2**
---
<img width="857" height="457" alt="image" src="https://github.com/user-attachments/assets/137e5440-7e21-4c45-baf7-39e9cec151b2" />


```sql
select c.cust_name,c.city ,o.ord_no,o.ord_date,o.purch_amt
from orders o
left join customer c on o.customer_id = c.customer_id
where c.city = 'London';
```

**Output:**

<img width="1307" height="430" alt="image" src="https://github.com/user-attachments/assets/48efe954-bea0-41e9-9e29-3eefc3f47a17" />


**Question 3**
---
<img width="925" height="793" alt="image" src="https://github.com/user-attachments/assets/8934a7d9-2849-47f0-a5cc-cb3fe3ceb317" />


```sql
select s.name as Salesman , c.cust_name, c.city
from salesman s
join customer c on c.city=s.city;
```

**Output:**

<img width="1248" height="747" alt="image" src="https://github.com/user-attachments/assets/23c6df25-889c-43ed-b3ba-d964a843c613" />


**Question 4**
---
<img width="886" height="817" alt="image" src="https://github.com/user-attachments/assets/ca45b525-fe3c-4ba1-a1ca-09d8c53083f4" />

```sql
select p.first_name as patient_name , d.first_name as doctor_name
from doctors d
inner join patients p on d.doctor_id=p.doctor_id
where p.discharge_date not null;
```

**Output:**

<img width="883" height="465" alt="image" src="https://github.com/user-attachments/assets/a61b3e7c-718c-4289-b004-a7d2d96dbe3f" />


**Question 5**
---
-- Paste Question 5 here

```sql
-- Paste your SQL code below for Question 5
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
Thus, the SQL queries to implement different types of joins have been executed successfully.
