# mule-audit-api

Dummy Mule 3.x audit API used for **log4j migration utility testing**.

## Scenario
- **log4j.xml**: 2 appenders — `CONSOLE` has the **old** pattern, `AUDIT_FILE` already has the **new** pattern
- **Expected migration result**: `SUCCESS` — only `CONSOLE` appender updated; `AUDIT_FILE` left unchanged

## Endpoints
| Method | Path                          | Description          |
|--------|-------------------------------|----------------------|
| POST   | /api/audit/events             | Record audit event   |
| GET    | /api/audit/trail/{entityId}   | Get audit trail      |
