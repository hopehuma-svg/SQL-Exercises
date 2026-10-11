# brightlearn-sql-case-statements

Solutions and table schemas for **BrightLearn Data Analytics: Exercise 03 (SQL Foundations)**. This set focuses entirely on row classification using conditional logic via `CASE` expressions.

## Focus Areas
* Simple and searched `CASE` syntax
* Multi-conditional filtering (`BETWEEN`, `AND`, `OR`, comparison operators)
* Row classification into custom buckets (price tiers, grades, status tracking)

---

## Solutions

### 01. The products Table
Classify products into price categories (`Budget`, `Mid-range`, `Expensive`).

```sql
SELECT 
    product_name,
    price,
    CASE 
        WHEN price > 1000 THEN 'Expensive'
        WHEN price BETWEEN 100 AND 1000 THEN 'Mid-range'
        ELSE 'Budget'
    END AS price_category
FROM products;
```

### 02. The orders Table
Categorize orders by their monetary valuation.

```sql
SELECT 
    customer_name,
    amount,
    CASE 
        WHEN amount >= 1000 THEN 'High Value'
        WHEN amount BETWEEN 500 AND 999.99 THEN 'Medium Value'
        ELSE 'Low Value'
    END AS order_value_category
FROM orders;
```

### 03. The employees Table
Combine department and salary parameters to verify corporate seniority.

```sql
SELECT 
    emp_name,
    department,
    salary,
    CASE 
        WHEN department = 'IT' AND salary > 85000 THEN 'Senior IT'
        WHEN department = 'HR' AND salary > 55000 THEN 'Experienced HR'
        ELSE 'Staff'
    END AS position_level
FROM employees;
```

### 04. The students Table
Convert raw numerical grade scores into distinct alphabetical blocks.

```sql
SELECT 
    student_name,
    score,
    CASE 
        WHEN score >= 90 THEN 'A'
        WHEN score BETWEEN 80 AND 89 THEN 'B'
        WHEN score BETWEEN 70 AND 79 THEN 'C'
        WHEN score BETWEEN 60 AND 69 THEN 'D'
        ELSE 'F'
    END AS grade
FROM students;
```

### 05. The deliveries Table
Evaluate order fulfillment speeds.

```sql
SELECT 
    delivery_id,
    delivery_time_minutes,
    CASE 
        WHEN delivery_time_minutes <= 30 THEN 'Fast'
        WHEN delivery_time_minutes BETWEEN 31 AND 60 THEN 'On Time'
        ELSE 'Late'
    END AS performance
FROM deliveries;
```

### 06. The tickets Table
Map numeric prioritization logs to system string descriptions.

```sql
SELECT 
    issue_type,
    priority,
    CASE priority
        WHEN 3 THEN 'High'
        WHEN 2 THEN 'Medium'
        WHEN 1 THEN 'Low'
    END AS priority_label
FROM tickets;
```

### 07. The attendance Table
Calculate baseline presence metrics and map the corresponding output standing.

```sql
SELECT 
    student_id,
    (days_present * 100.0 / total_days) AS attendance_percentage,
    CASE 
        WHEN (days_present * 100.0 / total_days) >= 90 THEN 'Excellent'
        WHEN (days_present * 100.0 / total_days) BETWEEN 75 AND 89 THEN 'Good'
        ELSE 'Needs Improvement'
    END AS attendance_status
FROM attendance;
```

### 08. The products_inventory Table
Track stock volumes against structural system minimum flags.

```sql
SELECT 
    product_id,
    stock_qty,
    CASE 
        WHEN stock_qty = 0 THEN 'Out of Stock'
        WHEN stock_qty BETWEEN 1 AND 5 THEN 'Low Stock'
        ELSE 'In Stock'
    END AS stock_status
FROM products_inventory;
```

### 09. The classes Table
Define cohort volumes based on explicit roster sizes.

```sql
SELECT 
    subject,
    enrolled_students,
    CASE 
        WHEN enrolled_students >= 25 THEN 'Large'
        WHEN enrolled_students BETWEEN 10 AND 24 THEN 'Medium'
        ELSE 'Small'
    END AS class_size_category
FROM classes;
```

### 10. The payments Table
Isolate combined transaction payment choices and thresholds to configure targeted promo qualifications.

```sql
SELECT 
    payment_id,
    payment_method,
    amount,
    CASE 
        WHEN payment_method = 'Cash' AND amount >= 200 THEN 'Eligible for Discount'
        ELSE 'Not Eligible'
    END AS discount_eligibility
FROM payments;
```
