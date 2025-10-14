# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
-- <img width="807" height="241" alt="image" src="https://github.com/user-attachments/assets/9cb542f5-7b6a-419a-a7b0-851ea4e1c9d3" />


```sql
UPDATE products
SET product_name = 'Grapefruit'
WHERE product_id = 4;
```

**Output:**

<img width="1213" height="307" alt="image" src="https://github.com/user-attachments/assets/5612072c-b161-429d-b10a-e7e1c4e04b08" />


**Question 2**
---
--<img width="806" height="510" alt="image" src="https://github.com/user-attachments/assets/da41f5b0-0cbd-426f-9eb6-2b66a6d6016b" />


```sql
UPDATE SALES
SET total_sell_price= quantity * sell_price
WHERE product_id = 10;
```

**Output:**

<img width="1218" height="570" alt="image" src="https://github.com/user-attachments/assets/cf52ecff-b0f7-4a11-ac0d-4ed9b5317e83" />
<img width="1207" height="562" alt="image" src="https://github.com/user-attachments/assets/1ebbe833-bcd0-4d2d-9842-c003cd6e83dd" />



**Question 3**
---
<img width="823" height="558" alt="image" src="https://github.com/user-attachments/assets/975cb2f9-266e-475f-9f0f-7ea8a4abb9b6" />


```sql
UPDATE Products
SET sell_price = sell_price * 1.15
WHERE quantity < 50  AND supplier_id = 10;
```

**Output:**

<img width="1211" height="563" alt="image" src="https://github.com/user-attachments/assets/d8ee8630-874e-444e-ba50-1c090c13bdce" />




**Question 4**
---
--
<img width="786" height="500" alt="image" src="https://github.com/user-attachments/assets/cdbe093e-069c-432c-bc47-4d0deb9ffb3d" />


```sql
DELETE FROM surgeries WHERE surgery_id = 3;
```

**Output:**

<img width="1212" height="456" alt="image" src="https://github.com/user-attachments/assets/e38dfa44-c5c1-4923-8169-1a974e62ddbb" />



**Question 5**
---
<img width="1210" height="620" alt="image" src="https://github.com/user-attachments/assets/918e49d9-3445-4053-b9e9-6990d674190e" />
<img width="1207" height="801" alt="image" src="https://github.com/user-attachments/assets/5c339eae-d403-428d-8057-d1c2dab70143" />


```sql
DELETE FROM Customer WHERE WORKING_AREA = 'New York';
```

**Output:**

<img width="1202" height="792" alt="image" src="https://github.com/user-attachments/assets/37b33ddb-6bbc-4191-905a-3e66efc073be" />
<img width="1190" height="800" alt="image" src="https://github.com/user-attachments/assets/551be26e-fab3-4397-ac7c-e6be6502f08e" />

**Question 6**
---
<img width="1203" height="691" alt="image" src="https://github.com/user-attachments/assets/495fa928-e7c8-458f-beea-c8abf31186fb" />


```sql
DELETE FROM Customer  WHERE GRADE >= 2;
```

**Output:**
<img width="1203" height="691" alt="image" src="https://github.com/user-attachments/assets/daee0702-d18d-4633-99fb-be7abec1bf4c" />

<img width="1210" height="621" alt="image" src="https://github.com/user-attachments/assets/0806075c-cd22-48de-87f8-f51035cb3f9c" />


**Question 7**
---
<img width="1133" height="458" alt="image" src="https://github.com/user-attachments/assets/fa5f1d41-5e9e-45c0-986f-d879a713f3ac" />

```sql
SELECT  * 
FROM salesman
where name LIKE 'N__l%';
```

**Output:**
<img width="1213" height="402" alt="image" src="https://github.com/user-attachments/assets/9fc5b515-e5ba-4272-95de-2b937e8fcc5f" />


**Question 8**
---
<img width="1183" height="637" alt="image" src="https://github.com/user-attachments/assets/6788f44e-2821-499c-ad4f-7976c3ed08cc" />


```sql
SELECT id,
    value2,
    CASE
        WHEN value2 < 10 THEN 'Small'
        WHEN value2 BETWEEN 10 AND 50 THEN 'Medium'
        WHEN value2 > 50 THEN 'Large'
    END AS size_category
FROM calculations;
```

**Output:**
<img width="1206" height="542" alt="image" src="https://github.com/user-attachments/assets/f42fb687-b48e-46e1-86eb-508ad8c8e335" />


**Question 9**
---
<img width="1042" height="662" alt="image" src="https://github.com/user-attachments/assets/88b7ce18-3d28-4a5d-add8-66fe37198361" />

```sql
select NAME , CITY
FROM salesman
where CITY IN ('London', 'Rome');
```

**Output:**
<img width="1220" height="417" alt="image" src="https://github.com/user-attachments/assets/3c34b145-1521-41d1-b9a0-93059f407981" />


**Question 10**
---
<img width="980" height="697" alt="image" src="https://github.com/user-attachments/assets/2c7940b2-b0b3-4137-abf4-7492d0d4b463" />


```sql
SELECT ename,  
       hiredate,
       CASE strftime('%w', hiredate)
            WHEN '0' THEN 'Sunday'
            WHEN '1' THEN 'Monday'
            WHEN '2' THEN 'Tuesday'
            WHEN '3' THEN 'Wednesday'
            WHEN '4' THEN 'Thursday'
            WHEN '5' THEN 'Friday'
            WHEN '6' THEN 'Saturday'
        END AS day_of_week
FROM emp;
```

**Output:**

<img width="1197" height="427" alt="image" src="https://github.com/user-attachments/assets/64243b07-d6e4-4286-a795-e529427adcde" />

##GRADE
<img width="1323" height="67" alt="image" src="https://github.com/user-attachments/assets/07f542e1-21ac-4bc7-b362-923a8582ff45" />


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
