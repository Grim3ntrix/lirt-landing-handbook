# PROJECT_BOOTSTRAP.md
# Engineering Handbook Bootstrap Agent
# Version: 0.2.0-alpha
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

Establish the complete engineering foundation for this repository.

The engineering foundation consists of three layers:

1. Engineering Handbook
2. Domain Bootstraps
3. Domain Specifications

Documentation always precedes implementation.

Implementation must never begin until all required engineering documentation has been generated, reviewed, and approved.

---

## Layer 1 — Engineering Handbook

The first responsibility is to create a production-ready Engineering Handbook that defines:

- Architecture
- Engineering Standards
- Folder Structure
- Design System
- Component Architecture
- React Standards
- Inertia Standards
- Laravel Standards
- Tailwind Standards
- nWidart Module Standards
- AI Workflow
- Performance Standards
- Accessibility Standards
- Code Review Standards
- Definition of Done

The Engineering Handbook becomes the single source of truth for every engineering decision within this repository.

---

## Layer 2 — Domain Bootstraps

After the Engineering Handbook has been completed and approved, generate the required Domain Bootstrap documents.

Each Domain Bootstrap defines how a specific project domain should be documented.

Example domains include:

- Landing Pages
- Dashboard
- Authentication
- Settings
- Inventory
- Reports

Each Domain Bootstrap inherits all Engineering Handbook standards.

---

## Layer 3 — Domain Specifications

After a Domain Bootstrap has been approved, generate its implementation-ready specifications.

Example:

LANDING_BOOTSTRAP.md

├── 01-minimal-saas
├── 02-modern-gradient
├── 03-dashboard-preview
├── 04-floating-cards
├── 05-bento-grid
├── 06-storytelling
└── 07-threejs

Domain Specifications inherit both:

- Engineering Handbook
- Domain Bootstrap

Implementation must only begin after all required specifications have been approved.

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

        LANDING_BOOTSTRAP.md

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

Landing Page Bootstrap

If

.ai/landing-pages/LANDING_BOOTSTRAP.md

does not exist

Generate it.

The Landing Bootstrap defines:

• Supported landing page styles

• Required documentation structure

• Document responsibilities

• Generation order

• Review workflow

• Engineering Handbook inheritance

• Complete landing page design catalog

• Design Selection Matrix

• Package Recommendation Matrix

• AI workflow

• Completion criteria

If LANDING_BOOTSTRAP.md already exists:

- Read it.
- Follow it.
- Do not regenerate it.
- Do not overwrite it.

Do not generate landing page specifications until LANDING_BOOTSTRAP.md has been approved.

Do not generate implementation.

---

Phase 5

Landing Specifications

Read

.ai/landing-pages/LANDING_BOOTSTRAP.md

Present the available landing page styles defined in LANDING_BOOTSTRAP.md.

Wait for the user to select a landing page style.

Generate only the selected landing page specification.

Review the specification.

Await approval.

Do not generate implementation.

---

# BOOTSTRAP RULES

Bootstrap documents define project architecture.

Bootstrap documents are immutable after approval.

If a bootstrap document already exists:

Read it.

Follow it.

Do not regenerate it.

Do not overwrite it.

Do not modify it.

Future modifications require explicit user approval.

Bootstrap documents always take precedence over generated specifications.

Specifications inherit bootstrap rules.

Implementation inherits specification rules.

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

The engineering foundation is considered complete only when:

✓ Engineering Handbook approved

✓ LANDING_BOOTSTRAP.md generated, reviewed, and approved

✓ All landing page specifications approved

✓ Folder structure finalized

✓ Architecture internally consistent

✓ No conflicting standards exist

✓ Documentation hierarchy complete

Only after these criteria are met may implementation begin.