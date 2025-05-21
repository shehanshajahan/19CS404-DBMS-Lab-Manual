# Experiment 3: DML Commands

### Name : Shehan Shajahan
### Register Number : 212223240154
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
Decrease the reorder level by 30 percent where the product name contains 'cream' and quantity in stock is higher than reorder level in the products table.
PRODUCTS TABLE

```sql
UPDATE PRODUCTS SET
reorder_lvl=reorder_lvl*0.7
WHERE product_name LIKE '%cream%' AND quantity>reorder_lvl;
```

**Output:**

![image](https://github.com/user-attachments/assets/831656b2-aea7-4c2d-98c2-c203dd9a449e)


**Question 2**
---
Write a SQL statement to Update the hire_date of employees in department 50 to 2024-01-24.

Employees table :
employee_id,first_name,last_name,emailphone_number,hire_date,job_id,salary,commission_pct,manager_id,department_id

```sql
UPDATE EMPLOYEES SET
HIRE_DATE='2024-01-24'
WHERE DEPARTMENT_ID=50;
```

**Output:**

![image](https://github.com/user-attachments/assets/fb327c54-215c-4e33-92f3-ea78623da544)


**Question 3**
---
Write a SQL query to Delete a Specific Surgery whose ID is 3 or surgeon ID is 4.
Sample table: Surgeries

```sql
DELETE FROM surgeries WHERE
surgery_id=3 OR surgeon_id=4;
```

**Output:**

![image](https://github.com/user-attachments/assets/ca68d4a4-69eb-4f8b-ae5e-704473a52ff4)


**Question 4**
---
Write a SQL query to Delete customers with following conditions
'CUST_COUNTRY' is not in a list of specified countries ('UK', 'USA', 'Canada')
'GRADE' is greater than or equal to 3
Sample table: Customer

```sql
DELETE FROM Customer WHERE
CUST_COUNTRY NOT IN('UK', 'USA', 'Canada') AND GRADE>=3;
```

**Output:**

![image](https://github.com/user-attachments/assets/9e359c5c-91ad-4a02-b4eb-0f7574001aff)


**Question 5**
---
Write a SQL query to Delete customers from 'customer' table where 'GRADE' is not equal to 3.
Sample table: Customer

```sql
DELETE FROM Customer
WHERE grade!=3;
```

**Output:**

![image](https://github.com/user-attachments/assets/345855d7-f442-42df-8891-4c691b127ea3)


**Question 6**
---
Write a SQL statement to Find all those customers with all information whose names are ending with the letter 'n'.
customer table

```sql
SELECT * FROM customer
WHERE cust_name LIKE "%n";
```

**Output:**

![image](https://github.com/user-attachments/assets/31e74c5d-fa2c-495d-8a9c-9e9bde737d39)


**Question 7**
---
Write a SQL statement to show all the contact_name, address, city of all customers who are from 'Germany', 'Mexico' and 'Spain' countries.

customers table

```sql
SELECT ContactName,Address,City FROM customers
WHERE Country IN('Germany','Mexico','Spain');
```

**Output:**

![image](https://github.com/user-attachments/assets/f4a327eb-e745-40ef-9121-8abdad0255ec)


**Question 8**
---
Write a SQL query to calculate the discount amount for each product. Return product_id, original_price, discount_percentage, and discount_amount.
Sample table: Products

```sql
SELECT product_id,original_price,discount_percentage,
original_price*discount_percentage AS discount_amount
FROM Products;
```

**Output:**

![image](https://github.com/user-attachments/assets/ffe9394e-889e-428b-9297-bf881b0b55f4)


**Question 9**
---
Write a SQL query to retrieve the year, month, and day from the hiredate column in the emp table.

```sql
SELECT STRFTIME('%Y',hiredate) AS Year,
STRFTIME('%m',hiredate) AS Month,
STRFTIME('%d',hiredate) AS Day FROM emp;
```

**Output:**

![image](https://github.com/user-attachments/assets/acffde14-7eb4-4527-9c56-50c7c7d3647f)


**Question 10**
---
Create a report that shows the capitalized FirstName and capitalized LastName renamed as FirstName and Lastname respectively and EmployeeId from the employees table sorted by EmployeeId in descending order.
employees table

```sql
SELECT UPPER(FirstName) AS FirstName,UPPER(LastName) AS LastName,EmployeeID FROM employees
ORDER BY EmployeeID DESC;
```

**Output:**

![image](https://github.com/user-attachments/assets/0aa9423f-762a-49b0-ace8-caa5d8550296)


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
