# CLAUDE.md

## Project Overview

Single-file web app. The entire application lives in `index.html`. There is no package.json, no build system, and no dependencies to install.

Public GitHub repo: https://github.com/jkastl/scatter

## Rules

### Keep it simple
Do not add tests, linters, CI configuration, or any code analysis tooling unless explicitly instructed. This project intentionally has no build or test infrastructure.

### Version bumping
Before pushing to the remote repo, increment the minor version number by 1. The version is displayed as a string (e.g. `v1.5`) inside the `.version-label` div in `index.html`. Update that string in place.

### No private information
This is a public repository. Do not include API keys, credentials, personal data, internal URLs, or any other private information in any commit or file.

### Git workflow
Develop and push all changes directly to the `main` branch. Do not create feature branches or pull requests unless explicitly asked. Commit directly to `main` and push with `git push -u origin main`.