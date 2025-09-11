# GitHub Copilot Instructions

These instructions guide Copilot to generate code consistently for this repository.

---

## General Guidelines
- Always write **clean, production-level Python code**.
- Follow **PEP8** style conventions.
- Use **type hints** for all function parameters and return values.
- Include **docstrings** for modules, classes, and functions (Google or NumPy style).
- Prefer readability over clever one-liners.
- Avoid unused imports or variables.
- Use `logging` instead of `print`.

---

## MongoDB (PyMongo)
- Always use **environment variables** (never hardcode credentials).
- Ensure proper **error handling** (duplicate keys, invalid queries, connection issues).
- Do not hard code any string, always create corresponding const and use only constants.
- Never include sensitive info in the log/print.

---

## Testing
- Write **pytest** tests.
- Use a **separate test database**.
- Mock external dependencies (like MongoDB) in unit tests.
- Ensure tests are isolated and reproducible.

---

## Security
- Do not log sensitive data (e.g., passwords, tokens).
- Validate and sanitize all user inputs.
- Use environment variables for secrets.

---