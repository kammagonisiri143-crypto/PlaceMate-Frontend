---
name: PlaceMate API boundary
description: Product constraint for backend ownership and frontend integration.
---

PlaceMate's backend is being developed independently with FastAPI and SQLite. Keep this app frontend-only; do not build a second backend or database. Integrate only against the backend's actual API contract, not guessed resource paths or payload shapes. Keep API mode separate from demo fixtures and never silently fall back to demo data.

**Why:** the user specified that the backend is independent and that the frontend must remain usable during its development; guessed contracts could conflict with the backend or misrepresent fake data as live.

**How to apply:** wait for the real OpenAPI contract or `/docs` before wiring API calls, and preserve the clearly labeled demo mode until then.
