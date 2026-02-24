# SMART TEST CASE GENERATOR -- SPEC (FINAL VERSION)

------------------------------------------------------------------------

## 1. Overview

### 1.1 Purpose

Smart Test Case Generator is an AI Skill designed to transform a
functional product specification (.md file) into structured,
high-coverage, risk-aware test cases.

The skill focuses on:

-   Functional test case generation
-   Edge & negative case detection
-   Ambiguity identification
-   Priority assignment
-   Structured output standardization

This skill is a productivity amplifier for QC, not a replacement for QA
judgment.

------------------------------------------------------------------------

## 2. Problem Statement

Manual test case writing:

-   Is time-consuming
-   Depends heavily on individual experience
-   Often misses edge cases
-   Produces inconsistent formats
-   Rarely challenges ambiguous specifications

The goal of this skill is to:

-   Reduce test case writing time by 5--10x
-   Increase structured coverage
-   Standardize QA output
-   Improve spec review quality

------------------------------------------------------------------------

## 3. Input Definition

### 3.1 Accepted Input

-   Functional product specification in Markdown (.md)
-   May include:
    -   Feature description
    -   Business rules
    -   User flow
    -   Validation rules
    -   System behavior

### 3.2 Assumptions

-   Spec is logically structured
-   Spec is readable
-   If incomplete or ambiguous, skill will detect and flag issues before
    generation

------------------------------------------------------------------------

## 4. Output Definition

The skill produces 5 structured layers:

1.  Requirement Analysis
2.  Ambiguity & Risk Detection
3.  Test Scenarios
4.  Detailed Test Cases
5.  Coverage Summary

------------------------------------------------------------------------

### 4.1 Detailed Test Case Structure

Each test case includes:

-   Test Case ID
-   Requirement Reference
-   Title
-   Precondition
-   Test Steps (atomic and numbered)
-   Test Data
-   Expected Result (clear and measurable)
-   Priority (Critical / Major / Minor)
-   Test Type (Functional / Validation / Edge / Negative)

------------------------------------------------------------------------

## 5. Core Logic Framework

The skill applies structured test design techniques:

### 5.1 Boundary Value Analysis

-   Minimum
-   Maximum
-   Just below
-   Just above

### 5.2 Equivalence Partitioning

-   Valid input group
-   Invalid input group

### 5.3 Negative Testing

-   Invalid inputs
-   Empty inputs
-   Null values
-   Special characters

### 5.4 Risk-Based Testing

High-risk scenarios include: - Authentication / Authorization -
Financial transactions - Data integrity - Core business flow

### 5.5 State Transition Testing (If Applicable)

-   Validate valid transitions
-   Validate invalid transitions

### 5.6 Decision Table Testing (If Complex Rules Exist)

-   Multi-condition logic combinations

------------------------------------------------------------------------

## 6. Priority Assignment Logic

Priority is assigned based on business impact:

Critical: - Core business flow - Financial impact - Authentication or
authorization - Data integrity risk

Major: - Important feature but not system-blocking

Minor: - UI behavior - Cosmetic issues - Low business impact

------------------------------------------------------------------------

## 7. Input Quality Handling Strategy

Before generating test cases, the skill evaluates input quality.

If spec is ambiguous: - Highlight ambiguous statements - Generate
clarification questions - Generate test cases with clearly stated
assumptions

If spec is incomplete: - Flag missing sections - Suggest standard
validation rules - Label assumptions explicitly

If spec contains conflicting logic: - Identify contradictions - Present
both interpretations - Request clarification

If validation rules are missing: - Suggest common best-practice
validations - Mark them as assumptions

------------------------------------------------------------------------

## 8. Coverage Evaluation Framework

Coverage is evaluated qualitatively based on:

-   Functional requirement mapping completeness
-   Validation coverage
-   Boundary case presence
-   Negative case presence
-   Risk-area coverage
-   Role-based coverage (if applicable)

Coverage classification:

High: - All functional requirements covered - Validation + boundary +
negative cases included - Risk areas addressed

Medium: - Functional covered - Some edge/boundary gaps

Low: - Core flows missing - Limited negative cases - No risk awareness

------------------------------------------------------------------------

## 9. Advanced Scenario Handling

If defined in spec, the skill also handles:

-   Role-based access scenarios
-   Cross-feature flow validation
-   Data persistence checks
-   Error message validation

------------------------------------------------------------------------

## 10. Non-Functional Requirements of the Skill

The skill must:

-   Produce consistent structured output
-   Avoid duplicate test cases
-   Ensure measurable expected results
-   Maintain traceability between requirement and test case
-   Perform self-review before final output

------------------------------------------------------------------------

## 11. Self-Review Mechanism

After generation, the skill must:

-   Check for duplicate cases
-   Check for missing boundary cases
-   Check for missing negative cases
-   Re-evaluate unclear expected results
-   Provide coverage assessment

------------------------------------------------------------------------

## 12. Out of Scope (MVP)

The following are intentionally excluded:

-   Performance / Load testing
-   Stress testing
-   Security penetration testing
-   Automation script generation (Selenium, Cypress, etc.)
-   UI pixel-perfect validation
-   Real test execution
-   CI/CD integration
-   Concurrency simulation
-   Deep API contract validation (unless explicitly defined in spec)
-   Multi-language localization testing

------------------------------------------------------------------------

## 13. Limitations

-   Output quality depends on spec quality
-   AI hallucination risk exists if spec is unclear
-   Large specifications may require chunking
-   Business context outside the spec cannot be inferred reliably

------------------------------------------------------------------------

## 14. Success Criteria

The skill is considered successful if:

-   It generates structured and reusable test cases
-   It covers happy, negative, boundary, and risk-based cases
-   It detects ambiguities in complex specifications
-   It reduces manual test case writing time significantly
-   It produces demo-ready output usable by QC immediately

------------------------------------------------------------------------

END OF SPEC
