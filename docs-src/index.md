# static-js-app-blueprint Documentation

Welcome to the official documentation for **static-js-app-blueprint**.

## Overview

static-js-app-blueprint is a template repository for building static frontend
applications using HTML, CSS, and JavaScript. It is framework-agnostic — the
default example uses vanilla HTML/CSS/JS, but the structure accommodates any
static build output (React, Vue, Svelte, etc.).

This template is built on top of the
[blueprint-repo-blueprints](https://github.com/efischer19/blueprint-repo-blueprints)
template, which provides a language-agnostic foundation for documentation,
architecture decision records, and developer tooling.

## Getting Started

1. **Use this template** — Click "Use this template" on GitHub to create a new
   repository.
2. **Open `src/index.html`** in a browser to see the starter page.
3. **Edit files in `src/`** — Modify `index.html`, `style.css`, and `script.js`
   to build your application.

## Project Structure

```text
static-js-app-blueprint/
├── src/              # Frontend source files
│   ├── index.html    # Entry point with semantic HTML
│   ├── style.css     # Stylesheet
│   └── script.js     # JavaScript entry point
├── meta/             # Development philosophy, ADRs, and plans
├── docs-src/         # Documentation source files (MkDocs)
├── scripts/          # Utility and automation scripts
└── .github/          # GitHub-specific configuration
```

## Development Philosophy

All work in this project follows the
[Development Philosophy](DEVELOPMENT_PHILOSOPHY.md), which emphasizes:

- **Code is for Humans First** — Clarity over cleverness
- **Favor Simplicity** — Static-first design with minimal complexity
- **Confidence Through Testing** — Comprehensive automated tests
- **Clean Commit History** — Atomic commits with descriptive messages

## Contributing

For information on contributing to this project, see the
[Contributing Guidelines](CONTRIBUTING.md).

## Getting Help

- Check the documentation pages listed in the navigation
- Review the [Architecture Decision Records](https://github.com/efischer19/static-js-app-blueprint/tree/main/meta/adr)
  for context on past decisions
- [Open an issue](https://github.com/efischer19/static-js-app-blueprint/issues)
  if you find a bug or want to suggest a feature
