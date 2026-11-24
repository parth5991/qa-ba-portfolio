# ParthBlog – Manual Test Cases

This folder contains the Excel workbook documenting the manual test cases for the ParthBlog project.

The test cases are derived from the Functional Requirements Specification and cover positive scenarios, negative scenarios, and meaningful validation checks. The objective is to maintain practical test coverage without unnecessary duplication.

**Latest Workbook:** `ParthBlog_TestCases_All_v1.5.xlsx`

**Total Test Cases:** 202

**Total Worksheets:** 15

## Test Case Coverage

The manual test cases cover all 11 functional requirements defined in the ParthBlog Functional Requirements Specification.

| Requirement ID | Requirement | Total Test Cases | Coverage Status |
|---|---|---:|---|
| REQ-01 | User Registration (Sign Up) | 14 | Covered |
| REQ-02 | User Login | 11 | Covered |
| REQ-03 | Forgot Password & Reset Password | 12 | Covered |
| REQ-04 | Home Page (Guest User and Authenticated User) | 24 | Covered |
| REQ-05 | Blogs (Main Blogs Feed and Individual Blog Page) | 53 | Covered |
| REQ-06 | Create Blog | 20 | Covered |
| REQ-07 | Edit Blog | 18 | Covered |
| REQ-08 | Delete Blog | 3 | Covered |
| REQ-09 | Customize Profile and Edit Profile | 36 | Covered |
| REQ-10 | Contact Us | 7 | Covered |
| REQ-11 | FAQs | 4 | Covered |
| **Total** | | **202** | **100% Covered** |

**Note:** Coverage Status indicates whether the documented test cases provide coverage for the corresponding requirements. It does not represent test execution results. ParthBlog is a fictional portfolio project, and a working website is not currently available for execution.

## Excel Workbook Structure

The workbook contains 15 separate worksheets for different features and user workflows. Related functionality may share a worksheet when it is available on the same screen.

The worksheets are arranged in user-journey order, starting with the Welcome Screen and authentication, followed by the main website pages, blog management, profile management, and general website functionality.

The workbook uses the following columns:

1. Test Case ID
2. Test Scenario
3. Test Steps
4. Test Data
5. Expected Result
6. Actual Result
7. Status

## Requirements Traceability Matrix (RTM)

A separate Requirements Traceability Matrix is maintained as part of the ParthBlog project documentation.

The RTM provides a requirement-level summary of test coverage, including:

- Requirement ID
- Module / Feature
- Requirement Summary
- Total Test Cases
- Coverage Status

The matrix provides an overview of coverage across all 11 functional requirements. Individual test case details remain documented in the Excel workbook.

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
| 1.5 | 24-11-2026 | Reviewed test coverage across all 11 functional requirements. Refined test cases for publisher profiles, blog management, profile validation, deletion confirmation, and other functional areas. Finalized the requirement-level RTM summary. Updated workbook to 202 test cases across 15 worksheets. |

## Future Updates

The documentation and version history will be updated when meaningful changes are made to the test cases, requirements, or workbook structure.
