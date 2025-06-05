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

- **Q: What is LEFT JOIN?**
  - A: Returns all records from the left table, and the matched records from the right table; if there is no match, the result is NULL on the right side.

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
Absolutely! Here's a **simple, interview-friendly explanation** of the **4 pillars of Object-Oriented Programming (OOP)** without using any code:

---

### 1. **Encapsulation**  
🔒 **"Wrapping data and methods into one unit."**

- Think of a capsule in medicine — it holds different ingredients inside one cover.  
- In programming, we bundle data (variables) and code (functions) that work on the data into one class.  
- It **protects data** from outside interference.  
- Example: You can use your phone, but you don’t need to know how the circuits inside work.

---

### 2. **Abstraction**  
🎭 **"Showing only the essential details, hiding the complexity."**

- Just like when you drive a car — you use the steering, brake, and accelerator without needing to know how the engine works.  
- It **hides the internal logic** and only exposes necessary parts.  
- Focuses on **what** an object does, not **how** it does it.

---

### 3. **Inheritance**  
👨‍👧 **"Reusing features from one class into another."**

- It’s like children inheriting traits from parents.  
- One class (child) gets properties and behaviors from another class (parent).  
- Helps in **code reusability** and building relationships between classes.

---

### 4. **Polymorphism**  
🎭 **"One name, many forms."**

- The same action behaves differently depending on the object.  
- For example, a single word “speak” — a dog barks, a cat meows, a human talks.  
- It allows **functions or methods to behave differently** based on context or object type.

---

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

Sure! Here's a **simple and clear explanation** of `try`, `except`, `else`, and `finally` in Python — perfect for interviews:

---

### 🧠 Imagine you're writing code that might cause an error.  
Python gives you a way to **handle those errors** without crashing the program using:

---

### ✅ `try`:  
**"Try this code, it might work..."**  
- You write the code that might cause an error here.

---

### ❌ `except`:  
**"If there’s an error, do this instead."**  
- This block will run **only if there's an error** in the try block.  
- Helps in **catching and handling** the error.

---

### 🎉 `else`:  
**"If no error happens, do this."**  
- Runs **only if the try block succeeds** without any error.  
- It’s like saying: “If everything goes well, continue here.”

---

### 🔒 `finally`:  
**"Do this no matter what happens."**  
- This block runs **always** — whether there was an error or not.  
- Great for **cleaning up**, like closing files or database connections.

---

### 📦 Simple Analogy:
Imagine you are withdrawing money from an ATM:

- `try`: Insert card and withdraw money  
- `except`: If the card is blocked, show error  
- `else`: If everything is fine, print “Transaction successful”  
- `finally`: Eject the card — this happens in all cases

Sure! Here's a simple **Python code example** that demonstrates `try`, `except`, `else`, and `finally` — along with its **output**:

---

### ✅ **Code:**

```python
def divide(a, b):
    try:
        result = a / b
    except ZeroDivisionError:
        print("❌ Cannot divide by zero!")
    else:
        print("✅ Division successful. Result =", result)
    finally:
        print("🔁 This runs no matter what (clean-up, closing files, etc).")

# Example 1: No error
divide(10, 2)

print()  # Just for spacing

# Example 2: Division by zero
divide(5, 0)
```

---

### 📤 **Output:**

```
✅ Division successful. Result = 5.0
🔁 This runs no matter what (clean-up, closing files, etc).

❌ Cannot divide by zero!
🔁 This runs no matter what (clean-up, closing files, etc).
```

---

Let me know if you'd like a **real-life use case** of this in file handling or database operations — that's often asked in interviews too.
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
Sure! Let's dive into **Flask** and **FastAPI**, two of the most popular Python web frameworks, and compare them in detail.

---

## 🚀 **Flask**

### 🔹 Overview
- **Flask** is a **lightweight**, **micro web framework** for Python.
- It's been around since **2010**, and is known for being simple and flexible.
- It gives developers the freedom to structure their app as they see fit.

### 🔹 Key Features
- Minimal and simple to get started.
- Supports extensions like Flask-SQLAlchemy, Flask-Login, etc.
- Based on Werkzeug (WSGI) and Jinja2 templating engine.
- Good for small to medium applications or quick prototyping.

### 🔹 Basic Example

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return 'Hello, Flask!'

if __name__ == '__main__':
    app.run(debug=True)
```

### 🔹 Pros
- Very beginner-friendly.
- Large community and mature ecosystem.
- Tons of plugins and documentation.

### 🔹 Cons
- Slower performance compared to FastAPI.
- Manual data validation required.
- Async support is limited.

---

## ⚡ **FastAPI**

### 🔹 Overview
- **FastAPI** is a **modern**, **fast (high-performance)** web framework built on **Starlette** and **Pydantic**.
- Released in **2018**.
- Designed for building APIs with automatic OpenAPI documentation.

### 🔹 Key Features
- Built-in support for **data validation** using **Pydantic**.
- **Auto-generated Swagger docs**.
- **Asynchronous (async/await)** support out-of-the-box.
- Based on ASGI (Asynchronous Server Gateway Interface) → better performance.

### 🔹 Basic Example

```python
from fastapi import FastAPI

app = FastAPI()

@app.get('/')
async def read_root():
    return {"message": "Hello, FastAPI!"}
```

### 🔹 Pros
- Fast and asynchronous.
- Auto data validation and serialization.
- Auto Swagger UI and ReDoc for API docs.
- Great for building modern APIs and microservices.

### 🔹 Cons
- Slightly more complex to learn if you're a beginner.
- Smaller ecosystem compared to Flask (though growing fast).

---

## 🔍 Comparison Table

| Feature                | Flask                        | FastAPI                      |
|------------------------|------------------------------|------------------------------|
| **Performance**        | Slower (WSGI)                | Faster (ASGI + async)        |
| **Ease of Use**        | Easier for beginners         | Slightly more complex        |
| **Async Support**      | Partial                      | Native support               |
| **Data Validation**    | Manual                       | Automatic (Pydantic)         |
| **Docs Generation**    | Manual (with tools)          | Automatic (Swagger & ReDoc)  |
| **Release Year**       | 2010                         | 2018                         |
| **Best For**           | Simple websites & APIs       | High-performance APIs        |

---

## 🧪 Real-world Use Cases

| Use Case                      | Use Flask For                             | Use FastAPI For                            |
|------------------------------|-------------------------------------------|--------------------------------------------|
| Quick prototypes             | ✅                                          | ✅                                          |
| Data-heavy APIs              | ❌                                          | ✅                                          |
| Machine Learning model APIs  | ✅ (but less efficient)                    | ✅ (better performance with async)          |
| Real-time applications       | ❌                                          | ✅                                          |
| Full-stack web app           | ✅                                          | ⚠️ (limited templating support)            |

---

It automatically:
- Validates the JSON input.
- Generates interactive docs at `/docs`.

---

## 🧠 Conclusion

- Use **Flask** if you want simplicity, flexibility, and are building a traditional web app or a small API.
- Use **FastAPI** if you need high performance, auto validation, and modern async features—especially useful for APIs and machine learning model deployment.

---
Here are **15 complex multiple-choice questions and answers (OMR-style)** for each of the following sections tailored for a **1–2 years experienced professional**:

---

## 📘 Section 1: **Database Management & SQL**

| Q.No | Question                                                     | Options                                                                                                                                                | Answer |
| ---- | ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------ |
| 1    | What does the `WITH` clause in SQL provide?                  | A) A loop in SQL<br>B) A temporary result set<br>C) A constraint<br>D) A join condition                                                                | B      |
| 2    | Which normal form removes transitive dependency?             | A) 1NF<br>B) 2NF<br>C) 3NF<br>D) BCNF                                                                                                                  | C      |
| 3    | What is a correlated subquery?                               | A) A query inside a query<br>B) A subquery that uses outer query values<br>C) Joins<br>D) View                                                         | B      |
| 4    | What does the `EXPLAIN` statement do?                        | A) Deletes a table<br>B) Creates indexes<br>C) Shows query plan<br>D) Performs joins                                                                   | C      |
| 5    | Which index is best for searching a range of values?         | A) Hash Index<br>B) B-Tree<br>C) Bitmap<br>D) Full-text                                                                                                | B      |
| 6    | What is the result of `SELECT NULL + 5` in most SQL engines? | A) 5<br>B) NULL<br>C) 0<br>D) Error                                                                                                                    | B      |
| 7    | Which isolation level can lead to phantom reads?             | A) READ UNCOMMITTED<br>B) READ COMMITTED<br>C) REPEATABLE READ<br>D) SERIALIZABLE                                                                      | C      |
| 8    | When is a full table scan preferred over an index scan?      | A) For small tables<br>B) When no WHERE clause<br>C) When index is corrupt<br>D) All of the above                                                      | D      |
| 9    | Which clause is used to filter aggregated data?              | A) WHERE<br>B) HAVING<br>C) GROUP BY<br>D) SELECT                                                                                                      | B      |
| 10   | What does ACID stand for in databases?                       | A) Accurate, Consistent, Isolated, Durable<br>B) Atomicity, Consistency, Isolation, Durability<br>C) Accurate, Calculated, Indexed, Durable<br>D) None | B      |
| 11   | What is a primary key?                                       | A) A nullable unique identifier<br>B) Always auto-increment<br>C) Uniquely identifies a row<br>D) All of the above                                     | C      |
| 12   | What is a deadlock in SQL?                                   | A) Query timeout<br>B) Two transactions waiting on each other<br>C) Memory leak<br>D) None                                                             | B      |
| 13   | What does `ROWNUM` in Oracle represent?                      | A) Row ID<br>B) Result order<br>C) Sequential pseudo column<br>D) None                                                                                 | C      |
| 14   | What is the function of `COALESCE()` in SQL?                 | A) Joins columns<br>B) Returns first non-null<br>C) Aggregates<br>D) Checks type                                                                       | B      |
| 15   | What is a materialized view?                                 | A) Live query<br>B) View stored as data<br>C) Temporary table<br>D) Procedure                                                                          | B      |

---

## 🐍 Section 2: **Python Programming**

| Q.No | Question                                              | Options                                                                                              | Answer |
| ---- | ----------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------ |
| 1    | What is the output of `bool([])`?                     | A) True<br>B) False<br>C) None<br>D) Error                                                           | B      |
| 2    | Which data structure uses hashing for lookup?         | A) List<br>B) Tuple<br>C) Dictionary<br>D) Set                                                       | C      |
| 3    | What does `@staticmethod` mean?                       | A) Static function<br>B) No access to class/instance<br>C) Global function<br>D) Instance method     | B      |
| 4    | How is memory managed in Python?                      | A) Manual<br>B) Garbage collected<br>C) Not managed<br>D) Dynamic typing only                        | B      |
| 5    | Which is not a valid exception in Python?             | A) TypeError<br>B) IOError<br>C) NullPointerException<br>D) ValueError                               | C      |
| 6    | What will `a is b` return for `a = [1]`, `b = [1]`?   | A) True<br>B) False<br>C) Error<br>D) None                                                           | B      |
| 7    | Which module is used for performance profiling?       | A) cProfile<br>B) inspect<br>C) timeit<br>D) tracemalloc                                             | A      |
| 8    | What is the difference between `deepcopy` and `copy`? | A) No difference<br>B) `copy` is faster<br>C) `deepcopy` copies nested<br>D) `copy` is recursive     | C      |
| 9    | What is `*args` used for?                             | A) Keyword arguments<br>B) Fixed parameters<br>C) Arbitrary non-keyword arguments<br>D) None         | C      |
| 10   | What is GIL in Python?                                | A) A global function<br>B) A threading lock<br>C) Garbage Interpreter Lock<br>D) None                | B      |
| 11   | What does `__init__` do in a class?                   | A) Initializes class<br>B) Creates method<br>C) Deletes class<br>D) None                             | A      |
| 12   | Which keyword is used to define a generator?          | A) return<br>B) yield<br>C) async<br>D) pass                                                         | B      |
| 13   | What does `enumerate()` do?                           | A) Creates list<br>B) Creates index-object pair<br>C) Filters<br>D) None                             | B      |
| 14   | What is duck typing in Python?                        | A) Strong typing<br>B) Type casting<br>C) Type inferred at runtime<br>D) Object shape-based behavior | D      |
| 15   | Which Python web framework is ASGI-compatible?        | A) Flask<br>B) FastAPI<br>C) Django (WSGI)<br>D) Bottle                                              | B      |

---

## 🤖 Section 3: **Artificial Intelligence & Machine Learning**

| Q.No | Question                                                | Options                                                                                                                      | Answer |
| ---- | ------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ------ |
| 1    | What is overfitting in ML?                              | A) Model underperforms<br>B) Model performs too well on train data<br>C) Slow training<br>D) None                            | B      |
| 2    | Which technique is used to handle overfitting?          | A) Data augmentation<br>B) Early stopping<br>C) Regularization<br>D) All of the above                                        | D      |
| 3    | What is the purpose of `train_test_split()` in sklearn? | A) Train only<br>B) Split data<br>C) Preprocess<br>D) Scale data                                                             | B      |
| 4    | What is precision in classification?                    | A) TP/(TP+FP)<br>B) TP/(TP+FN)<br>C) FP/(FP+TP)<br>D) TN/(TN+FN)                                                             | A      |
| 5    | What is RAG in modern LLM systems?                      | A) Recurrent Attention Generator<br>B) Retrieval-Augmented Generation<br>C) ReLU Activation Graph<br>D) Regularized AI Graph | B      |
| 6    | What does a confusion matrix not include?               | A) True Positives<br>B) False Positives<br>C) Recall<br>D) True Negatives                                                    | C      |
| 7    | What’s the role of activation functions?                | A) Normalize data<br>B) Introduce non-linearity<br>C) Initialize weights<br>D) Optimize loss                                 | B      |
| 8    | What is `fine-tuning` in NLP?                           | A) Training from scratch<br>B) Using pretrained model and updating weights<br>C) Pruning<br>D) Data cleaning                 | B      |
| 9    | What is vector embedding?                               | A) Numeric representation of features<br>B) Text formatting<br>C) Tokenization<br>D) Activation layer                        | A      |
| 10   | What is cosine similarity used for?                     | A) Model accuracy<br>B) Distance between vectors<br>C) Normalization<br>D) Loss calculation                                  | B      |
| 11   | What is the output of sigmoid activation?               | A) 0–1<br>B) -1 to 1<br>C) Any real number<br>D) Only integers                                                               | A      |
| 12   | What does model distillation aim to achieve?            | A) Better visualization<br>B) Compress large models<br>C) Regularization<br>D) Overfitting                                   | B      |
| 13   | What is batch normalization used for?                   | A) Faster training<br>B) Normalize activations<br>C) Reduce internal covariate shift<br>D) All of the above                  | D      |
| 14   | What is `cross entropy loss` used for?                  | A) Regression<br>B) Clustering<br>C) Classification<br>D) Reinforcement learning                                             | C      |
| 15   | What is the benefit of dropout in neural nets?          | A) Slower convergence<br>B) Better generalization<br>C) Higher complexity<br>D) Gradient descent                             | B      |

---

## ☁️ Section 4: **Cloud & Deployment (Preferred)**

| Q.No | Question                                             | Options                                                                                                     | Answer |
| ---- | ---------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ------ |
| 1    | What does `S3` stand for in AWS?                     | A) Simple Storage Service<br>B) Secure Storage Service<br>C) Static Storage Space<br>D) None                | A      |
| 2    | Which AWS service is best for hosting ML models?     | A) EC2<br>B) S3<br>C) Lambda<br>D) SageMaker                                                                | D      |
| 3    | Which Azure service provides notebooks and models?   | A) Azure DevOps<br>B) Azure ML Studio<br>C) Azure Blob<br>D) Azure Cosmos DB                                | B      |
| 4    | What is Docker primarily used for?                   | A) Scaling<br>B) Logging<br>C) Containerization<br>D) Deployment                                            | C      |
| 5    | Which of the following is serverless?                | A) EC2<br>B) Elastic Beanstalk<br>C) Lambda\<brD) LightSail                                                 | C      |
| 6    | What is an IAM role in AWS?                          | A) Identity verification<br>B) Access policy<br>C) Backup tool<br>D) Encryption key                         | B      |
| 7    | What is CI/CD in ML model deployment?                | A) Central Integration<br>B) Continuous Integration / Continuous Deployment<br>C) Cloud Internet<br>D) None | B      |
| 8    | Which is a container orchestration tool?             | A) GitHub<br>B) Jenkins<br>C) Kubernetes<br>D) Bitbucket                                                    | C      |
| 9    | How is a Flask app typically deployed to production? | A) Using WSGI server like Gunicorn<br>B) Flask run<br>C) Python run<br>D) Heroku only                       | A      |
| 10   | What is a Load Balancer used for?                    | A) Balancing databases<br>B) Managing memory<br>C) Distributing traffic<br>D) Scaling RAM                   | C      |
| 11   | What is Elastic Beanstalk?                           | A) Data warehouse<br>B) Platform-as-a-Service<br>C) Load balancer<br>D) Serverless engine                   | B      |
| 12   | What is ECS in AWS?                                  | A) Elastic Compute Service<br>B) Elastic Container Service<br>C) Edge Cloud Services<br>D) None             | B      |
| 13   | How is HTTPS enabled for a Flask app on EC2?         | A) With Gunicorn<br>B) SSL cert + Nginx<br>C) Flask SSL<br>D) AWS by default                                | B      |
| 14   | What is the benefit of using CDN for ML model API?   | A) Encrypts models<br>B) Improves latency<br>C) Data pipeline<br>D) Version control                         | B      |
| 15   | What is the use of Dockerfile?                       | A) Logs container<br>B) Describes container build steps<br>C) Runs cronjob<br>D) None                       | B      |

---

## 🔹 SQL Section

### 1. **What is the difference between DDL and DML?**

**Answer:**

* **DDL (Data Definition Language):** Used to define schema – `CREATE`, `ALTER`, `DROP`.
* **DML (Data Manipulation Language):** Used to manipulate data – `INSERT`, `UPDATE`, `DELETE`.

---

### 2. **Write a query to get the 2nd highest salary from a table `employees`.**

```sql
SELECT MAX(salary) 
FROM employees 
WHERE salary < (SELECT MAX(salary) FROM employees);
```

---

### 3. **Aggregate Functions Example**

```sql
SELECT 
    COUNT(*) AS total_employees,
    AVG(salary) AS avg_salary,
    MIN(salary) AS min_salary,
    MAX(salary) AS max_salary
FROM employees;
```

---

### 4. **Difference between INNER JOIN and OUTER JOIN**

* **INNER JOIN:** Returns matching records from both tables.
* **OUTER JOIN:** Returns matching + non-matching records (NULLs filled in non-matches).

```sql
SELECT e.name, d.dept_name
FROM employees e
LEFT JOIN departments d ON e.dept_id = d.id;
```

---

### 5. **Example of Window Function**

```sql
SELECT name, salary,
       RANK() OVER (ORDER BY salary DESC) AS rank
FROM employees;
```

---

### 6. **Query Optimization Techniques**

* Use **indexes**
* Avoid `SELECT *`
* Use **JOINs** wisely
* Use **LIMIT** to restrict rows

---

## 🔹 Python Section

### 1. **What are Python data types?**

**Answer:** int, float, str, list, tuple, dict, set, bool

```python
x = 5
print(type(x))  # <class 'int'>
```

---

### 2. **Numpy Example**

```python
import numpy as np
arr = np.array([1, 2, 3])
print(arr.mean())  # Output: 2.0
```

---

### 3. **Pandas Example**

```python
import pandas as pd
data = {'Name': ['John', 'Jane'], 'Salary': [50000, 60000]}
df = pd.DataFrame(data)
print(df.describe())
```

---

### 4. **Data Visualization using Matplotlib**

```python
import matplotlib.pyplot as plt

salaries = [40000, 50000, 60000]
names = ['John', 'Jane', 'Doe']
plt.bar(names, salaries)
plt.title('Employee Salary')
plt.show()
```

---

### 5. **Regex in Python**

```python
import re
text = "Email me at test@example.com"
match = re.search(r'\S+@\S+', text)
print(match.group())  # Output: test@example.com
```

---

## 🔹 Data Structures (Python)

### 1. **Reverse a list**

```python
my_list = [1, 2, 3, 4]
print(my_list[::-1])
```

---

### 2. **Check for Palindrome**

```python
def is_palindrome(s):
    return s == s[::-1]

print(is_palindrome("madam"))  # True
```

---

### 3. **Binary Search**

```python
def binary_search(arr, target):
    low, high = 0, len(arr)-1
    while low <= high:
        mid = (low + high)//2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1
    return -1

print(binary_search([1, 2, 3, 4, 5], 4))  # Output: 3
```

---
Here are the **questions, explanations, and Python code** for the three topics you asked about: **Fibonacci series**, **Leader numbers**, and **Triangle star pattern**.

---

## 🔷 1. Fibonacci Series

**Q: Write a Python program to generate the Fibonacci series up to `n` terms.**

**Fibonacci Series:** 0, 1, 1, 2, 3, 5, 8, 13, ...

**Code:**

```python
def fibonacci(n):
    a, b = 0, 1
    for i in range(n):
        print(a, end=' ')
        a, b = b, a + b

# Example: First 10 terms
fibonacci(10)
```

---

## 🔷 2. Leader Numbers in an Array

**Q: Write a Python program to find leader elements in an array.**

**Definition:** A **leader** is an element that is **greater than all the elements to its right** in the array.

**Example:**
For input `[16, 17, 4, 3, 5, 2]` → Output: `17, 5, 2`

**Code:**

```python
def find_leaders(arr):
    n = len(arr)
    leaders = []
    max_from_right = arr[-1]
    leaders.append(max_from_right)
    
    for i in range(n-2, -1, -1):
        if arr[i] > max_from_right:
            max_from_right = arr[i]
            leaders.append(max_from_right)
    
    # Reverse to maintain order of appearance
    leaders.reverse()
    return leaders

# Example
arr = [16, 17, 4, 3, 5, 2]
print(find_leaders(arr))  # Output: [17, 5, 2]
```

---

## 🔷 3. Star Triangle Pattern

**Q: Write a program to print a triangle star pattern.**

**Example Output (for 5 rows):**

```
    *
   ***
  *****
 *******
*********
```

**Code:**

```python
def print_star_triangle(rows):
    for i in range(rows):
        spaces = ' ' * (rows - i - 1)
        stars = '*' * (2 * i + 1)
        print(spaces + stars)

# Example
print_star_triangle(5)
```
Here are **10 essential beginner-to-intermediate level questions** from **SQL, Python, and PySpark**, complete with **answers and code** examples:

---

## 🔹 SQL – 4 Questions

### 1. **What is the difference between `WHERE` and `HAVING` clause?**

**Answer:**

* `WHERE` filters rows **before** aggregation.
* `HAVING` filters **after** aggregation.

```sql
-- WHERE filters rows before GROUP BY
SELECT department, COUNT(*) 
FROM employees
WHERE salary > 50000
GROUP BY department;

-- HAVING filters groups after aggregation
SELECT department, COUNT(*) 
FROM employees
GROUP BY department
HAVING COUNT(*) > 5;
```

---

### 2. **What is a JOIN? List different types.**

**Answer:**
A JOIN combines rows from two or more tables.

Types:

* INNER JOIN
* LEFT JOIN
* RIGHT JOIN
* FULL OUTER JOIN
* SELF JOIN
* CROSS JOIN

```sql
SELECT e.name, d.name 
FROM employee e
JOIN department d ON e.dept_id = d.id;
```

---

### 3. **What is a subquery?**

**Answer:**
A subquery is a query inside another query.

```sql
SELECT name, salary 
FROM employee 
WHERE salary > (SELECT AVG(salary) FROM employee);
```

---

### 4. **What is normalization in databases?**

**Answer:**
Normalization organizes data to reduce redundancy and improve integrity.

* 1NF: Atomic values
* 2NF: Remove partial dependencies
* 3NF: Remove transitive dependencies

---

## 🔹 Python – 4 Questions

### 5. **What are Python’s basic data types?**

**Answer:**
`int`, `float`, `str`, `bool`, `list`, `tuple`, `dict`, `set`

```python
a = 10          # int
b = "Hello"     # str
c = [1, 2, 3]   # list
```

---

### 6. **What is the difference between a list and a tuple?**

**Answer:**

* `list` is mutable: can change values
* `tuple` is immutable: can't change

```python
my_list = [1, 2, 3]
my_tuple = (1, 2, 3)
```

---

### 7. **What is a lambda function?**

**Answer:**
An anonymous function in Python.

```python
square = lambda x: x * x
print(square(5))  # Output: 25
```

---

### 8. **How do you handle exceptions in Python?**

**Answer:**
Use `try...except` block.

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Can't divide by zero!")
```

---

## 🔹 PySpark – 2 Questions

### 9. **What is PySpark?**

**Answer:**
PySpark is the Python API for Apache Spark – used for big data processing.

```python
from pyspark.sql import SparkSession
spark = SparkSession.builder.appName("Basics").getOrCreate()
```

---

### 10. **How do you read a CSV file using PySpark?**

```python
df = spark.read.csv("data.csv", header=True, inferSchema=True)
df.show()
```
Absolutely! Here's a set of **10 theoretical questions with clear and concise answers** covering **SQL, Python, and PySpark** concepts—ideal for interviews and revision.

---

## 🔹 SQL – Theory Questions

### 1. **What is a Primary Key?**

**Answer:**
A **Primary Key** uniquely identifies each row in a table. It cannot be `NULL` and must be **unique**.

---

### 2. **What is the difference between DELETE, TRUNCATE, and DROP?**

**Answer:**

* **DELETE:** Deletes selected rows, can be rolled back.
* **TRUNCATE:** Deletes all rows, cannot be rolled back.
* **DROP:** Deletes the entire table structure.

---

### 3. **What is a View in SQL?**

**Answer:**
A **View** is a virtual table based on the result of a SQL query. It does not store data physically.

```sql
CREATE VIEW high_salary AS
SELECT name, salary FROM employee WHERE salary > 50000;
```

---

### 4. **What are constraints in SQL?**

**Answer:**
Constraints enforce rules on data columns, like:

* `NOT NULL`
* `UNIQUE`
* `PRIMARY KEY`
* `FOREIGN KEY`
* `CHECK`
* `DEFAULT`

---

## 🔹 Python – Theory Questions

### 5. **What is the difference between shallow copy and deep copy?**

**Answer:**

* **Shallow copy:** Copies the reference of objects.
* **Deep copy:** Recursively copies the entire structure.

```python
import copy
a = [[1, 2], [3, 4]]
b = copy.deepcopy(a)
```

---

### 6. **What are Python decorators?**

**Answer:**
Decorators are functions that modify the behavior of other functions.

```python
def decorator(func):
    def wrapper():
        print("Before")
        func()
        print("After")
    return wrapper
```

---

### 7. **What is the difference between `is` and `==`?**

**Answer:**

* `==` checks for **value equality**.
* `is` checks for **object identity** (memory address).

```python
a = [1, 2]
b = a
print(a == b)  # True
print(a is b)  # True
```

---

## 🔹 PySpark – Theory Questions

### 8. **What is an RDD in PySpark?**

**Answer:**
RDD (Resilient Distributed Dataset) is the **core data structure** of Spark. It is immutable, distributed, and fault-tolerant.

---

### 9. **What is the difference between RDD and DataFrame?**

**Answer:**

| Feature     | RDD           | DataFrame              |
| ----------- | ------------- | ---------------------- |
| Type        | Low-level API | High-level API         |
| Performance | Slower        | Optimized via Catalyst |
| Schema      | No            | Yes                    |

---

### 10. **How does Spark achieve fault tolerance?**

**Answer:**
Using **lineage** (DAG), Spark can recompute lost data by tracking the operations used to build the dataset.

---

## 🔹 1. **DDL – Data Definition Language**

**Used to define and manage database structure (schema).**

| Command    | Description                                     |
| ---------- | ----------------------------------------------- |
| `CREATE`   | Creates a new table or database                 |
| `ALTER`    | Modifies an existing table (add/remove columns) |
| `DROP`     | Deletes a table or database                     |
| `TRUNCATE` | Deletes all rows from a table (cannot rollback) |
| `RENAME`   | Renames a table                                 |

**Example:**

```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    salary FLOAT
);
```

---

## 🔹 2. **DML – Data Manipulation Language**

**Used to manipulate data inside the tables.**

| Command  | Description                 |
| -------- | --------------------------- |
| `INSERT` | Add new records to a table  |
| `UPDATE` | Modify existing records     |
| `DELETE` | Remove records from a table |
| `SELECT` | Retrieve records            |

**Example:**

```sql
INSERT INTO employees (id, name, salary) VALUES (1, 'John', 50000);
UPDATE employees SET salary = 55000 WHERE id = 1;
DELETE FROM employees WHERE id = 1;
```

---

## 🔹 3. **DCL – Data Control Language**

**Used to control access to data (security permissions).**

| Command  | Description              |
| -------- | ------------------------ |
| `GRANT`  | Give access to users     |
| `REVOKE` | Remove access from users |

**Example:**

```sql
GRANT SELECT ON employees TO user1;
REVOKE SELECT ON employees FROM user1;
```

---

## 🔹 4. **TCL – Transaction Control Language**

**Used to manage transactions in a database.**

| Command           | Description                   |
| ----------------- | ----------------------------- |
| `COMMIT`          | Save changes permanently      |
| `ROLLBACK`        | Undo changes                  |
| `SAVEPOINT`       | Set a point to rollback to    |
| `SET TRANSACTION` | Define transaction properties |

**Example:**

```sql
BEGIN;
UPDATE employees SET salary = 60000 WHERE id = 2;
SAVEPOINT sp1;
DELETE FROM employees WHERE id = 3;
ROLLBACK TO sp1;
COMMIT;
```
