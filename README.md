# katalon-saucelabs-mobile

## Project Overview

This project focuses on mobile application automation testing using Katalon Studio and an Android APK file.
The project aims to validate mobile application functionality through positive and negative test scenarios. Test cases are created manually without using the Record Mobile feature.
The APK file is stored inside the Katalon project, allowing the application to be managed alongside the automation scripts.

## Objectives
- Automate mobile application testing using Katalon Studio.
- Create three test cases covering positive and negative scenarios.
- Create test steps manually without using Record Mobile.
- Store the APK file inside the Katalon project.
- Use a dynamic or project-relative APK path instead of an absolute hardcoded path.
- Execute all test cases through a Test Suite.
- Generate an execution report after the Test Suite finishes.

## Test Scenarios
The project includes positive and negative test scenarios to validate the application's behavior under different conditions.

| Test Case ID | Test Scenario | Type |
|---|---|---|
| TC001 | Verify a primary application function using valid input | Positive |
| TC002 | Verify the application handles invalid password | Negative |
| TC003 | Verify the application handles invalid username and invalid password | Negative |

## Testing Approach
### 1. Manual Test Case Creation
All mobile test cases are created manually in Katalon Studio.
The Record Mobile feature is not used. Test steps are implemented using Katalon mobile keywords, test objects, and Groovy scripts where necessary.

### 2. APK Management
The APK file is stored inside the Katalon project to keep the application file organized with the automation resources.

### 3. Dynamic and Project-Relative APK Path
A project-relative path is used to locate the APK file rather than an absolute path tied to a specific computer.

Example:

```groovy
def apkPath = RunConfiguration.getProjectDir() +
    '/Include/apk/application.apk'
```

The APK path is resolved from the Katalon project directory, making it easier to run the project on another computer without changing a machine-specific path.

### 4. Test Suite Execution
All mobile test cases are organized into a Katalon Test Suite.
The Test Suite is used to:
- Execute the mobile test cases from one place.
- Track pass and fail statuses.
- Collect execution logs and error details.
- Generate an execution report.

### 5. Execution Report
After the Test Suite finishes, Katalon Studio provides execution results containing test statuses, errors, and execution details.
The report is reviewed to evaluate test outcomes and investigate failed test cases.

## How to Run the Tests
1. Clone or download the repository.
2. Open the project in Katalon Studio.
3. Verify that the APK file exists in the project-relative location.
4. Ensure the Android device or emulator is connected and ready.
5. Verify the mobile test objects and test scripts.
6. Run the Test Suite.
7. Review the execution results and generated report.

## Limitations
- Test coverage depends on the functionality available in the APK.
- Execution may vary depending on Android versions, device configurations, and emulator settings.
- The APK must be included in the repository and available at the configured relative path.
- Actual results should be updated after the Test Suite has been executed.

## Conclusion
This project demonstrates mobile automation testing using Katalon Studio, with manually created test cases, positive and negative scenarios, project-relative APK management, and centralized Test Suite execution.
The project is designed to improve test portability, maintainability, and consistency while providing execution reports for result analysis.

## Disclaimer
This project is intended for educational and demonstration purposes only.
