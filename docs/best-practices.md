---
title: Best Practices
description: "A comprehensive guide to Claude Code recommended prompts and efficiency tips."
---

# Claude Code Recommended Prompts Guide

The powerful features of Claude Code largely depend on how you communicate with it effectively. This document compiles efficient prompt templates for various development scenarios.

---

## 🚀 Project Initialization

### Quick Project Structure Understanding
> Please read the project's README.md, package.json and main directories, help me understand this project's architecture and tech stack, but don't write any code for now.

### Create Project Configuration File
> Please help me create a detailed CLAUDE.md file, including project architecture description, common commands, coding standards and development environment configuration.

---

## 🎯 Feature Development

### New Feature Development Flow
> I need to develop [feature description]. Please follow these steps:
> 1. First read relevant code to understand the existing architecture
> 2. Create a detailed implementation plan
> 3. Implement core functionality
> 4. Write tests
> 5. Update documentation
> Please pause after each step and wait for my confirmation.

### Component Development
> Please help me create a [component name] component, requirements:
> - Follow existing component patterns in the project
> - Include TypeScript type definitions
> - Support [specific feature requirements]
> - Write corresponding test files

---

## 🔧 Code Debugging & Optimization

### Error Diagnosis
> I encountered this error: [error message]. Please help me analyze the cause and provide a fix. If you need to check related code, please let me know.

### Code Review
> Please conduct a code review for [file/feature], focus on checking:
> - Code standards
> - Security issues
> - Performance issues
> - Best practices
> - Potential bugs

---

## 🧪 Testing Related

### Test Case Writing
> Please write comprehensive test cases for [function/class/component], including:
> - Normal case testing
> - Boundary condition testing
> - Error case testing
> - Mock dependencies

---

## 🔄 Git Workflow

### Code Commit
> Please review the current changes, write appropriate commit messages and commit the code. The commit message should follow the project's commit conventions.

---

## 📋 Usage Recommendations

### Prompt Writing Principles
- **Be Specific**: Describe requirements in detail, avoid vague expressions.
- **Step by Step**: Break complex tasks into multiple steps.
- **Set Boundaries**: Clearly state what to do and what not to do.
- **Include Context**: Provide necessary background information.
- **Verify and Confirm**: Require confirmation for important steps before continuing.

### Common Modifiers
- **"Please first analyze..."**: Require Claude to understand before acting.
- **"Don't ... for now"**: Set clear boundaries.
- **"Please pause after each step"**: Control execution pace.
- **"Follow existing project..."**: Maintain consistency.

### Efficiency Tips
- **Use @ to reference files**: `@src/components/Button.tsx`
- **Utilize extended thinking**: Press Shift+TAB twice to enter PLAN mode.
- **Clean context properly**: Use `/clear` and `/compact`.
- **Batch operations**: Handle multiple similar tasks at once.
