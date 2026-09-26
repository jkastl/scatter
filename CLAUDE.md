# CLAUDE.md

## Project Overview

Single-file web app. The entire application lives in `index.html`. There is no package.json, no build system, and no dependencies to install.

Public GitHub repo: https://github.com/jkastl/scatter

## Rules

### Keep it simple
Do not add tests, linters, CI configuration, or any code analysis tooling unless explicitly instructed. This project intentionally has no build or test infrastructure.

### Version bumping
The version uses [semver](https://semver.org/) and is updated by hand. It's displayed as `vMAJOR.MINOR.PATCH · YYYY-MM-DD` (e.g. `v1.8.0 · 2026-09-26`) inside the `.version-label` div in `index.html`. With every change you push, bump the right part of the version, set the date to today and add an entry to `CHANGELOG.md`. See the Versioning section of `README.md` for which part to bump.

### No private information
This is a public repository. Do not include API keys, credentials, personal data, internal URLs, or any other private information in any commit or file.

### Git workflow
Develop and push all changes directly to the `main` branch. Do not create feature branches or pull requests unless explicitly asked. Commit directly to `main` and push with `git push -u origin main`.