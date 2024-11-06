# Test Strategy Document


## 1. Introduction
- **Project Name**: MTOGO Exam project 2024
- **Overview**: MTOGO is an online food ordering and delivery platform. MTOGO connects with a broad range of local restaurants, so you can have your favorite food delivered to your doorstep.
- **Test Objectives**: 
    - Ensure that all features of the app functions as intended without any critical defects.
    - Verify that the app meets all performance and security requirements.
    - Ensure a bug-free user experience.



## 2. Scope
- **In Scope**: 
	- User features; such as restaurant search, cart functionality, user registration, user login, ordering, and review creation.
	- Backend logic; such as bonuses for delivery agents.
    - Database operations.
	- API endpoints and integrations.
- For specifics, refer to the detailed **Test Plan**.
- **Out of Scope**: 
	- Payment services will be external and not implemented at this time
	- Frontend testing


## 3. Testing Approach
- **Testing Levels**: 
    - Unit tests for individual modules like order processing, user accounts, and delivery agent management.
    - Integration tests for verifying interactions between the restaurant, delivery, and mocked payment services.
    - System tests for the overall functionality of the food ordering and delivery process.
    - Acceptance tests that ensure the system meets the requirements for handling various order workflows (e.g., customer reviews, bonuses for delivery agents).
- **Types of Testing**:
	- Functional testing to know if the features work according to the requirements.
	- Regression testing to make sure new development doesn’t negatively affect the overall functionality.
	- Performance testing to see how the system performs in terms of responsiveness and stability under different workloads.
- **Test Design Techniques**: 
	- Boundary value analysis and equivalence partitioning
	- Mocking 
	- Mutation tests


## 4. Test Environment
- **Environment Overview**: 
    - Hardware: Windows 11, Ubuntu 22.04 & 24.04 LTS
    - Software: Google Chrome
    - Network config: WiFi and Ethernet connections
    - Database: Redis, PostgreSQL, MongoDB
    - CI/CD integration: GitHub Actions


## 5. Test Tools
- **Tool Types**: 
  	- Framework: XUnit as the testing framework.
  	- Performance Testing Tools: JMeter for performance and load testing.
  	- Defect Tracking: Qodana, SonarQube for tracking and managing defects.
	- Coverage Report: Coverlet, dotCover for making test coverage reports. 
- Details on how each tool will be used for specific tests will be covered in the Test Plan.


## 6. Test Schedule
- **Phases**: 
	- Test planning: 1 week, during the preparation phase.
	- Test execution: Over the span of the entire project, we will work with a test-first strategy (TDD) and use regression testing.


## 7. System Test Entry and Exit Criteria
- **Entry Criteria**: 
	- Code Completion: All features and functions have been developed and implemented, and the code is "frozen" (no new changes except for bug fixes).
    - Unit and Integration Tests Passed: All unit and integration tests must have been executed successfully without any critical issues.
    - Basic Functionality Verified: Key functionality; such as user registration, ordering, order processing, or database connections, should work without major defects.
    - Test Data Prepared: Required test data, mock systems, and test cases are ready and available for execution.
- **Exit Criteria**: 
	- All Tests Executed: All system test cases, including functional, non-functional, and regression tests, have been executed.
    - Critical Issues Resolved: All "showstopper" or critical defects have been fixed. The remaining major and minor defects fall below an agreed-upon threshold (e.g., no more than 5 major bugs and 10 minor bugs).
    - Successful End-to-End Testing: Key business workflows or critical user journeys (e.g., user registration, ordering) have been successfully validated.
    - Test Report Generation: Test reports, including defect logs, test execution status, and performance results.
    - Build Stability: The system can generate stable and deployable builds.


## 8. Risk Management
- **Potential Risks**: 
	- The exam deadline.


## 9. Deliverables
- **Test Strategy**: The high-level approach to testing (this document).
- **Test Plan**: A comprehensive plan covering detailed test cases, schedules, and resources.
- **Test Cases**: The documented test cases.
- **Test Coverage Report**: A report of the percentage of features and code covered by the tests.


## 10. Metrics for Evaluation
- **Key Metrics** to evaluate testing effectiveness:
 	- Defect Density: Number of defects per module.
    - Test Coverage: Percentage of coverage against planned test cases.
 	- Pass/Fail Rate: Success rate of executed test cases.


## 11. Approval
- **Approval**: Who must review and approve this Test Strategy document:
	- Caroline Lærke Høg Rendtorff
	- Helena Botn Lykstoft
    - Jamie Grønbæk Callan
    - Markus Isak Møgelvang




