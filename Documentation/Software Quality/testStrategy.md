# Test Strategy Document

## 1. Introduction
- **Project Name**: MTOGO Exam project 2024
- **Overview**: MTOGO is an online food ordering and delivery platform. MTOGO connects with a broad range of local restaurants, so you can have your favorite food delivered to your doorstep.
- **Test Objectives**:
	- 	Ensure that all features of the app functions as intended without any critical defects.
	- Verify that the app meets all performance and security requirements.
	- Ensure a bug-free user experience.

## 2. Scope
- **In Scope**: 
	- Core functionalities, including user interactions, backend logic, and API integrations, will be tested to ensure business-critical processes work seamlessly.

For specifics, refer to the detailed **Test Plan**.
- **Out of Scope**: 
	- Third-party payment service integration.
	- Frontend testing

## 3. Testing Approach
- **Testing Levels**: 
	- Unit tests for individual modules like order processing, user accounts, and delivery agent management.
	- Integration tests for verifying interactions between the restaurant, delivery, and mocked payment services.
	- System tests for the overall functionality of the food ordering and delivery process.
	- Acceptance tests that ensure the system meets the requirements for handling various order workflows.
- **Types of Testing**:
	- Functional testing to verify features align with the requirements.
	- Regression testing to make sure new development doesn’t negatively affect the overall functionality.
	- Performance testing to ensure the system scales and performs in terms of responsiveness and stability under different workloads.
- **Test Design Techniques**: 

	To ensure thorough testing, we use two key techniques:
	- Grouping Similar Inputs: We group inputs into categories that are expected to behave the same way. 
	- Testing Boundaries: We focus on testing the smallest and largest numbers allowed and just outside the allowed range. 
	- A mix of manual and automated testing will be employed to balance thoroughness and efficiency. The approach aligns with the project’s iterative development process, emphasizing continuous testing and feedback.

   These techniques help us cover more scenarios with fewer tests and increase the chances of finding bugs in critical areas.

## 4. Test Environment

**Expected Environment Configuration**:
- **Operating System**:  
  Windows-based system to ensure compatibility with deployment targets and for backend compatibility.

- **Database**:  
  A database instance is expected to simulate production data interactions, supporting tests for data integrity, CRUD operations, and handling real-world data scenarios.

- **CI/CD Integration**:  
  The test environment should integrate seamlessly with CI/CD pipelines to allow for automated testing and deployment validation, ensuring efficient feedback loops and release-readiness.

## 5. Test Tools

**Expected Tool Configuration**:
Tools will be selected based on their ability to support efficient and scalable testing for unit, integration and performance needs. Specific tool decisions will be made in alignment with project goals and is as follows:
- **Testing Framework**:  
  XUnit is expected to be used as the primary testing framework, supporting structured and consistent test execution.

- **Performance Testing Tools**:  
  JMeter is anticipated for performance and load testing, providing insights into system responsiveness under various loads.

- **Defect Tracking**:  
  Qodana and SonarQube are expected to facilitate defect tracking and management, ensuring that issues are identified and documented efficiently.

- **Coverage Reporting**:  
  Coverage tools such as Coverlet and dotCover will be used to generate detailed test coverage reports, supporting thorough evaluation of code coverage across test cases.

## 6. Test Schedule
Testing will follow an iterative cycle aligned with the development timeline, ensuring continuous verification and validation. These come in the form of phases:
- **Phases**: 
	- Test planning: 1 week, during the preparation phase.
	- Test execution: Will be an ongoing integration with development for the entirety of the project's lifetime.

## 7. System Test Entry and Exit Criteria

- **Entry Criteria**:  
	- Code Completion: All features and functions must be implemented, and the code is "frozen" (no new changes except for bug fixes).
	- Basic Functionality Verified: Core functionality, such as user registration, ordering, and database connectivity, should work without major defects.

- **Exit Criteria**:  
	 - All Tests Executed: All system test cases, including functional, non-functional, and regression tests, must be completed.
	 - Critical Issues Resolved: All "showstopper" or critical defects have been fixed. Major and minor defects should remain below a defined threshold (e.g., no more than 5 major bugs and 10 minor bugs).
	- Build Stability: The system must generate stable, deployable builds consistently, indicating readiness for production.

## 8. Risk Management
- **Potential Risks**: 
	- Tight deadlines may impact thoroughness.
	- Dependencies on external systems, such as third-party APIs.

## 9. Deliverables
- **Test Strategy**: The high-level test strategy (this document).
- **Test Cases**: The documented test cases.
- **Test Coverage Report**: A report of the percentage of features and code covered by the tests.

## 10. Metrics for Evaluation
- **Key Metrics** to evaluate testing effectiveness:
 	- Defect Density: Number of defects per module.
- Test Coverage: Percentage of coverage against planned test cases.
 	- Pass/Fail Rate: Success rate of executed test cases.

## 11. Approval
- **Approval**: Approval from all team members to ensure alignment with the project’s testing goals:
	- Caroline Lærke Høg Rendtorff
	- Helena Botn Lykstoft
	- Jamie Grønbæk Callan
	- Markus Isak Møgelvang
