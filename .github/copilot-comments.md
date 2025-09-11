# GitHub Copilot PR Review Guidelines

When reviewing pull requests in this repository, follow these rules:

---

## Code Style
- Ensure code follows **PEP8** conventions.
- Verify all functions include **type hints** and **docstrings**.
- Check for unused imports or variables.
- Always keep imports on top of the file.
- Check line length, shouldn't cross 110.

---

## MongoDB Usage
- Ensure **no credentials are hardcoded** (must use env variables).
- Verify queries go through the **service layer**, not directly from routes.
- Check CRUD functions follow the **BaseService** pattern with logging.
- Check all the db alter operations are added to audit logs

---

## Security
- Confirm sensitive values are not logged.
- Check input validation is present for new endpoints.
- Verify proper exception handling for DB operations.

---

## Testing
- Ensure **pytest tests** exist for new functionality.
- Check tests use a **test database** (not production).
- Confirm external dependencies (like MongoDB) are mocked where necessary.

---

## Do Not
- Do not approve code with hardcoded secrets or tokens.
- Do not allow bypass of centralized config, logging, or error handling.
- Do not allow direct database queries inside routes.
