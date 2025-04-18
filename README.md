# Interview Preparation Guide

This document is a comprehensive interview preparation guide covering topics in:
- **Database Management & SQL**
- **Python Programming**
- **Artificial Intelligence & Machine Learning**
- **Cloud Computing (AWS & Azure)**

Each topic includes **Theory**, **Q&A**, and **Examples with Code** in **simple language**.

---

## 📘 Database Management & SQL

### 🔹 Aggregate Functions

**Theory**: Aggregate functions perform a calculation on a set of values and return a single value.

**Common Functions**: `SUM()`, `AVG()`, `COUNT()`, `MIN()`, `MAX()`

**Q&A**:
- **Q: What does COUNT() do?**
  - A: It counts the number of rows that match a specified condition.

**Example**:
```sql
SELECT COUNT(*) FROM employees WHERE department = 'Sales';
```

---

### 🔹 Joins

**Theory**: Joins combine rows from two or more tables based on a related column.

**Types**: INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL JOIN

**Q&A**:
- **Q: What is INNER JOIN?**
  - A: It returns rows that have matching values in both tables.

**Example**:
```sql
SELECT employees.name, departments.dept_name
FROM employees
INNER JOIN departments ON employees.dept_id = departments.id;
```

---

### 🔹 Nested Queries & Subqueries

**Theory**: A subquery is a query inside another query.

**Q&A**:
- **Q: Where can subqueries be used?**
  - A: In SELECT, FROM, and WHERE clauses.

**Example**:
```sql
SELECT name FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```

---

## 🐍 Python Programming

### 🔹 OOPS (Object-Oriented Programming)

**Theory**: OOP is based on objects and classes.

**Concepts**: Class, Object, Inheritance, Polymorphism, Encapsulation

**Example**:
```python
class Person:
    def __init__(self, name):
        self.name = name
    def greet(self):
        print("Hello, my name is", self.name)

p = Person("Alice")
p.greet()
```

---

### 🔹 Error Handling

**Theory**: Use try-except blocks to handle exceptions.

**Example**:
```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

---

### 🔹 User-Defined Functions

```python
def add(a, b):
    return a + b
print(add(3, 5))
```

---

### 🔹 Fibonacci Series

```python
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        print(a, end=' ')
        a, b = b, a + b
fibonacci(10)
```

---

### 🔹 Palindrome Check

```python
def is_palindrome(s):
    return s == s[::-1]
print(is_palindrome("madam"))
```

---

### 🔹 Matrix Operations

```python
A = [[1, 2], [3, 4]]
B = [[5, 6], [7, 8]]
result = [[A[i][j] + B[i][j] for j in range(2)] for i in range(2)]
print(result)
```

---

## 🤖 AI & ML

### 🔹 Supervised Learning
**Theory**: Learning with labeled data (e.g. classification, regression)

### 🔹 Unsupervised Learning
**Theory**: Learning without labeled data (e.g. clustering)

### 🔹 Classification
**Example**:
```python
from sklearn.linear_model import LogisticRegression
model = LogisticRegression()
model.fit(X_train, y_train)
```

### 🔹 Regression
**Example**:
```python
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(X_train, y_train)
```

### 🔹 RAG (Retrieval Augmented Generation)
**Theory**: Combines a retriever to fetch relevant documents and a generator (like GPT) to generate answers.

---

## ☁️ Cloud Computing

### 🔹 AWS
- **EC2**: Virtual machine
- **S3**: Object storage
- **RDS**: Managed database service
- **Lambda**: Serverless compute

### 🔹 Azure
- **VM**: Azure Virtual Machines
- **Blob Storage**: Object storage
- **Azure SQL**: Managed SQL DB
- **Functions**: Serverless compute

---

## 📌 Tips for Interview
- Always explain logic simply.
- Write clean and commented code.
- Be confident in explaining your thought process.

---
