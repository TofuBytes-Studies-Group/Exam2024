# Test Plan Document

## 1. Introduction
- **Project Name**: MTOGO Exam project 2024
- **Test Objectives**: 
	- Validate all order functions, ensuring correctness and alignment with requirements.
- Very the accuracy of customer registration functions
	- Ensure end-user usability is intuitive and meets accessibility standards.
	- Confirm security controls prevent unauthorizedaccess
	- Validate the correctness of order and bonus calculations
	- Ensure all integration points within the system and external systems (e.g., mocking of payment service) work as intended.

## 2. Scope 
- **In Scope**: 
	- User features:
-  Restaurant search, cart functionality, user registration, login, ordering and review creation.
	- Backend logic:
- Bonus calculation for delivery agents.
   	 - Database operations:
- CRUD operations for PostgreSQL and MongoDB
	- API endpoints and integrations:
- Endpoints facilitating user and order-related processes, including integrations with the mock payment service
- **Out of Scope**: 
	- Payment services:
- Will be external and not implemented at this time (besides mocking for testing).
	- Frontend testing:
		- Limited to API responses and UI-rendered data consistency.


## 3. Testing Approach
- **Testing Levels**: 
    - Unit tests:
- Validate modules such as order processing, user management, and bonus calculations.
    - Integration tests:
- Verify interactions between subsystems, including the restaurant, delivery services, and mocked payment services.
    - System tests: 
- Assess the end-to-end functionality, including workflows for placing and completing orders.
    - Acceptance tests:
-  Ensure the system meets the requirements for handling various order workflows (e.g., customer reviews, bonuses for delivery agents).

- **Types of Testing**:
	- Functional testing:
- Validate feature behavior against specifications.
	- Regression testing:
- Ensure updates do not break existing functionality
	- Performance testing:
- Measure response timers and stability under load using tools like JMeter.

- **Test Design Techniques**: 
	- Boundary value analysis
- Test edge conditions (e.g., max/min values for input fields).
	- Equivalence Partitioning:
		- Group similar input data for streamlined validation
	- Mocking.
		- simulate external dependencies such as the payment service
	- Mutation tests:
		- Assess test robustness by introducing code mutations.


## 4. Test Environment
- **Environment Overview**: 
    - Hardware: Windows 11 & 11 Pro, Ubuntu 22.04 & 24.04 LTS
	- Samsung Galaxy Book Pro NP950XDB
	11th Gen Intel(R) Core(TM) i7-1165G7 @ 2.80GHz   2.80 GHz
	16 GB RAM
	500 GB Storage

	- LENOVO MT 83EQ BU idea FM IdeaPad Slim 3 14IAH8
12th Gen Intel(R) Core(TM) i5-12450H, 2000 Mhz, 8 Core(s), 12 Logical Processor(s)
16 GB RAM
1 TB Storage

	- VivoBook ASUS Laptop X432FLC S432FL
Intel(R) Core(TM) i7-10510U CPU @ 1.80GHz, 2304 Mhz, 4 Core(s), 8 Logical processor(er)
	16 GB RAM
	500 GB Storage

	- Lenovo Yoga Slim 7 Pro 14ACH5
AMD Ryzen 7 5800H with Radeon Graphics, 3201 Mhz, 8 Core(s), 16 Logical Processor(s)
	16 GB RAM DDR4
	500 GB Storage





    - Software: Google Chrome
    - Network config: WiFi and Ethernet connections
    - Database: Redis, PostgreSQL, MongoDB
    - CI/CD integration: GitHub Actions
    - Server: 
	Docker CLI/Desktop 
	Docker Swarm
	Ubuntu Linux Operating System
	

- **Browser**:  
  Google Chrome will be the primary browser for testing, with the expectation that all functionalities perform consistently and efficiently.



## 5. Test Tools
- **Tool Types**: 
  	- Framework: XUnit as the testing framework.
  	- Performance Testing Tools: JMeter for performance and load testing.
  	- Defect Tracking: Qodana, SonarQube for tracking and managing defects.
	- Coverage Report: Coverlet, dotCover for making test coverage reports. 
- Details on how each tool will be used for specific tests will be covered in the Test Plan.


## 6. Test Schedule
- **Phases**: 
	- Test planning: Duration of 1 week, during the preparation phase.
	- Test execution: Ongoing throughout the project, focusing on TDD and iterative testing.



## 7. System Test Entry and Exit Criteria
- **Entry Criteria**:  
  - Unit and Integration Tests Passed: All unit and integration tests must pass without critical defects.
  - Test Data: Mocks and relevant infrastructure must be prepared.

- **Exit Criteria**:
- All critical workflows validated.
  - Successful End-to-End Testing: 
- Key business workflows or critical user journeys (e.g., user registration, ordering) must be validated successfully.
  - Test Report Generation: 
- Test reports, including defect logs, test execution status, and performance results, should be completed and available.


## 8. Risk Management
- **Potential Risks**: 
	- Tight deadlines impacting test coverage and thoroughness.
- Dependencies on external services (e.g., payment service)
- Environmental inconsistencies during CI/CD deployments.


## 9. Deliverables- **Test Plan**: A comprehensive plan covering detailed test cases, schedules, and resources.
- **Test Cases**: The documented test cases.
- **Test Coverage Report**: A report of the percentage of features and code covered by the tests.
-**Test Analysis*: Defect logs and performance analysis.



## 10. Metrics for Evaluation
- **Key Metrics** to evaluate testing effectiveness:
 	- Defect Density: Number of defects per module.
	- Test Coverage: Percentage of coverage against planned test cases.
	- Target 70%+ coverage for unit and integration tests.
- Pass/Fail Rate:
-Success rate of executed test cases.



## 11. Approval
- **Approval**: Approval from all team members to ensure alignment with the project’s testing goals:
	- Caroline Lærke Høg Rendtorff
	- Helena Botn Lykstoft
    	- Jamie Grønbæk Callan
    	- Markus Isak Møgelvang
