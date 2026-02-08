# Swagger.io petstore public API Test Plan

## 1. Introduction
- The purpose of this test plan is to define the scope, objectives, and test resources for testing the Swagger.io petstore public API.
- The goal of testing is to verify that the functionality of public API works correctly. To observe API behavior on different requests. 
- Testing covers testing of Swagger petstore public API (Functional, Negative, End-to-End testing). Using of Postman for executing test and flow/auto tests. Jira for planing and controling of tests and bugs.
- The expected result are shown in Swagger pet store documentation. 

---

## 2. Test Objectives
- Verify API responses with positive testing using method GET, POST, PUT, DELETE.
- Verify API responses with negative testing using method GET, POST, PUT, DELETE.
- Working with API using requests in Postman.
- Creating, updating and deleting of pets in different ways using form-data, JSON, raw data.
- Making Flow tests in Postman, using scripts for autotests.
- Jira tracker for handling of test cases and bug reports 

---

## 3. Scope

### In Scope

- Functional, negative, network, and end-to-end testing of Swagger Petstore public REST API (Pet, User, Store endpoints)
- Validation of HTTP methods (GET, POST, PUT, DELETE)
- Manual and automated testing using Postman collections

### Out of Scope

- UI testing
- Performance/load testing
- Database and source code testing

---

## 4. Test Approach
- Manual functional and non-functional testing.
- Flow tests and auto tests with Postman application 
- Negative testing to simulate API behavior on unexpected results. 

---

## 5. Test Types
- **Functional Testing**
- **Network Testing**: Handling of server errors (e.g., 404, 500).
- **Negative Testing**: Invalid input data.
- **End-to-End Testing**: Create and delete a pet, try to GET deleted pet. 
- **Regression Testing** (re-running flows after changes)

---

## 6. Test Environment
- PC: Windows 10 or higher
- Tools: Postman, Jira
- Network: Wi-Fi
- External Services: Chrome browser, Notepad 

---

## 7. Entry Criteria
- PC is available.
- Postman is installed on the PC.
- Jira account is available. 
- Stable Wi-Fi connection is available.

---

## 8. Exit Criteria
- All planned test cases are executed or canceled. 
- Test documentation and screenshots are prepared.
- All identified defects are documented and reported.

---

## 9. Risks
- Possible differences in different Postman application versions
- Public API Swagger could be updated or closed. 
- Problems with internet connection and access to public API.

