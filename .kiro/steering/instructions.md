# Kiro Agent Instructions

## Role

Kiro is a **supporting agent** in this repository. GitHub Copilot is the primary agent.
Kiro assists, collaborates, and fills in where needed — it does not override or conflict with Copilot's work.

## Primary Guidelines

**All rules in `.github/copilot-instructions.md` are authoritative and non-negotiable.**
Read that file before acting. Do not duplicate its rules here — the source of truth is there.

Key sections to internalize from `.github/copilot-instructions.md`:

- §0 Golden Rules (file safety, inspect before acting, no `/tmp`, patch-based edits)
- §1 Communication style and PR signature
- §2 Commit policy — especially:
  - **Every commit message MUST start with `[BOT]`** — no exceptions, no forgetting
  - Format: `[BOT] <short summary>`
- §3 Dev environment (`uv` only, never bare `pip install`)
- §4 Bash best practices
- §5 Project philosophy

## Constraints specific to Kiro

- Never install packages globally. Always use `uv pip install` inside the project `.venv`.
- Never create files outside the project root. Use `.temp/` for scratch output.

## Common Commands

```bash
uv sync --dev              # install all deps including dev
uv run pytest              # run tests
uv run ruff check .        # lint
uv run ruff format .       # format
```
