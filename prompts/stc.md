# Spec-Then-Code: Specification Template

> **LLM Instructions**: When a user writes a prompt starting with "stc" followed by a feature description (e.g., "stc create a user authentication system"), interpret this as a request to generate a specification for that feature following this template. The prefix "stc" indicates the user wants to apply the Spec-Then-Code methodology to the described feature or component.

This document provides a structured template for writing specifications. Use this template to ensure consistency and completeness when documenting design and implementation plans.

This is a living document that evolves as the project progresses through collaborative human/AI interaction. Sections like Root Cause Analysis may expand or adapt as new insights emerge. The document serves as a shared knowledge base that the AI continually updates to reflect the current status of the project. In essence, it functions as an externalized context window, maintaining project state and decisions across multiple development sessions.

## Overview
*A brief summary of the feature, change, or fix being specified.*

### Output Location
Write the specification in a markdown file in the specs directory (create the specs directory if necessary).

## Problem Statement
*A clear and concise statement of the problem being addressed.*

## Background
*Relevant context and information about the problem or feature.*

### Justification
*Why this change is necessary or valuable.*

## Acceptance Criteria
*Specific, measurable conditions that must be met for the implementation to be considered complete and correct.*

### Design Goals
*The key principles and objectives guiding the design decisions.*

## Analysis of the Issue
*Detailed examination of the problem or feature.*

### Root Cause Analysis
*For bugs or issues, the underlying causes identified.*

### Research Findings
*Results of any investigation or exploration done to understand the problem space.*

## Benefits
*The anticipated positive outcomes of implementing this specification.*

## Affected Code
*Description of the code areas that will be impacted by this change.*

### Current Implementation
*Description of how things currently work in the codebase.*

### List of Files
*Specific files that will need to be modified or created.*

### Relevant Code Snippets
*Key pieces of existing code that are relevant to understanding the change.*

### Relevant Call Stacks
*Important call paths in the current implementation if applicable.*

### Relevant Object/Component Hierarchies
*Description of object relationships or component structures affected.*

## Proposed Solutions
*The potential approaches to solving the problem or implementing the feature.*

## Analysis of Changes Needed
*A detailed breakdown of what changes will be required to implement the chosen solution.*

## Implementation Plan
*Detailed step-by-step instructions for implementing the chosen solution.*

### Executable Steps for AI Agent
*Very detailed, precise steps that an AI coding agent can follow without human intervention. Should reference exact file paths and be specific about modifications.*

- [ ] Step 1: *Description of specific code change with exact file path*
- [ ] Step 2: *Description of specific code change with exact file path*

> **Note:** Each step should be granular and self-contained enough that an AI agent can execute it without additional context. Include specific file paths, function names, and code snippets where needed.
> 
> **Size Guidance:** Each executable step should be approximately the magnitude of "one story point" in planning poker terminology. This provides a consistent scale for task complexity and effort estimation.

### Required Code Changes
*Specific code modifications needed, with careful attention to dependencies and side effects.*

## Test-Driven Development
*Define verification mechanisms before implementation to ensure quality and correctness.*

### Verification Criteria
*Specific, measurable criteria that will verify the solution works correctly.*

### Test Cases
*Concrete test cases that should pass when the implementation is complete.*

- [ ] Test 1: *Description of test and expected outcome*
- [ ] Test 2: *Description of test and expected outcome*

### Edge Cases
*Special conditions or inputs that need specific handling and verification.*

### System Integration Points
*How the changes integrate with the rest of the system and verification needed at these points.*

> **Note:** All tests should be defined and reviewed BEFORE beginning code implementation. This ensures that the implementation is guided by clear verification criteria rather than assumptions.

## AI-Human Collaboration Notes
*Guidance on the division of responsibility between AI and human collaborators.*

### AI-Executable Tasks
*Tasks that can be fully handled by an AI coding agent.*

### Human Verification Points
*Critical points where human review or testing is needed.*
