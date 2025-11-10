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
<img width="1200" height="758" alt="image" src="https://github.com/user-attachments/assets/1e2ab07c-af8b-4ccd-b3d9-45e4f71168fd" />

<img width="1026" height="732" alt="image" src="https://github.com/user-attachments/assets/2d71d607-ef65-41e0-acfc-f046b84d3234" />



```sql
select c.cust_name,c.city,o.ord_no,o.ord_date,o.purch_amt as "Order Amount" ,  s.name, s.commission
from customer c
left join orders o on c.customer_id = o.customer_id
left join salesman s on s.salesman_id = c.salesman_id;
```

**Output:**
<img width="1263" height="796" alt="image" src="https://github.com/user-attachments/assets/59358d05-4307-42ad-a8c7-f56b85fa60d2" />

<img width="1275" height="803" alt="image" src="https://github.com/user-attachments/assets/0dfc7d3b-1ab6-4f80-9d6d-54bf79f2b5dd" />

<img width="1260" height="555" alt="image" src="https://github.com/user-attachments/assets/d3cdcbbb-752d-433d-aa81-0df4b490503d" />


**Question 6**
---
<img width="1276" height="768" alt="image" src="https://github.com/user-attachments/assets/23e802a4-998e-4100-b133-51c620e41be2" />


```sql
select c.cust_name , c.city, c.grade, s.name as Salesman, s.city
from customer c
join salesman s on c.salesman_id = s.salesman_id
order by c.customer_id asc;
```

**Output:**

<img width="1321" height="788" alt="image" src="https://github.com/user-attachments/assets/a7f046df-8095-4b63-8d8e-f855f82c2b4e" />


**Question 7**
---
<img width="1243" height="662" alt="image" src="https://github.com/user-attachments/assets/664c7a47-beaa-45e9-9dcc-633321e9f3ca" />
<img width="907" height="660" alt="image" src="https://github.com/user-attachments/assets/08e0600c-924b-453a-b0a6-5980375a1db3" />

-- 


```sql
select o.ord_no ,o.ord_date,o.purch_amt,c.cust_name as "Customer Name" ,c.grade,s.name as Salesman,s.commission
from orders o
left join customer c on o.customer_id = c.customer_id
left join salesman s on o.salesman_id = s.salesman_id;
```

**Output:**

<img width="1335" height="821" alt="image" src="https://github.com/user-attachments/assets/2d77cdff-5e28-4628-9fe2-12ccbdb67508" />


**Question 8**
---
<img width="1185" height="657" alt="image" src="https://github.com/user-attachments/assets/b98633c1-81b2-4061-a8ef-4c86dee9a4d1" />


```sql
select p.first_name as patient_name , t.test_name
from patients p
inner join test_results t on p.patient_id = t.patient_id;
```

**Output:**

<img width="1281" height="558" alt="image" src="https://github.com/user-attachments/assets/03eeb79b-40cd-48ae-ba47-a83f044e0e98" />


**Question 9**
---
<img width="1261" height="316" alt="image" src="https://github.com/user-attachments/assets/c1673289-8c5d-4bbd-ab18-3b60c911cc9d" />


```sql
select s.*
from salesman s 
left join customer c on s.salesman_id=c.salesman_id
where cust_name = 'Fabian Johns';
```

**Output:**
<img width="1283" height="427" alt="image" src="https://github.com/user-attachments/assets/ab51e7a6-6c52-4e6d-9885-a03814a112f7" />


**Question 10**
---
<img width="1257" height="666" alt="image" src="https://github.com/user-attachments/assets/ce4f487d-4886-4e1a-9fc8-df559e122a87" />


```sql
select p.first_name as patient_name  ,d.first_name  as doctor_name
from patients p
inner join doctors d on p.doctor_id = d.doctor_id
where p.discharge_date is null;
```

**Output:**

<img width="1282" height="482" alt="image" src="https://github.com/user-attachments/assets/7917efca-f9b6-4f51-8c67-5b19d548fb83" />


##GRADE
<img width="1280" height="60" alt="image" src="https://github.com/user-attachments/assets/ca0b6217-15c3-4a86-aa9d-720b6cd60c3c" />



## RESULT
Thus, the SQL queries to implement different types of joins have been executed successfully.
