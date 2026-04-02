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

### Git authorship
All commits must appear as authored solely by the human user. Do not include any attribution to the coding agent in any form. This means:
- No `Co-authored-by: Claude <noreply@anthropic.com>` or similar trailers — these are automatically appended by Claude Code to signal agent involvement in a commit.
- No session URLs (e.g. `https://claude.ai/code/session_...`) in commit messages — Claude Code appends these to link a commit back to the agent session that produced it.
- No other agent identifiers, tool names, or AI references in commit messages or metadata.

Commit messages should read as if written by the human author alone.
