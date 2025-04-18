# 📘 Interview Preparation: Q&A with Code

This repository contains simplified **Questions and Answers** with **code examples** for interview preparation, covering:

- ✅ Database Management & SQL  
- 🐍 Python Programming  
- 🧠 AI & Machine Learning  
- ☁️ Cloud (AWS & Azure)
---

## ✅ Database Management & SQL

### 🔹 Q1: What are Aggregate Functions in SQL?
**Answer:** Aggregate functions perform calculations on multiple values and return a single value.

**Examples:**
```sql
SELECT COUNT(*) FROM employees;
SELECT AVG(salary) FROM employees;
SELECT MAX(age), MIN(age) FROM employees;
```

---

### 🔹 Q2: What is a JOIN? Types of JOINs?
**Answer:** A JOIN combines rows from two or more tables based on related columns.

**Types:**
- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- FULL JOIN

**Example:**
```sql
SELECT e.name, d.department_name
FROM employees e
INNER JOIN departments d ON e.department_id = d.id;
```

---

### 🔹 Q3: What is a Subquery & Nested Query?
**Answer:** A subquery is a query within another query.

**Example:**
```sql
SELECT name FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```

---

## 🐍 Python Programming

### 🔹 Q1: What is OOPS in Python?
**Answer:** OOP stands for Object-Oriented Programming. Key concepts: Class, Object, Inheritance, Encapsulation, Polymorphism.

**Example:**
```python
class Animal:
    def __init__(self, name):
        self.name = name
    def speak(self):
        return f"{self.name} makes a sound."

class Dog(Animal):
    def speak(self):
        return f"{self.name} barks."

dog = Dog("Buddy")
print(dog.speak())  # Buddy barks.
```

---

### 🔹 Q2: What is Error Handling in Python?
**Answer:** Used to handle exceptions using try-except blocks.

**Example:**
```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```

---

### 🔹 Q3: What is a User-Defined Function?
**Answer:** A function created by the user using `def`.

**Example:**
```python
def greet(name):
    return f"Hello, {name}"

print(greet("John"))
```

---

### 🔹 Q4: Fibonacci Series in Python
```python
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        print(a, end=" ")
        a, b = b, a + b

fibonacci(10)
```

---

### 🔹 Q5: Palindrome Program
```python
def is_palindrome(s):
    return s == s[::-1]

print(is_palindrome("madam"))  # True
```

---

### 🔹 Q6: Matrix Addition
```python
A = [[1, 2], [3, 4]]
B = [[5, 6], [7, 8]]

result = [[A[i][j] + B[i][j] for j in range(len(A[0]))] for i in range(len(A))]
print(result)
```

---

## 🧠 AI & Machine Learning

### 🔹 Q1: What are Classifiers?
**Answer:** Algorithms used for classification tasks (e.g., SVM, Decision Tree, KNN).

**Example (Logistic Regression in Sklearn):**
```python
from sklearn.linear_model import LogisticRegression
model = LogisticRegression()
model.fit(X_train, y_train)
```

---

### 🔹 Q2: What is Regression?
**Answer:** Predicting continuous values. (e.g., Linear Regression, Ridge)

**Example:**
```python
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(X_train, y_train)
```

---

### 🔹 Q3: Supervised vs Unsupervised Learning
**Answer:**
- Supervised: Uses labeled data (e.g., Classification, Regression)
- Unsupervised: Uses unlabeled data (e.g., Clustering, PCA)

---

### 🔹 Q4: What is RAG (Retrieval Augmented Generation)?
**Answer:** It combines a retriever (fetches documents) and a generator (like LLMs) to answer queries using external knowledge.

---

## ☁️ Cloud (AWS & Azure)

### 🔹 Q1: What is AWS?
**Answer:** Amazon Web Services - A cloud computing platform offering compute, storage, and networking.

**Common Services:**
- EC2 (Compute)
- S3 (Storage)
- Lambda (Serverless)
- RDS (Database)

---

### 🔹 Q2: What is Azure?
**Answer:** Microsoft Azure - A cloud platform offering similar services like:
- Azure VM (Compute)
- Blob Storage (Storage)
- Azure Functions (Serverless)
- Azure SQL (Database)

---

### 🔹 Q3: Difference between AWS and Azure
| Feature        | AWS           | Azure         |
|----------------|----------------|----------------|
| Compute        | EC2            | Azure VM       |
| Storage        | S3             | Blob Storage   |
| Serverless     | Lambda         | Azure Functions|
| Database       | RDS            | Azure SQL      |

---

> 📌 **Tip:** Practice regularly and build small projects to showcase your skills during interviews.
```

---

Let me know if you'd like a downloadable version or a GitHub repo initialized with this file!
