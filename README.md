# Interview Preparation Guide

This document is a complete and simple guide to help you crack interviews. It includes key questions and answers with code examples in simple language.

---

## 📁 Database Management & SQL

### 1. Aggregate Functions
**Q: What are aggregate functions in SQL?**  
**A:** Aggregate functions perform a calculation on a set of values and return a single value.  
**Examples:** `SUM()`, `AVG()`, `MAX()`, `MIN()`, `COUNT()`

```sql
SELECT AVG(salary) FROM employees;
SELECT COUNT(*) FROM employees WHERE department = 'HR';
```

---

### 2. Joins
**Q: What are Joins in SQL?**  
**A:** Joins are used to combine rows from two or more tables based on a related column.

```sql
-- INNER JOIN
SELECT emp.name, dept.name
FROM employee emp
INNER JOIN department dept ON emp.dept_id = dept.id;

-- LEFT JOIN
SELECT emp.name, dept.name
FROM employee emp
LEFT JOIN department dept ON emp.dept_id = dept.id;
```

---

### 3. Nested Queries / Subqueries
**Q: What is a subquery?**  
**A:** A subquery is a query inside another query.

```sql
SELECT name FROM employee
WHERE salary > (SELECT AVG(salary) FROM employee);
```

---

## 🐍 Python Programming

### 1. OOPS (Object-Oriented Programming)
```python
class Car:
    def __init__(self, brand):
        self.brand = brand

    def drive(self):
        print(f"Driving {self.brand}")

car1 = Car("Toyota")
car1.drive()
```

### 2. Error Handling
```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```

### 3. User-Defined Function
```python
def greet(name):
    return f"Hello {name}"

print(greet("Alice"))
```

### 4. Fibonacci Series
```python
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        print(a, end=" ")
        a, b = b, a + b

fibonacci(10)
```

### 5. Palindrome Check
```python
def is_palindrome(word):
    return word == word[::-1]

print(is_palindrome("madam"))  # True
```

### 6. Matrix Example
```python
matrix = [
    [1, 2],
    [3, 4]
]
for row in matrix:
    print(row)
```

---

## 🤖 AI & ML

### 1. Classifiers
**Q: What is a classifier?**  
**A:** A classifier is a model used to assign labels to input data.
```python
from sklearn.naive_bayes import GaussianNB
model = GaussianNB()
```

### 2. Regressions
**Q: What is regression?**  
**A:** Predicting continuous values.
```python
from sklearn.linear_model import LinearRegression
model = LinearRegression()
```

### 3. RAG (Retrieval Augmented Generation)
**Q: What is RAG?**  
**A:** It combines retrieval of data and generative models to give better answers.

### 4. Supervised vs Unsupervised
- **Supervised:** Uses labeled data (e.g., Classification, Regression)
- **Unsupervised:** Uses unlabeled data (e.g., Clustering)

---

## ☁️ Cloud Computing

### AWS (Amazon Web Services)
**Q: What is EC2?**  
**A:** EC2 is a virtual server to run applications in AWS.

**Q: What is S3?**  
**A:** S3 is a storage service to store and retrieve files.

### Azure
**Q: What is Azure VM?**  
**A:** A virtual machine to run services in Microsoft Azure.

**Q: What is Azure Blob Storage?**  
**A:** Used to store large amounts of unstructured data like images, videos, etc.

---

> Keep practicing! Best of luck for your interview 🚀

