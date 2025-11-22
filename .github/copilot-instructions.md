# GitHub Copilot / AI Agent Instructions for MIKE.MAFIA

Repository state: minimal — only `README.md`; no manifests or CI.

Goal: Propose minimal, safe scaffolding only after confirming language/architecture with the owner.

Checklist for all tasks:
- Read `README.md`; if missing info, ask: "Which language/runtime and primary purpose (service, library, CLI)?"
- If asked to implement a feature and there is no manifest, propose two stacks (Node+Express, Python+FastAPI). Ask for confirmation before starting.
- After confirmation, add minimal skeleton: `src/`, `tests/`, and a relevant manifest (`package.json`/`pyproject.toml`/`go.mod`).
- Update `README.md` to include run/test commands and assumptions.

Branching & PR rules:
- Create a branch for non-trivial changes (e.g., `feat/add-foo`).
- PRs must contain a 1–2 line summary, key files changed, and one or two run/test commands.
- Use commit prefixes: `feat:`, `fix:`, `chore:`, `docs:`, `test:`.

Testing & CI:
- If no CI exists, propose a minimal GitHub Actions workflow to run tests and linting.
- Add test/lint scripts to the project manifest and include short examples in the README.

Examples (brief):
- Node: `package.json` with `start` (`node src/index.js`) and `test` (`jest`).
- Python: `pyproject.toml` with `pytest`; `src/main.py` and `tests/test_basic.py`.

Integration & secrets:
- If adding integrations, request: target environment, where secrets should be stored, and sample data flows.

When to ask the owner:
- If the repo lacks a manifest or code and the requested work needs frameworks, CI, or infra.
- If credentials, external APIs, or data samples are required.

Do NOT do without confirmation:
- Do not change license/author details.
- Do not assume a stack or add credentials/CI with secrets.

If anything is unclear, ask the owner a concise clarifying question before making changes.