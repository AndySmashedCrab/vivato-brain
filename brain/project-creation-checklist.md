# Project Creation Checklist

This checklist describes the steps required to create a new project using the company platform template.

---

## Step 1 — Create Project from Template

Create a new repository using the `company-template`.

Ensure both frontend and backend projects build successfully.

---

## Step 2 — Configure Environment

Update configuration values:

* application name
* environment settings
* API base URLs
* authentication configuration

---

## Step 3 — Verify Core Platform Features

Confirm the following features are working:

* Login
* Logout
* Authentication
* My Account page
* Role handling (`SuperAdmin`, `Admin`, `User`)
* Navigation
* Theming
* Error handling

---

## Step 4 — Verify API Connectivity

Confirm the frontend can call backend endpoints using `ApiContext`.

Verify error responses behave correctly.

---

## Step 5 — Create First Module

Create the first business module using the standard module structure.

Frontend example:

```
features/
  example-module/
    components/
    models/
```

Backend example:

```
Modules/
  ExampleModule/
    Controllers/
    Models/
    Services/
    ViewModels/
```

---

## Step 6 — Begin Real Feature Development

Once the platform is verified, begin implementing the real modules required by the project.

Modules should follow the agreed structure.

---

## Step 7 — Evaluate for Reuse

When a module matures, consider whether it should be promoted to the shared modules repository.

Promotion should occur only when the module is reasonably reusable.
