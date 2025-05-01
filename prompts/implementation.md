# Spec-Then-Code: Implementation Guide

> **LLM Instructions**: When a user writes a prompt starting with "stc implement" followed by a reference to a specification (e.g., "stc implement [path-to-spec-file]"), interpret this as a request to generate an implementation plan and/or code that follows this guide based on the referenced specification. The prefix "stc implement" indicates the user wants to move from specification to implementation following the Spec-Then-Code methodology.

This document provides guidance for implementing code based on specifications created using the Spec-Then-Code methodology.

## Output Location
Write the implementation plan in a markdown file in the specs directory (create the directory if necessary).

## Implementation Plan
*A step-by-step plan for implementing the solution, presented as a series of checkable tasks.*

- [ ] Task 1
- [ ] Task 2
- [ ] Task 3

## Implementation Guidelines
*When implementing a task from this spec:*

1. Review the entire specification to understand the context
2. Implement or update tests based on the Test-Driven Development section
3. Verify the tests fail appropriately (for new features) or correctly identify the issue (for bug fixes)
4. Make the necessary code changes to satisfy the tests
5. Run the tests to verify your implementation works correctly
6. Use `git diff` to review your changes
7. Compare the changes against the specific task requirements and verification criteria
8. Mark the task as complete if it meets all requirements and passes all tests
9. If not, continue iterating until all verification criteria are satisfied
