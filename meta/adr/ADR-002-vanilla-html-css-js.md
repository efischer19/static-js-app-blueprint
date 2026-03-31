---
title: "Record 2: Use Vanilla HTML/CSS/JavaScript as the Default Frontend Stack"
status: "Accepted"
date: "2026-03-31"
tags:
  - "frontend"
  - "architecture"
  - "framework"
---

## Context

* **Problem:** This template repository needs a default frontend technology choice. As a blueprint for static frontend applications, it must provide a starting point that is accessible, maintainable, and adaptable to downstream projects that may adopt any framework.
* **Constraints:** The template should remain framework-agnostic by design. The default implementation must work without a build step, dev server, or package manager to minimize onboarding friction.

## Decision

The default frontend stack for this template is **vanilla HTML, CSS, and JavaScript** — no framework, no build step, no package manager. Downstream projects may adopt any framework (React, Vue, Svelte, etc.) by adding the appropriate tooling on top of this foundation.

## Considered Options

1. **Vanilla HTML/CSS/JS (The Chosen One):** Ship plain HTML, CSS, and JS files that can be opened directly in a browser.
    * *Pros:* Zero dependencies, zero build step, maximum simplicity, universally understood, aligns with the "Favor Simplicity & Static-First Design" principle from the Development Philosophy.
    * *Cons:* No component model, no built-in state management, may require more boilerplate for complex UIs.
2. **Vite + Vanilla JS:** Use Vite as a dev server and bundler with vanilla JS.
    * *Pros:* Fast dev server with hot module replacement, modern module support, easy upgrade path to frameworks.
    * *Cons:* Requires Node.js and npm, adds a build step, introduces a dependency for what may be a simple project.
3. **React / Vue / Svelte:** Ship with a specific framework pre-configured.
    * *Pros:* Component model, ecosystem of libraries, familiar to many developers.
    * *Cons:* Opinionated choice that conflicts with the goal of being framework-agnostic, heavier dependency footprint, requires a build step.

## Consequences

* **Positive:** The template is as simple as possible — a new user can open `src/index.html` in a browser and start working immediately. No tooling prerequisites beyond a text editor and a web browser.
* **Negative:** Developers who want a framework will need to set it up themselves. The template does not provide hot module replacement or a dev server out of the box.
* **Future Implications:** Downstream projects should document their framework choice in a new ADR that supersedes this one. The README includes guidance on adding a build step (Vite, Webpack, Parcel) when needed.
