# ParthBlog – Manual Test Cases

This folder contains the Excel workbook documenting the manual test cases for the ParthBlog project.

The test cases are derived from the Functional Requirements Specification and cover positive scenarios, negative scenarios, and meaningful validation checks. The objective is to maintain practical test coverage without unnecessary duplication.

## Test Case Coverage

| Requirement ID | Requirement | Status |
|---|---|---|
| REQ-01 | User Registration (Sign Up) | Documented |
| REQ-02 | User Login | Documented |
| REQ-03 | Forgot Password & Reset Password | Documented |
| REQ-04 | Welcome Screen (Guest User) | Documented |
| REQ-04 | Home Screen (Authenticated User) | Documented |
| REQ-05 | Main Blogs Feed | Documented |
| REQ-05 | Individual Blog Page | Documented |
| REQ-06 | Create Blog | Documented |
| REQ-07 | Edit Blog | Documented |
| REQ-08 | Delete Blog | Documented |
| REQ-09 | Customize Profile | Documented |
| REQ-09 | Edit Profile | Documented |
| REQ-10 | Contact Us | Documented |
| REQ-11 | FAQs | Documented |

**Note:** These statuses refer to test-case documentation and review, not test execution. ParthBlog is a fictional portfolio project, and a working website is not currently available for execution.

## Excel Workbook Structure

The workbook contains separate worksheets for the different features and user workflows. Related functionality may share a worksheet when it is available on the same screen.

The worksheets are arranged in user-journey order, starting with the Welcome Screen and authentication, followed by the main website pages, blog management, profile management, and general website functionality.

The workbook uses the following columns:

1. Test Case ID
2. Test Scenario
3. Test Steps
4. Test Data
5. Expected Result
6. Actual Result
7. Status

## Testing Approach

- Cover important positive and negative scenarios.
- Include meaningful boundary and input-validation checks.
- Avoid redundant test cases and unnecessary field-by-field validation.
- Base expected results on the documented functional requirements and established design decisions.
- Avoid inventing functionality or expected behavior that has not been specified.
- Review test cases for mistakes, consistency, and meaningful coverage.

## Execution Status

The test cases have been documented and reviewed but have not been executed against a live application.

Actual Result will remain blank and Status will remain `Not Started` until test execution becomes possible.

## Version History

| Version | Date | Changes |
|---|---|---|
| 1.0 | 14-10-2026 | Initial documentation of ParthBlog manual test cases. |
| 1.1 | 14-10-2026 | Added and reviewed test cases for User Registration, User Login, Forgot Password, Reset Password, and FAQs. Refined test data, expected results, and scenario coverage. |
| 1.2 | 15-10-2026 | Added and reviewed test cases for the Welcome Screen, authenticated Home Screen, Individual Blog Page, and Contact Us. Refined expected results and focused on practical, non-exhaustive coverage. |
| 1.3 | 19-10-2026 | Added and reviewed test cases for the Main Blogs Feed, Create Blog, and Edit Blog. Refined validation scenarios, expected results, and test data. |
| 1.4 | 21-10-2026 | Added and reviewed test cases for Publish Blog, Delete Blog, Customize Profile, and Edit Profile. Organized the Excel worksheets into user-journey order. |

## Future Updates

The documentation and version history will be updated when meaningful changes are made to the test cases, requirements, or workbook structure.
