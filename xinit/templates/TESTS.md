# Testing standard

## Stack
- Framework: {{test framework and runner}}. Tests live in {{folder and file naming pattern}}.

## Levels
| Level | Covers | Location | Command |
|---|---|---|---|
| Unit | {{pure logic, no I/O}} | `{{path}}` | `{{command}}` |
| Integration | {{DB, API, queues with real or containerised deps}} | `{{path}}` | `{{command}}` |
| E2E | {{critical user flows}} | `{{path}}` | `{{command}}` (manual browser checks: `/xtestweb`) |

## Rules
- New logic gets unit tests. New endpoints and integrations get integration tests.
- Every bug fix adds a test that fails before the fix.
- Test behaviour through public interfaces, not implementation details.
- Tests are deterministic and isolated: no shared state, real network, unseeded randomness or wall-clock dependence.
- Mock only at system boundaries ({{external APIs, clock, email}}). {{What must use real deps, e.g. the database}}.
- Never skip, disable or weaken a test to get green. Fix the code, or ask.

## Test data
- Fixtures/factories: `{{path}}`. No production data or real secrets.

## Running
- All: `{{command}}`
- Single test/file: `{{command}}`
- Coverage: `{{command}}`. Target: {{percentage or TODO(user)}}.

## Done means
- Affected tests and {{full suite / CI job}} pass, and were actually run. Report anything not run.
