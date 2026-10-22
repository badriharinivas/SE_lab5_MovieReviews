# Lab 5: Static Code Analysis — Issue Log

## Objective

Analyze and improve the movie review application using Pylint, Bandit, and Flake8.

## Issues Identified and Fixes

| Issue | Type | Original line(s) | Description | Fix approach |
|---|---|---|---|---|
| Missing module docstring | Code quality | 1 | The module lacked a description. | Added a module docstring. |
| Non-standard naming | Code quality | 8, 11, 16, 26, 34, 39, 45, 48, 54 | Variables, functions, and parameters used inconsistent naming conventions. | Renamed functions and parameters to snake_case and removed the featured global variable. |
| Missing function docstrings | Code quality | Multiple | Functions did not explain their purpose. | Added descriptive docstrings. |
| Unnecessary else after return | Code quality | 28 | The else branch was unnecessary after a return statement. | Removed else and de-indented the remaining code. |
| Inefficient index iteration | Code quality | 50 | A range and list length were used to iterate over a list. | Replaced the loop with enumerate(). |
| Binding to all network interfaces (B104) | Security | 4 | The host configuration could expose the service on all network interfaces. | Changed the host to 127.0.0.1 for local-only binding. |
| Hardcoded password (B105) | Security | 6 | A password was embedded in the source code. | Removed the unused hardcoded password. |
| Standard pseudo-random generator (B311) | Security | 41 | random.choice was flagged for security-sensitive random selection. | Replaced it with secrets.choice. |
| Weak MD5 hash (B324) | Security | 46 | MD5 was used to generate review identifiers. | Replaced MD5 with SHA-256 while retaining a 10-character output. |
| Missing operator whitespace (E225) | Style | 35 | An operator lacked the required whitespace. | Added spaces around the operator. |
| Missing blank lines (E302) | Style | 48 | A top-level function did not have the required blank lines before it. | Corrected the spacing. |
| Inline comment spacing (E261) | Style | 70 | An inline comment lacked the required preceding spaces. | Corrected the comment spacing. |
| Missing comma whitespace (E231) | Style | 72 | A comma was not followed by a space. | Corrected the spacing. |

## Verification Results

- Initial Pylint score: 5.47/10.
- Final Pylint score: 10.00/10.
- Final Bandit scan: No issues identified.
- Final Flake8 scan: No violations reported.
- Program execution: Completed successfully.
