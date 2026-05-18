# E-Commerce API Testing Framework

## Project Overview

API automation testing framework for e-commerce application backend testing using Postman, Newman, and JavaScript.

The framework covers:
- API functional testing
- end-to-end user flows
- positive and negative scenarios
- destructive testing
- dynamic test data generation
- reusable validation logic
- automated execution with Newman
- HTML reporting

This project was created as a portfolio-level API testing framework focused on backend QA automation practices.

Target API:
https://automationexercise.com/api_list

---

## Tech Stack

- Postman
- Newman
- JavaScript
- Node.js
- HTML Extra Reporter

---

## Features

### API Flow Testing
Implemented complete user lifecycle scenarios:

- Create account
- Verify login
- Get user details
- Update account
- Delete account

---

### Dynamic Test Data
The framework automatically generates:
- usernames
- emails
- passwords
- runtime user data

This allows repeatable and independent test execution without hardcoded credentials.

---

### Validation Layer
Implemented validations for:
- HTTP status codes
- API response codes
- response messages
- response time
- required fields
- data types
- business logic consistency

---

### Negative Testing
Implemented negative scenarios for:
- invalid credentials
- malformed payloads
- SQL injection-like inputs
- script injection payloads
- invalid request data

---

### Destructive Testing
Separate destructive test suite created for:
- risky operations
- invalid account manipulation
- cleanup-related scenarios

---

### Cleanup Strategy
The framework includes automatic runtime data cleanup:
- created test users are deleted after execution
- runtime environment variables are cleared automatically

---

## Project Structure

```text
E-Commerce-API-Testing-Framework/
│
├── collections/
├── environments/
├── postman/
├── reports/
│
├── package.json
└── README.md
```
---
## Test Suites
### Smoke

Critical end-to-end user flow validation.

### Negative

Validation of invalid input handling and unexpected data.

### Destructive

Risky and system-affecting scenarios separated from regular execution.

---

## Running Tests
### Install dependencies
```
npm install
```
### Run Smoke Tests
```
npm run smoke
```
### Run Negative Tests
```
npm run negative
```
### Run Clean up variables
```
npm run utils
```

---

## Reporting

The project uses Newman HTML Extra Reporter for detailed execution reports.

Generated reports include:

- passed/failed tests
- request details
- response information
- execution statistics

---

## Key QA Automation Concepts Used
- API automation
- reusable test architecture
- runtime data generation
- environment management
- response validation
- cleanup strategy
- destructive testing separation
- Newman CLI execution

---

## Author

QA Automation portfolio project created by Konstantin Kovalenko.

* GitHub: https://github.com/KonstantinKovalenko  
* LinkedIn: [www.linkedin.com/in/kostyantyn-kovalenko/](https://www.linkedin.com/in/kostyantyn-kovalenko/)
* Email: chvyaka.kk@gmail.com
* Telegram: @kovakost