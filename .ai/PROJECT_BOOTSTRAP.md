# PROJECT_BOOTSTRAP.md
# Engineering Handbook Bootstrap Agent
# Version: 0.1.0-alpha
# Status: Alpha
# Phase: Foundation
# Authority: Highest
#
# Read this file before performing ANY task.
#
# This document defines how this repository is initialized.
# It is NOT an implementation guide.
# It is the engineering architect for this project.

---

# MISSION

Your responsibility is NOT to build the application.

Your first responsibility is to establish the Engineering Handbook that will govern the application.

No source code shall be generated until the Engineering Handbook has been completed and approved.

Documentation always precedes implementation.

---

# PROJECT STACK

The project uses the following technologies.

Backend
- Laravel (latest stable)

Frontend
- React
- Inertia.js
- Tailwind CSS

Optional Backend Modularity
- nWidart Laravel Modules

Package Manager
- Composer
- npm

Language
- PHP
- JavaScript

---

# PRIMARY GOAL

Create a production-ready Engineering Handbook that defines:

- Architecture
- Standards
- Folder Structure
- Design System
- Component Standards
- React Standards
- Inertia Standards
- Laravel Standards
- Tailwind Standards
- AI Workflow
- Performance Standards
- Accessibility Standards
- Code Review Standards
- Definition of Done

The handbook becomes the single source of truth.

Do NOT skip directly to implementation.

---

# REQUIRED DIRECTORY STRUCTURE

Create exactly this structure.

.ai/

    AGENTS.md

    HANDBOOK_BLUEPRINT.md

    handbook/

        01-principles.md

        02-architecture.md

        03-folder-structure.md

        04-design-system.md

        05-component-architecture.md

        06-react.md

        07-inertia.md

        08-laravel.md

        09-tailwind.md

        10-nwidart.md

        11-ai-workflow.md

        12-performance.md

        13-accessibility.md

        14-code-review.md

        15-definition-of-done.md

    landing-pages/

        01-minimal-saas/

        02-modern-gradient/

        03-dashboard-preview/

        04-floating-cards/

        05-bento-grid/

        06-storytelling/

        07-threejs/

    prompts/

        create-component.md

        review-component.md

        optimize-component.md

        refactor-component.md

Do not rename folders.

Do not rename files.

Do not generate additional documents unless requested.

---

# GENERATION ORDER

Always generate documents in this order.

Phase 0

Generate

HANDBOOK_BLUEPRINT.md

Wait for approval.

----------------------------

Phase 1

Generate

01-principles.md

Review

Approve

----------------------------

Generate

02-architecture.md

Review

Approve

----------------------------

Generate

03-folder-structure.md

Review

Approve

----------------------------

Generate

04-design-system.md

Review

Approve

----------------------------

Generate

05-component-architecture.md

Review

Approve

----------------------------

Phase 2

Generate

06-react.md

07-inertia.md

08-laravel.md

09-tailwind.md

10-nwidart.md

One document at a time.

Review after every document.

----------------------------

Phase 3

Generate

11-ai-workflow.md

12-performance.md

13-accessibility.md

14-code-review.md

15-definition-of-done.md

Review every document.

Approve every document.

----------------------------

Phase 4

Generate landing page documentation.

Do NOT generate implementation.

---

# DOCUMENT TEMPLATE

Every handbook document MUST contain the following sections.

# Purpose

Explain why this document exists.

# Scope

Define what this document covers.

# Principles

High-level engineering philosophy.

# Standards

Mandatory rules.

# Best Practices

Recommended implementation patterns.

# Anti-patterns

Practices that are prohibited.

# Examples

Illustrative examples.

# Checklist

Verification checklist.

# Dependencies

List prerequisite documents.

# References

Related handbook documents.

---

# ENGINEERING PRINCIPLES

Always prefer

- Simplicity
- Readability
- Maintainability
- Reusability
- Accessibility
- Performance
- Scalability
- Consistency

Avoid

- Overengineering
- Premature optimization
- Duplicate documentation
- Conflicting standards
- Magic values
- Framework-specific hacks

---

# FRONTEND ARCHITECTURE

When later generating React code, follow Feature-First Architecture.

Example

Features/

    Landing/

    Inventory/

    Repairs/

    Authentication/

    Dashboard/

Shared UI components belong in a common UI layer.

Feature-specific components remain inside their feature.

---

# MODULARITY

Backend modules may use nWidart Laravel Modules.

Frontend architecture must remain feature-based and independent from backend module boundaries.

Avoid tightly coupling frontend folders to backend modules.

---

# REVIEW PROCESS

After every generated document perform:

1. Structural Review

2. Consistency Review

3. Dependency Review

4. Improvement Pass

5. Final Review

Only continue after all checks pass.

---

# IMPLEMENTATION RULE

Implementation is prohibited until:

✓ Handbook Blueprint approved

✓ All handbook documents completed

✓ Review completed

✓ Folder structure finalized

✓ Design system finalized

✓ Component architecture finalized

Only then may implementation begin.

---

# OUTPUT RULES

Never generate multiple handbook documents unless requested.

Never skip phases.

Never change filenames.

Never change folder names.

Never invent architecture.

Never contradict previously approved documents.

If a conflict exists, stop and request clarification instead of guessing.

---

# SUCCESS CRITERIA

The Engineering Handbook is considered complete only when:

✓ Every required document exists.

✓ Every document follows the standard template.

✓ Dependency order is respected.

✓ No duplicate standards exist.

✓ Folder structure is finalized.

✓ Architecture is internally consistent.

✓ The handbook is ready to guide future implementation.

Only after these criteria are met may application development begin.