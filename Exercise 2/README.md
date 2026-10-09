# BrightLearn SQL Foundations: Aggregate Functions & Operators 

## Project Overview
This repository contains my solutions and handwritten sketches for **BrightLearn Data Analytics Exercise 02: SQL Foundations**. The objective of this lab is to master the execution of aggregate functions, complex filtering logic, data grouping patterns, and result limitations across relational database tables. 

The exercise focuses on a "Read, Query, and Draw" methodology—hand-writing structurally sound SQL syntax and predicting the exact relational output tables prior to engine execution.

##  Core Learning Objectives
* **Data Aggregation:** Processing calculations across row subsets using `COUNT()`, `SUM()`, `AVG()`, `MIN()`, and `MAX()`.
* **Grouping & Filtering Blocks:** Organizing relational rows with `GROUP BY` and applying conditional group criteria via `HAVING`.
* **Logical Operators:** Implementing `DISTINCT`, `BETWEEN`, `IN`, `NOT`, `AND`, and `OR` to run precise row triage.
* **Output Optimization:** Sorting and capping query result lengths using `ORDER BY` and `LIMIT` adjustments.
* **Column Customization:** Utilizing explicit `AS` aliases to construct clear, corporate-ready reporting headers.

---

##  Relational Database Schema
The project executes 15 distinct business queries across 5 independent entity tables:

1. **`students`**: Records student enrollment tracking metadata including age parameters and academic department tags.
2. **`courses`**: A centralized curriculum catalog detailing course identities, subjects, and assigned credit values.
3. **`enrollments`**: A transactional link registry mapping student IDs to courses alongside final academic performance grades.
4. **`salaries`**: A simple payroll table capturing foundational employee salary data, bonus allocations, and business departments.
5. **`projects`**: A localized corporate registry listing active business projects, handling divisions, and specific budget allocations.

---

##  Query Inventory & Solutions Covered

### 01 | Student Registry Analysis (The `students` Table)
* **Query 01:** Isolating distinct operating departments using `DISTINCT`.
* **Query 02:** Computing the credit-weighted average age of students per unique department using `AVG()` and `GROUP BY`.
* **Query 03:** Filtering out individual departments to isolate sections managing more than 1 active student profile using `HAVING COUNT() > 1`.
* **Query 04:** Fetching specific student blocks using numerical boundaries with the `BETWEEN 21 AND 23` operator.
* **Query 05:** Running compound row isolation to find mature students (>21) inside target departments using conditional `IN('IT', 'HR')` arrays.

### 02 | Curriculum Architecture (The `courses` Table)
* **Query 06:** Summing up department credit payloads and applying dual-layer filters with combined `WHERE`, `GROUP BY`, and `HAVING` logic.
* **Query 07:** Performing complete mismatch identification across credit matrices using the `NOT` or `!=` operators.
* **Query 08:** Querying the top 3 highest-valued credit profiles ordered sequentially using `ORDER BY DESC` and `LIMIT 3` restrictions.

### 03 | Transactional Grade Records (The `enrollments` Table)
* **Query 09:** Generating a holistic statistical profile (Maximum, Minimum, and Average metrics) for final grades across all active enrollments utilizing explicit `AS` aliasing.
* **Query 10:** Processing volumetric aggregation to count how many individual student enrollments exist per unique course code.

### 04 | Payroll and Operations Triage (The `salaries` Table)
* **Query 11:** Calculating total baseline payroll costs and cumulative bonus payloads grouped by active business sectors.
* **Query 12:** Screening organizational structures to isolate departments maintaining baseline average salaries above a 55,000 threshold.
* **Query 13:** Computing inline calculations (`salary + bonus`) to identify employees whose total structural compensation values exceed 60,000.

### 05 | Capital Project Controls (The `projects` Table)
* **Query 14:** Aggregating cumulative and average budgets across structural teams, enforcing strict group baseline caps over 70,000.
* **Query 15:** Running deep boundary queries for project values between 50,000 and 120,000 while explicitly excluding specific operational divisions (e.g., Marketing).

---

##  Tech Stack & Methodology
* **Language:** Structured Query Language (SQL)
* **Standards Enforced:** ANSI SQL Standards (Keywords in `UPPERCASE`, system variables/tables in `lowercase`).
* **Execution Format:** Handwritten pen-and-paper mapping to cultivate immediate syntax visualization capabilities prior to database deployment.

