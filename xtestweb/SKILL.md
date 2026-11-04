---
name: xtestweb
description: Test a web app feature in a real browser against a throwaway mock backend. Use when the user asks to test, run or verify a web feature in the browser.
---

# xtest-browser
Verify web features in a real browser without the real backend.

1. Find how to run the app (`AGENTS.md`, `docs/`, README, package/project files). Ask if the dev command, API URL setting or login flow is unclear.
2. Read the feature's UI code, its API client, and the backend contract (routes, request/response types) so the mock matches the real API.
3. Write a dependency-free mock server in the scratchpad directory, never in the repo. Use a free port (check with `netstat`). Add CORS headers and answer `OPTIONS`. Implement login (a user with the needed permissions), the feature's routes (list, filters, create, update, delete), lookup routes, and an empty `[]` or `{}` for anything else. Log every request to a file.
4. Install dependencies if missing. Start the mock and the dev server in the background, pointing the app at the mock through an environment variable or flag. Do not edit config or `.env*` files and never start the real backend.
5. Open the app with `preview_start`. Log in with made-up test values. Prefer `find`, `read_page` and `get_page_text` over screenshots.
6. Exercise the feature: list and filters, create (validation errors, then valid save), edit, delete with confirm, permission gating, state after navigating away. After each write, compare the request body in the mock log with the contract.
7. Report what passed, what failed and what was not exercised. Do not claim untested flows work. Fix real bugs found in the app code and rerun.
8. Stop the mock and dev server (kill by port). Do not commit unless asked.
