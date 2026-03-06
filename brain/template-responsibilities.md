# Template Responsibilities

## Purpose

The template provides the **host platform** for all applications built on the company React + ASP.NET Core stack.

Its goal is to allow a new project to start quickly with the core platform concerns already implemented.

The template should remain **thin but production-ready**.

It should provide shared infrastructure and architectural structure, but **not business functionality**.

---

## What the Template Provides

### Frontend Platform

The template frontend provides the core application framework:

* Application shell
* Routing and navigation framework
* Provider configuration
* Shared application contexts

Standard contexts provided:

* `ApiContext`
* `AuthContext`
* `UserContext`
* `RoleContext`
* `ToastContext`
* `ThemeContext`

These contexts are considered **platform services** and should be consumed by modules.

---

### Authentication

The template includes a working authentication system.

Capabilities:

* Login
* Logout
* Authentication handling
* Role-based access
* My Account management

Roles supported in the template:

* `SuperAdmin`
* `Admin`
* `User`

Permissions are **not included in v1**.

---

### Backend Platform

The backend template provides:

* ASP.NET Core API host
* JWT authentication
* Role-based claims
* User management foundation
* Standard error handling
* Structured logging
* Correlation IDs

Backend modules plug into this host.

---

### Error Handling

Both frontend and backend include a consistent error handling approach.

Frontend:

* user-friendly error display
* toast notifications

Backend:

* standard API error responses
* structured logging

---

## What the Template Does NOT Include

The template intentionally avoids:

* client-specific business features
* demo modules
* experimental architecture
* large collections of business functionality
* permission management systems

Business capabilities belong in **modules**, not the template.

---

## Design Principles

The template should follow these principles:

* **Real project ready**
* **Minimal but complete**
* **Predictable structure**
* **Stable platform services**
* **Business logic lives in modules**

---

## Definition of Success

A project created from the template should immediately support:

* login / logout
* authentication
* role-based access
* user management
* navigation
* theming
* error handling

Developers should then be able to begin building **real modules immediately**.
