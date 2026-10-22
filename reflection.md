# Lab 5: Static Code Analysis — Reflection

### 1. What is the purpose of static code analysis?

Static code analysis examines source code without executing it to identify potential bugs, security vulnerabilities, maintainability problems, and style violations. It helps improve software quality before deployment.

### 2. What did Pylint, Bandit, and Flake8 identify?

Pylint identified missing docstrings, inconsistent naming conventions, an unnecessary else branch, use of a global statement, and inefficient iteration. Bandit identified a hardcoded password, binding to all network interfaces, use of a standard pseudo-random generator, and weak MD5 hashing. Flake8 identified whitespace and blank-line violations.

### 3. How did fixing the issues improve the program?

The changes improved readability and maintainability, removed the hardcoded password, restricted the configured host to local access, replaced MD5 with SHA-256, and used a security-oriented random selection function. The rating function also validates movie existence and rating values. The existing demonstration workflow continued to execute successfully.

### 4. What did you learn from this lab?

I learned that different static analysis tools identify different classes of problems. Pylint focuses on code quality, Bandit focuses on common security weaknesses, and Flake8 checks style and formatting. Running all three tools and verifying the results helped me improve the program systematically. The Pylint score increased from 5.47/10 to 10.00/10, while the final Bandit and Flake8 scans reported no findings.
