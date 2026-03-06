# Module Guidelines

## Purpose

Modules represent **self-contained business capabilities** that can be reused across projects.

Examples of modules may include:

* CRM
* Quoting
* Activity Log
* Delivery Calendar

Modules are **full-stack**, meaning they include both frontend and backend components.

---

## Module Philosophy

All project features should be built in a **modular shape**.

However, not every feature needs to become a shared module.

Only features with clear reuse value should be promoted into the shared modules library.

---

## Frontend Module Structure

Frontend modules should live under:

```
src/features/
```

Standard structure:

```
features/
  module-name/
    components/
    models/
    contexts/   (optional)
    hooks/      (optional)
```

### components

Contains:

* page components
* supporting UI components

If a module contains multiple pages, each page may use a subfolder.

---

### models

Frontend data models used by the module.

---

### contexts (optional)

Module-specific state shared across components.

---

### hooks (optional)

Reusable logic used within the module.

This may include:

* API calls
* data loading logic
* UI state helpers

---

## Backend Module Structure

Backend modules live under:

```
Modules/
```

Standard structure:

```
Modules/
  ModuleName/
    Controllers/
    Models/
    Services/
    ViewModels/
```

---

### Controllers

Responsible for:

* exposing HTTP endpoints
* handling request/response flow

Controllers should remain **thin**.

Business logic should not live here.

---

### Models

Database models only.

These represent persistent data owned by the module.

---

### Services

Contains module business logic.

Responsibilities may include:

* business workflows
* validation logic
* orchestration
* supporting utilities

---

### ViewModels

API request and response models used by the module.

These represent the data shape exposed to clients.

---

## Module Responsibilities

A module should:

* represent a clear business capability
* own its own persistence where appropriate
* expose clear API endpoints
* minimize coupling with other modules

Cross-module interaction should generally occur through:

* APIs
* interfaces
* helpers

---

## Promotion to Shared Modules

A feature may be promoted into the shared modules repository when:

* it has a clear business boundary
* it is likely reusable in other projects
* it is not deeply client-specific
* it follows the module structure
* basic documentation is provided

Not every feature should be promoted.

Modules should only be added when they provide real value.
