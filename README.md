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
- Generation of HTML test report (htmlextra)
- Upload of test report as GitHub Actions artifact

This pipeline simulates a real CI workflow used in QA environments, ensuring automated validation of API functionality on every code change.

---

## Reporting

Test execution reports are generated using Newman with the HTML Extra reporter.

Reports include:
- request/response details
- assertion results
- execution timeline

Reports are automatically generated in CI and stored as GitHub Actions artifacts.

---

## Tech Stack

- Postman
- Newman
- JavaScript
- Node.js
- HTML Extra Reporter

---

## Test Strategy

The framework includes three levels of testing:

### Smoke Testing
Critical end-to-end API flows:
- account creation
- login verification
- user data retrieval
- account update
- account deletion

### Negative Testing
Validation of invalid inputs and error handling:
- invalid credentials
- malformed requests
- injection attempts
- invalid data formats

### Destructive Testing
Risk-based scenarios affecting system state:
- account deletion
- invalid account operations
- cleanup validation

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