# Spec-Then-Code: Commit Message Template

> **LLM Instructions**: When a user writes a prompt starting with "stc commit" (e.g., "stc commit"), interpret this as a request to generate a commit message following this template based on the recent code changes. The prefix "stc commit" indicates the user wants to create a structured commit message following the Spec-Then-Code methodology. 

This document provides structured guidance for writing high-quality commit messages that effectively communicate the purpose and context of code changes within the Spec-Then-Code methodology.

## Overview

Commit messages serve as a crucial part of project documentation, helping team members understand what changes were made, why they were necessary, and how they relate to the overall project goals. When written properly, commit messages create a clear trail of development decisions that enhance collaboration and maintainability.

## Commit Message Structure

When writing a commit message, follow this structure:

```
<title in past tense in sentence case>

<description of problem>

<description of solution>

<optional: description of alternatives considered (if highly relevant)>

Testing:
- <describe automated or manual tests performed>
```

### Title
- Should be in past tense (e.g., "Added", "Fixed", "Refactored")
- Use sentence case (capitalize first letter only)
- Be concise but descriptive (ideally under 50 characters)
- No period at the end

### Problem Description
- Clearly state what issue was being addressed
- Provide context that helps teammates understand the motivation for the change
- Reference relevant specification sections or requirements
- May include links to issues or specifications

### Solution Description
- Explain how your changes solve the problem
- Focus on the "what" and "why" rather than the "how" (the diff shows the how)
- Highlight key implementation decisions if they're not obvious from the code

### Alternatives (Optional)
- Only include if the decision-making process is valuable to document
- Briefly explain why the chosen approach was selected over alternatives

### Testing
- Document how the changes were tested
- Include both automated tests and manual verification steps
- This helps reviewers understand the scope of testing performed
- Can serve as documentation for how to test similar changes in the future

## Formatting Guidelines
- Use Markdown syntax for formatting
- Don't use hard line breaks; assume soft wrapping
- Use bullet points for lists
- Use code blocks for code snippets if needed

## Example Prompts

### Basic Prompt

```
Write a commit message for the changes I just made.
```

### Detailed Contextual Prompt

```
Write a commit message based on:
1. The git diff
2. The specification in [path/to/spec.md]
3. The implementation in [path/to/implementation.md]

Focus on how these changes address the requirements specified in the spec file.
```

### Enhanced Prompt with Testing Focus

```
Review the git diff and write a commit message that describes:
1. What problem was solved
2. How the solution addresses the requirements in [path/to/spec.md]
3. Include details about the tests performed to verify correctness
```

## Example LLM Response

When asked to "write a commit message", the LLM should:

1. First, run `git diff` to understand the code changes
2. Review relevant specification and implementation files
3. Analyze the relationship between the changes and the overall project goals
4. Generate a commit message following the template structure

### Example Response

```
Added user authentication middleware with role-based access control

The system lacked a secure way to validate user permissions for protected API endpoints, which could lead to unauthorized access to sensitive operations.

Implemented a multi-layered middleware approach that validates JWT tokens, extracts user roles, and checks permissions against a role-configuration map. This ensures that endpoints are only accessible to users with appropriate privileges while maintaining clean separation of authentication and business logic.

Testing:
- Added unit tests for token validation edge cases including expired tokens and malformed payloads
- Performed integration testing with the user service to verify proper role extraction
- Manually tested all protected endpoints with various user role combinations
```

## Integration with Spec-Then-Code Workflow

The commit message should explicitly reference how the changes relate to the specification document. This creates a clear traceability between requirements and implementation, which is a core principle of the Spec-Then-Code methodology.

When writing commit messages:
1. Reference the specific section of the specification being implemented
2. Note any deviations from the specification and why they were necessary
3. Update the specification if the implementation revealed issues with the original plan

This bidirectional relationship between specification and commit message helps maintain an accurate and up-to-date project history.
