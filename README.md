# static-js-app-blueprint

> A template repository for building static frontend applications with HTML, CSS, and JavaScript.

## What Is This?

This is a **GitHub template repository** that provides the foundational directory structure, documentation, and configuration for static frontend web applications. It is framework-agnostic — the default example uses vanilla HTML/CSS/JS, but the structure accommodates any static build output (React, Vue, Svelte, etc.).

This template is derived from the [blueprint-repo-blueprints](https://github.com/efischer19/blueprint-repo-blueprints) grandparent template, which provides universal scaffolding for documentation, ADRs, and developer tooling.

## How to Use This Template

1. Click the **"Use this template"** button at the top of the repository page on GitHub.
2. Choose a name for your new repository.
3. Clone your new repository and begin building your frontend application in the `src/` directory.

For more details on GitHub template repositories, see the [official documentation](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository).

## What's Included

| Path | Purpose |
| :--- | :--- |
| `src/` | Frontend source files — `index.html`, `style.css`, `script.js` |
| `meta/adr/` | Architecture Decision Records — the logbook of *why* decisions were made |
| `meta/plans/` | Project plans and roadmaps |
| `docs-src/` | Source files for generated documentation (e.g., MkDocs) |
| `scripts/` | Utility and automation scripts |
| `.github/` | GitHub-specific configuration (issue templates, PR templates, Copilot instructions) |

### Key Files

- **`src/index.html`** — Starter page with semantic HTML and basic accessibility attributes
- **`src/style.css`** — Minimal stylesheet with CSS custom properties
- **`src/script.js`** — JavaScript entry point with example DOM interaction
- **`LICENSE.md`** — MIT License
- **`CODE_OF_CONDUCT.md`** — Contributor Covenant Code of Conduct
- **`SECURITY.md`** — Security policy and vulnerability reporting
- **`CONTRIBUTING.md`** — Guidelines for contributing to the project
- **`meta/adr/ADR-002-vanilla-html-css-js.md`** — Framework selection rationale (vanilla HTML/CSS/JS)

## Getting Started

After creating a new repository from this template:

### 1. Preview the Starter Page

Open `src/index.html` directly in a browser — no build step or dev server required.

### 2. Build Your Application

Edit files in `src/` to build your frontend application:

- **`src/index.html`** — Add your HTML content with semantic markup
- **`src/style.css`** — Add your styles
- **`src/script.js`** — Add your JavaScript logic

### 3. Adding a Build Step (Optional)

The default setup requires no build step. If you need a bundler (e.g., for JSX, TypeScript, or module bundling), add your configuration at the project root:

- **Vite**: `npm create vite@latest . -- --template vanilla` and point `root` to `src/`
- **Webpack**: Add `webpack.config.js` at the project root
- **Parcel**: Run `npx parcel src/index.html`

Document your choice in a new ADR (see `meta/adr/TEMPLATE.md`).

### 4. Set Up Local Development

```bash
# Install pre-commit hooks
pip install pre-commit
pre-commit install

# Run local quality checks
./scripts/local-ci-check.sh

# Build documentation (optional)
pip install -r docs-requirements.txt
./scripts/build-docs.sh
```

### 5. Verify CI

Push a change or open a pull request to confirm the CI workflow runs and passes in your new repository.

## Design Principles

- **Framework-agnostic.** The default is vanilla HTML/CSS/JS, but the structure supports any frontend framework or build tool.
- **No build step required.** Open `src/index.html` in a browser and start building.
- **Minimal by design.** Only universal scaffolding is included — add tools and dependencies as needed.
- **Documentation-first.** Every significant decision is captured in an ADR.
- **AI-friendly.** The structure and conventions are designed to work well with AI-assisted development workflows.

## License

This project is licensed under the [MIT License](./LICENSE.md).
