# Experiment 5: Subqueries and Views

## AIM
To study and implement subqueries and views.

## THEORY 

### Subqueries
A subquery is a query inside another SQL query and is embedded in:
- WHERE clause
- HAVING clause
- FROM clause

**Types:**
- **Single-row subquery**:
  Sub queries can also return more than one value. Such results should be made use along with the operators in and any.
- **Multiple-row subquery**:
  Here more than one subquery is used. These multiple sub queries are combined by means of ‘and’ & ‘or’ keywords.
- **Correlated subquery**:
  A subquery is evaluated once for the entire parent statement whereas a correlated Sub query is evaluated once per row processed by the parent statement.

**Example:**
```sql
SELECT * FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```
### Views
A view is a virtual table based on the result of an SQL SELECT query.
**Create View:**
```sql
CREATE VIEW view_name AS
SELECT column1, column2 FROM table_name WHERE condition;
```
**Drop View:**
```sql
DROP VIEW view_name;
```

**Question 1**
--
<img width="1046" height="727" alt="image" src="https://github.com/user-attachments/assets/63746f72-c993-4719-8ee7-f545769544eb" />


```sql
select c.customer_id , c.cust_name,c.city,c.grade,c.salesman_id
from customer c
JOIN salesman s ON c.customer_id=(s.salesman_id-2001) and s.name ='Mc Lyon';
```

**Output:**

<img width="1257" height="405" alt="image" src="https://github.com/user-attachments/assets/a8c60f35-e75d-4aae-a0ba-adc1687cc7c1" />


**Question 2**
---
<img width="827" height="552" alt="image" src="https://github.com/user-attachments/assets/2737fad8-3864-4b86-9465-d439cc8bf001" />

```sql
select name,city
from customer 
where city IN (
    SELECT city
    FROM customer
    where id in (3,7)
);
```

**Output:**

<img width="868" height="518" alt="image" src="https://github.com/user-attachments/assets/5a8ece64-ed77-4b75-a95c-ea9e6e62b785" />


**Question 3**
---
<img width="856" height="748" alt="image" src="https://github.com/user-attachments/assets/1e5df6f8-22d9-4169-9da9-aae04c4cfcb0" />


```sql
select o.ord_no, o.purch_amt, o.ord_date, o.customer_id ,o.salesman_id
from orders o
JOIN salesman s ON o.salesman_id = s.salesman_id
where s.name = 'Paul Adam';

```

**Output:**
<img width="1261" height="461" alt="image" src="https://github.com/user-attachments/assets/2d2ff755-6e13-4bba-aee3-d4f6c3928eb7" />


**Question 4**
---
<img width="860" height="637" alt="image" src="https://github.com/user-attachments/assets/d30ce395-c901-4ba6-a663-13bc3ab3a721" />

```sql
select *
from Employee
where age < (
        select AVG(age)
        from Employee
        where income > 1000000
);
```

**Output:**

<img width="1262" height="507" alt="image" src="https://github.com/user-attachments/assets/cb478640-7f42-4091-970c-da35bc0af766" />


**Question 5**
---
<img width="856" height="658" alt="image" src="https://github.com/user-attachments/assets/c397cb13-62d0-4098-9b9d-286ccf565337" />


```sql
select g.student_id, g.student_name, g.subject, g.grade
from grades g
where grade = (
    select MAX(grade)
    from grades
    where g.subject=subject
);
```

**Output:**
<img width="1261" height="527" alt="image" src="https://github.com/user-attachments/assets/b5eb78f8-2486-4b94-a18c-252bbfd8fe7c" />

**Question 6**
---
<img width="856" height="577" alt="image" src="https://github.com/user-attachments/assets/240360dd-6e34-4ab4-8075-71b6f34bb53a" />

```sql
select name
from customer
where phone IN (
    select phone
    from customer
    group by phone
    having count(*)=1
);
```

**Output:**

<img width="905" height="520" alt="image" src="https://github.com/user-attachments/assets/55ef12f6-855f-4bf4-ac0d-78a47e9e1f73" />


**Question 7**
---
<img width="823" height="805" alt="image" src="https://github.com/user-attachments/assets/2e047df3-f6ff-47a2-8cd2-e11b066d94d8" />


```sql
select o.ord_no, o.purch_amt, o.ord_date, o.customer_id ,o.salesman_id
from orders o
JOIN salesman s ON o.salesman_id = s.salesman_id
where s.city = 'New York';
```

**Output:**
<img width="1252" height="563" alt="image" src="https://github.com/user-attachments/assets/421f236a-c6c3-4194-85f9-3d89d9a39d00" />



**Question 8**
---
<img width="1151" height="680" alt="image" src="https://github.com/user-attachments/assets/eb9f159a-7aec-44aa-9fb0-00f3cfbb2466" />


```sql
select *
from CUSTOMERS
WHERE ADDRESS = 'Delhi' AND AGE < '30'
ORDER BY ID ASC;
```

**Output:**

<img width="1258" height="433" alt="image" src="https://github.com/user-attachments/assets/8a657bdf-32ed-41bf-95ef-bf33168ebb0e" />

**Question 9**
---
<img width="866" height="763" alt="image" src="https://github.com/user-attachments/assets/51ec0495-1246-4ccf-8718-5e875a5a6b64" />


```sql
SELECT *
FROM CUSTOMERS
WHERE SALARY > 1500;
```

**Output:**

<img width="1258" height="666" alt="image" src="https://github.com/user-attachments/assets/6d34dea2-5926-463a-9728-1ef185094f58" />


**Question 10**
---
<img width="912" height="512" alt="image" src="https://github.com/user-attachments/assets/836cf92d-0cf3-4e7e-b595-caf24ea6485a" />


```sql
select medication_id as medic, medication_name, dosage
from Medications
WHERE dosage = (
        select MAX(dosage)
        from Medications
);
```

**Output:**
<img width="878" height="470" alt="image" src="https://github.com/user-attachments/assets/de8fdb5c-e029-494f-9b17-4fdaa8625306" />


## GRADE
<img width="1127" height="71" alt="image" src="https://github.com/user-attachments/assets/2d1650ee-bf17-4f39-9d98-3ba24ad5a435" />


## RESULT
Thus, the SQL queries to implement subqueries and views have been executed successfully.
