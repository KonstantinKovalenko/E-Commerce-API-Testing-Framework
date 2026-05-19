# E-Commerce API Testing Framework
![CI](https://github.com/KonstantinKovalenko/E-Commerce-API-Testing-Framework/actions/workflows/api-tests.yml/badge.svg?branch=main)
## Project Overview

API automation framework for backend testing of an e-commerce system, designed as a portfolio-level QA engineering project.

The framework covers:
- API test design for core business flows
- validation of backend business logic
- CI execution via GitHub Actions
- test reporting via Newman (HTML Extra reporter)

Target API:
https://automationexercise.com/api_list

---

## CI/CD Pipeline

The project includes automated CI execution using GitHub Actions.

On every push to the `main` branch, the following steps are executed:

- Repository checkout
- Node.js environment setup
- Installation of dependencies
- Execution of Newman smoke tests
- Generation of HTML test report (Newman HTML Extra reporter)
- Upload of report as GitHub Actions artifact for download and review

This pipeline simulates a real CI workflow used in QA environments, ensuring automated validation of API functionality on every code change.

---

## Reporting

The project uses Newman with the HTML Extra reporter to generate structured API test execution reports.

Reports provide detailed visibility into test execution results, including:

- request and response data for each API call
- assertion results for validation checks
- execution timeline for performance overview
- grouping of tests by suite (Smoke / Negative / Destructive)

Reports are automatically generated during CI execution and saved as downloadable GitHub Actions artifacts for analysis and debugging.

---

## Tech Stack

- Postman
- Newman
- JavaScript
- Node.js
- HTML Extra Reporter

---

## Test Strategy

The framework is organized into three levels of API testing based on risk and system behavior.

---

### Smoke Testing

Critical end-to-end user flow validation covering the main business lifecycle:

- account creation
- login verification
- user data retrieval
- account update
- account deletion
- environment cleanup after execution (test data removal and variable reset)

This suite ensures the core API flow works as expected under normal conditions.

---

### Negative Testing

Validation of API behavior under invalid or incomplete input conditions:

- login with invalid credentials
- login with missing parameters
- account creation with missing parameters
- cleanup execution for invalid test data

This suite verifies input validation, error handling, and API robustness.

---

### Destructive Testing

Risk-based scenarios focusing on system behavior under invalid, malicious, or edge-case operations:

- account creation with invalid email formats (API accepts and creates record)
- account update with invalid data (SQL injection attempts, special characters, malformed input)
- deletion of invalid or corrupted user accounts
- API method misuse testing (unsupported HTTP methods like GET/PUT/DELETE, including 405 responses)
- cleanup after execution to reset system state

This suite is designed to expose weaknesses in validation logic and backend data handling.

---

### Project Structure

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
### Run Destructive
```
npm run destructive
```

---

## Key QA Automation Concepts Used
This project demonstrates practical QA engineering skills in API automation:

- designing API test flows based on business requirements
- validating backend behavior through positive and negative scenarios
- implementing dynamic test data generation for test independence
- structuring test suites based on risk levels (smoke / negative / destructive)
- integrating automated API tests into CI pipelines (GitHub Actions)
- analyzing test execution results via Newman reporting

---

## Project Status

Completed portfolio-level API automation project with CI integration and reporting.

---

## Author

QA Automation portfolio project created by Konstantin Kovalenko.

* GitHub: https://github.com/KonstantinKovalenko  
* LinkedIn: [www.linkedin.com/in/kostyantyn-kovalenko/](https://www.linkedin.com/in/kostyantyn-kovalenko/)
* Email: chvyaka.kk@gmail.com
* Telegram: @kovakost