# CLAUDE.md

This file provides guidance to AI assistants (Claude and others) working in this repository.

## Repository Overview

**Repository**: `Ishwor123-gtm/Skill`
**Status**: New / empty repository — no source code exists yet.

This repository is in its initial state. No tech stack, framework, or project structure has been established. When the project is initialized, this file should be updated to reflect the actual codebase.

---

## Working in This Repository

### Branch Convention

- Development happens on feature branches prefixed with `claude/` for AI-driven tasks
- Never push directly to `main` without explicit permission
- Always use `git push -u origin <branch-name>` when pushing a new branch

### Git Workflow

```bash
# Check current state
git status
git log --oneline --all

# Stage specific files (avoid git add -A to prevent committing sensitive files)
git add <file>

# Commit with a descriptive message
git commit -m "type: short description of change"

# Push branch
git push -u origin <branch-name>
```

### Commit Message Style

Use conventional commits format:

```
feat: add user authentication
fix: resolve null pointer in login handler
docs: update API usage examples
refactor: extract validation logic to helper
test: add unit tests for parser
chore: update dependencies
```

---

## AI Assistant Guidelines

### General Principles

1. **Read before editing** — always read a file before modifying it
2. **Minimal changes** — make only what is needed; do not refactor surrounding code unless asked
3. **No speculative abstractions** — don't add helpers, utilities, or abstractions for one-time use
4. **No unnecessary files** — prefer editing existing files over creating new ones
5. **No added comments** — only add comments where the logic is non-obvious
6. **Security first** — never introduce command injection, XSS, SQL injection, or other OWASP top-10 vulnerabilities
7. **No backwards-compat hacks** — if something is unused, delete it cleanly

### Scope Discipline

- A bug fix does not require cleaning up surrounding code
- A feature request does not imply adding extra configurability
- Do not add error handling for scenarios that cannot occur
- Do not add feature flags or shims when you can simply change the code

### Risky Actions — Always Confirm First

The following actions require explicit user confirmation before proceeding:

| Action | Risk |
|--------|------|
| `git push --force` | Overwrites remote history |
| `git reset --hard` | Destroys local uncommitted work |
| Deleting files/branches | Hard to reverse |
| Modifying CI/CD pipelines | Affects all contributors |
| Dropping database tables | Data loss |
| Publishing to external services | Visible to others |

---

## Project Setup (To Be Completed)

Once the project is initialized, update the sections below:

### Tech Stack

> _Not yet determined. Update this section after the project is initialized._

### Directory Structure

```
/
├── (to be defined)
```

### Development Commands

```bash
# Install dependencies
# (define after project init)

# Run development server
# (define after project init)

# Run tests
# (define after project init)

# Lint / format
# (define after project init)

# Build
# (define after project init)
```

### Testing

> _No test framework selected yet. Update after project setup._

### Linting & Formatting

> _No linter or formatter configured yet. Update after project setup._

---

## Environment Configuration

- Never commit `.env` files or secrets
- Use `.env.example` to document required environment variables (with placeholder values)
- Load secrets from environment variables, not hardcoded values

---

## Updating This File

This file should be kept current. Update it when:

- A tech stack or framework is chosen
- New development commands are added
- Architectural patterns are established
- Testing or linting conventions are defined
- CI/CD pipelines are configured

The goal is that any AI assistant (or new human contributor) can read this file and immediately understand how to work in the repository.
