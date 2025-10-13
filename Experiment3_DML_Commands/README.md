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
![Uploading image.png…]()



**Question 4**
---
-- Paste Question 4 here

```sql
-- Paste your SQL code below for Question 4
```

**Output:**

![Output4](output.png)

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
Thus, the SQL queries to implement DML commands have been executed successfully.
