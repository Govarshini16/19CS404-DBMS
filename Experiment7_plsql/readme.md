# Experiment 7: PL/SQL – Variables, Control Structures and Loops

## AIM
To write and execute simple PL/SQL programs using variables, loops, and conditional statements.


## THEORY

PL/SQL, which stands for Procedural Language extensions to the Structured Query Language (SQL). It is a combination of SQL along with the procedural features of programming languages.

**Syntax:**
```sql
DECLARE 
   <declarations section> 
BEGIN 
   <executable command(s)>
EXCEPTION 
   <exception handling> 
END;
```

### Basic Components of PL/SQL Block:
- DECLARE: Section to declare variables and constants.
- BEGIN: The execution section that contains PL/SQL statements.
- EXCEPTION: Handles errors or exceptions that occur in the program.
- END: Marks the end of the PL/SQL block.

# PL/SQL Programs – Steps and Expected Output

## 1. Write a PL/SQL program to find the Greatest of Two Numbers

### Steps:
- Declare two numeric variables and initialize them.
- Use an `IF` statement to compare the values.
- Display the greater number using `DBMS_OUTPUT.PUT_LINE`.

  
**Code:

```
DECLARE
   num1 NUMBER := 25;
   num2 NUMBER := 80;
   greatest NUMBER;
BEGIN
   IF num1 > num2 THEN
      greatest := num1;
   ELSE
      greatest := num2;
   END IF;

   DBMS_OUTPUT.PUT_LINE('The greatest number is: ' || greatest);
END;
```

**Expected Output:**  
Greater number is: 80

**Output
<img width="925" height="92" alt="image" src="https://github.com/user-attachments/assets/b5c62edc-cdb0-48ba-aa15-da1273992013" />


---

## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

### Steps:
- Declare a variable `n` and assign a value (e.g., 10).
- Initialize a `sum` variable to 0.
- Use a `WHILE` loop to iterate from 1 to `n`, adding each number to the sum.
- Display the result using `DBMS_OUTPUT.PUT_LINE`.


*CODE
```
DECLARE
   n NUMBER := 10;       
   sum NUMBER := 0;
   i   NUMBER := 1;
BEGIN
   WHILE i <= n LOOP
      sum := sum + i;
      i := i + 1;
   END LOOP;

   DBMS_OUTPUT.PUT_LINE('Sum of first ' || n || ' natural numbers is: ' || sum);
END;
```
**Expected Output:**  
Sum of first 10 natural numbers is: 55

**OUTPUT
<img width="907" height="83" alt="image" src="https://github.com/user-attachments/assets/6691a1de-0aa8-4162-89fe-24a68cce8dd2" />


---

## 3. Write a PL/SQL program to generate Fibonacci series

### Steps:
- Declare the variable `n` to indicate how many terms to generate.
- Initialize the first two Fibonacci numbers (0 and 1).
- Use a loop to generate the next terms using the formula `c = a + b`.
- Print each term in the series.


**CODE

```
DECLARE
    n NUMBER := 7; -- number of terms to generate
    a NUMBER := 0;
    b NUMBER := 1;
    c NUMBER;
    i NUMBER := 1;
BEGIN
    DBMS_OUTPUT.PUT_LINE('Fibonacci sequence:');
    WHILE i <= n LOOP
        IF i = 1 THEN
            DBMS_OUTPUT.PUT(a);
        ELSIF i = 2 THEN
            DBMS_OUTPUT.PUT(', ' || b);
        ELSE
            c := a + b;
            DBMS_OUTPUT.PUT(', ' || c);
            a := b;
            b := c;
        END IF;
        i := i + 1;
    END LOOP;
    DBMS_OUTPUT.NEW_LINE;
END;
```


**Expected Output:**  
n = 7  
Fibonacci sequence: 0, 1, 1, 2, 3, 5, 8

**OUTPUT

<img width="907" height="280" alt="Screenshot 2025-11-12 111425" src="https://github.com/user-attachments/assets/5f9f27ba-8501-44e3-8aae-acba6c13fc1b" />


---

## 4. Write a PL/SQL Program to display the number in Reverse Order

### Steps:
- Declare a variable `n` and assign a value (e.g., 1535).
- Use a loop to extract each digit using modulo and reverse the number.
- Display the reversed number.

**CODE
```
DECLARE
   n NUMBER := 1535;         
   reversed NUMBER := 0;
   remainder NUMBER;
   original NUMBER := 1535;  
BEGIN
   WHILE n > 0 LOOP
      remainder := MOD(n, 10);           
      reversed := (reversed * 10) + remainder;  
      n := TRUNC(n / 10);                 
   END LOOP;

   DBMS_OUTPUT.PUT_LINE('n = ' || original);
   DBMS_OUTPUT.PUT_LINE('Reversed number is ' || reversed);
END;
```


**Expected Output:**  
n = 1535  
Reversed number is 5351

**OUTPUT
<img width="882" height="312" alt="image" src="https://github.com/user-attachments/assets/1cd8db66-7e6d-4782-b71d-203fb33e232e" />

---

## 5. Write a PL/SQL program to find the largest of three numbers

### Steps:
- Declare three numeric variables `a`, `b`, and `c`.
- Use nested `IF-ELSIF-ELSE` conditions to find the largest among the three.
- Display the largest number.

*CODE
```
DECLARE
   a NUMBER := 10;
   b NUMBER := 9;
   c NUMBER := 15;
   largest NUMBER;
BEGIN
   IF (a >= b) AND (a >= c) THEN
      largest := a;
   ELSIF (b >= a) AND (b >= c) THEN
      largest := b;
   ELSE
      largest := c;
   END IF;

   DBMS_OUTPUT.PUT_LINE('a = ' || a || ', b = ' || b || ', c = ' || c);
   DBMS_OUTPUT.PUT_LINE('Largest of three numbers is ' || largest);
END;
```

**Expected Output:**  
a = 10, b = 9, c = 15  
Largest of three number is 15

**OUTPUT

<img width="915" height="82" alt="image" src="https://github.com/user-attachments/assets/f5396c66-535f-41f5-a8fd-4467f9f36557" />


## RESULT
Thus, the PL/SQL programs using variables, conditionals, and loops were executed successfully.



