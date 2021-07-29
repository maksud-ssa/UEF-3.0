# Master Test Plan for User Experience Framework (UEF 3.0)
#### RASCODE: XXXX
#### PRISM ID: XXXX
#### PROJECT TYPE: DEVELOPMENT.
#### DATE: July 26, 2021.

# Table of Content

 1. Introduction
 2. Test Items and their Features/Functions to Test or Exclude
 3. Approach/Strategy
 4. Item Pass/Fail Criteria
 5. Suspension Criteria and Resumption Requirements
 6. Test Deliverables
 7. Remaining Test Tasks
 8. Test Environments
 9. Responsibilities
 10. Staffing and Training Needs
 11. Proposed Schedule for Testing
 12. Risks and Contingencies
 13. Change History
 14. Addendum A - Testing Organizations/Responsibilities
 15. Addendum B – Testing Approach
 16. Addendum C – Test Boundaries Diagram


## DETAIL DESCRIPTION
## I. Introduction
This document describes the approach and methodologies used by the DCS/DIACS/UXG to plan, organize and manage the testing of **User Experience Framework (UEF)** Release **3.0.** It does not describe implementation details of test cases or technical details of how the product features should work.
However the team consensus was:

 - All testing will be aggregated through Storybook
 - Puppeteer will be utilized under the hood through Stencil.js

 *The structure of this document is primarily based on IEEE 829-1998 Standard for Software Test Documentation.*

## II. Test Items and their Features/Functions to Test or Exclude

UEF 3.0 is a collection of W3C standard Web Components that were created to support the SSA Design System. Based on how the components are developed we have come up with the following test requirements.

- **Unit Testing**
	 - Each individual component codes will be tested for its functionality & attributes.
	 - Jest will be used in common story format.
		 - Implement Jest in Storybook - *Mark.*
#### **A.** Test Item 1 (i.e. Please include items to be tested in Unit Test)
| Functions/Features to Test | Tool/Technique  | Level of Risk (H,M,L) |
|--|--|--|
|Individual Functionality | Jest | High |
|Component Attributes |Manual Testing| High |
|-- |--| |

| **Functions/Features to Exclude** |Level of Risk (H,M,L)  |
|--|--|
|- List item |Add Item|
|- List item |Add Item|
|- List item |Add Item|
|-- |--|

- **Automated Accessibility Testing**
We will conduct Automated Accessibility Testing to ensure that all our components are  tested before we apply for a formal 508 compliance certificate from ASB, to detect most common defects earlier in the development phase.

#### **B. Test Item 2 (i.e. Please include items to be tested in Automated Accessibility Test)**

| Functions/Features to Test |Tool/Technique| Level of Risk (H,M,L)  |
|--|--|--|
|Color contrast | aXe| High |
|HTML elements | aXe| High 	|
|Semantics|--|--|
|--|--|--|

- **Integration Test**
All components in UEF 3.0 will go through a System Integration Testing to verify the behavior of the complete system. We will conducted on a complete, integrated system to evaluate the system's compliance with its specified requirement.

#### **C.** Test Item 3 (i.e. Please include items to be tested in Integration Test)
|Functions/Features to Test | Tool/Technique  | Level of Risk (H,M,L) |
|--|--|--|
|Framework Integration test. (Does our stuff work in Angular/React/etc.?)|List Item| High |
|Component Integration - If there are components that passes its values to another component, those are the ones should be categorized for integration testing.| Add item | High|
|Architectural Integration |Add Item | High |


- **Visual Testing**
UEF will perform a Visual testing for comparing visible output of all our components against a baseline image. In its most basic form, visual testing, sometimes referred to as snapshot testing compares differences in an image by looking at pixel variations.

#### D. Test Item 4 (i.e. Please include items to be tested in Visual Testing)
| Functions/Features to Test| Tool/Technique  | Level of Risk (H,M,L) |
|--|--|--|
|Visual Differences | Storybook--Jest--Puppeteer | Medium |
|--|--|--|

- **Visual Regression Testing**
After every new build all UEF 3.0 baselined components will go through a regression test to ensure that the new build did not have any adverse effect on the existing components.

| Functions/Features to Test | Tool/Technique | Level of Risk (H,M,L) |
|--|--|--|
|Visual Differences | Storybook--Jest--Puppeteer | High |

#### E. Test Item 5 (i.e. Please include items to be tested in Visual Regression Testing)
| **Functions/Features to Test** | Tool/Technique  | Level of Risk (H,M,L) |
|--|--|--|
|- List item |List Item| |

- **End-to-end Test**
	 - End-to-end test will be performed to ensure that the deployment of the components in production are working as per requirements. The followings are suggested for testing using the Puppeteer tool.


#### F. Test Item 6 (i.e. Please include items to be tested in End-to-End Testing)

| Functions/Features to Test | Tool/Technique  | Level of Risk (H,M,L) |
| --|--|--|
|Testing the workflows |--|--|
| Complex and Compound patterns | | |
| Interaction Section on Standards Website | | |
|-- |-- | -- |

## III. Approach/Strategy
Through the coordination of internal testing and validation components, testing will be conducted to ensure each individual components functionality as well as interoperability will achieve the desired outcome.  The strategy for testing includes the use of automated test libraries, built in functions and exploratory testing.

Basic metrics will be kept for Test Effort, Test Cases Executed and Defects.

See Addendum B.

## IV. Item Pass/Fail Criteria
Manual & Automated test scripting will determine the pass/fail criteria.  Should a case fail processing or not achieve the desired results, the exit criteria will be documented and an error description added to the test case.

See Addendum B.

## V. Suspension Criteria and Resumption Requirements

Environmental & Server issues may cause suspension of testing activities. Test can resume when the environment is stable and restored. Testing results that fail to meet the pass criteria will cause suspension of testing where subsequent pass criteria is dependent on successful completion of initial test criteria.

## VI. Test Deliverables

- Master Test Plan
- Validation Plan
- Test Case/Data Creation
- Defect tracking reports – Pick a tool.
- Manual test scripts & test data to support the manual test scripts
- Automate the selected stable test cases for regression

## VII. Remaining Test Tasks

Regression testing will be conducted after every production build

## VIII. Test Environments
- DEV - For development activities & Unit testing.
- VAL - For Validation Team
- PROD - To test code in production

**Available Testing Tools**

| Objective | Tool   | Objective |
|--|--|--|--|
| Documentation of test cases and results | Jira | For creating, tracking, managing test cases & defects and overall project management  |
| Unit Test Creation & Execution | Jest | To perform Unit Test Creation/Execution |
| End To End Test Creation & Execution | Puppeteer | To automate e-2-e testing & Regression test suite execution |
| Automated Accessibility Testing | aXe | To identify proper color contrast & html attributes  |

## IX. Responsibilities
| Task | Responsible Person | Component |
|--|--|--|
| Test Creations |  |  |
| Automated Test Creation |  |  |
| Test Execution |  |  |

## X. Staffing and Training Needs
- Basic understanding of Testing and Validation.
- Basic  understanding of the functionalities of User Experience Framework.
- Basic understanding and grasp of identifying the requirements/Use cases/Business rules from the Requirements and Design Document.
- Basic understanding of defects management & lifecycle process.
- The validation staff is trained and has proper understanding of the following testing tools.
	- Jest Automated Testing Process
	- Puppeteer Automated Testing Process
	- Microsoft Office Tools
	- aXe automation tool
	- Basic web development process
	- Basics of Angular testing
	- Basics of REACT testing

## XI. Proposed Schedule for Testing
Note: We will follow Kanban method to develop UEF 3.0 and therefore we will start testing as soon as the development begins.

| Activity| Start | End |
|--|--|--|
| Test Planning |  |  |
| Development |  |  |
| Unit Test |  |  |
| Integration Test |  |  |
| End-to-End Test |  |  |

## XII. Risks and Contingencies
| Activity| Start | End |
|--|--|--|
|  |  |  |
|  |  |  |
|  |  |  |

## Change History
| Version| Date | Changes |
|--|--|--|
| V0.1 | April 13, 2021 | Created the Template. |
| V0.2 | April 22, 2021 | Updated based on the first team review. |
| V0.3 | May 21, 2021 | Created the first (MD) version. |
| V0.4 | Jul 21, 2021 | Updated the MD content. |
| V0.5 | Jul 26, 2021 | Updated the content. |
