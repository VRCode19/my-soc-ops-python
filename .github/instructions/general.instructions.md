---
applyTo: "**"
---

Here is the compressed copilot-instructions.md with the mandatory development checklist at the top, ready to be saved as a single file in `.github/copilot-instructions.md`:

```markdown
# Copilot Workspace Instructions

## ✅ Development Checklist

1. **Lint**: `uv run ruff check .`
2. **Test**: `uv run pytest`
3. **Build**: `uv run uvicorn app.main:app --reload`

---

## Stack

- **Backend**: FastAPI 3.13+
- **Templates**: Jinja2 + HTMX
- **Styling**: Custom CSS utilities (no Tailwind)
- **State**: Server-side cookies (itsdangerous)

## Structure

```
app/
  main.py           → Routes
  game_logic.py     → Board & win logic
  game_service.py   → Sessions
  models.py         → Data models
  data.py           → Questions
  templates/ + static/

tests/
  test_api.py       → Routes
  test_game_logic.py → Logic
```

## Conventions

- **Board**: 5×5, free center, 24 questions
- **Win**: 5 in a row (row/col/diagonal)
- **Updates**: HTMX partials, no full reloads

## Agents & Guidance

- `/tdd` — Red-Green-Refactor
- `/ui-review` — Frontend feedback
- See `instructions/` folder for detailed guides

## Commands

```bash
uv run uvicorn app.main:app --reload  # Dev server
uv run pytest -v                       # Tests
uv run ruff check . --fix              # Auto-fix
```
```

Just copy and save this content to `.github/copilot-instructions.md` in your repository. This single file covers all requirements.
## No Simple Browser

Never use the Simple Browser or `open_simple_browser` to preview the application. When running the app, just start it and confirm it's running — do not open any browser preview.
