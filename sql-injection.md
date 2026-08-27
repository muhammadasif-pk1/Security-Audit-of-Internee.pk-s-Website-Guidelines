# WEB-001 — SQL Injection

## Status

`Not Tested / Not Confirmed`

## Severity

`To Be Determined`

## OWASP Category

**A03 — Injection**

## Affected Component

```text
Application: [AUTHORIZED_TEST_APPLICATION]
Endpoint: [AUTHORIZED_ENDPOINT]
Parameter: [TEST_PARAMETER]
HTTP Method: [GET/POST]
```

## Description

SQL Injection occurs when untrusted input is incorporated into a database query without adequate validation or parameterization.

A successful SQL Injection vulnerability may allow an attacker to alter the intended database query and potentially access, modify, or delete information.

This finding should only be marked as confirmed after controlled testing against an authorized environment.

## Preconditions

* Written authorization to test the target
* Authorized staging/test environment
* Test account where required
* Non-production test data
* Appropriate security-testing tool

## Testing Method

Use OWASP ZAP or Burp Suite to identify potentially injectable parameters.

Testing should be:

* Performed only against the authorized test environment
* Non-destructive
* Limited to test data
* Carefully monitored for unintended impact

Do not attempt destructive database operations.

## Evidence

Store only sanitized evidence here.

```text
Request:
[REDACTED]

Response:
[REDACTED]

Observed behavior:
[DOCUMENT OBSERVATION]
```

Do not commit:

```text
Passwords
API keys
Session cookies
Database credentials
Personal information
Production data
```

## Impact

If SQL Injection is confirmed, potential impact may include unauthorized access to application data, modification of database records, or other database-level compromise depending on the application's database privileges.

The actual impact must be determined from controlled testing rather than assumed.

## Remediation

Recommended defensive measures include:

1. Use parameterized queries/prepared statements.
2. Avoid constructing SQL queries through string concatenation.
3. Apply server-side input validation.
4. Use least-privilege database accounts.
5. Avoid exposing database error details to users.
6. Use appropriate ORM/database security features.
7. Add security regression tests for affected parameters.

## Verification

After remediation, repeat the authorized test and confirm that:

* The vulnerable behavior no longer occurs.
* Input is handled safely.
* Database errors are not unnecessarily exposed.
* Existing application functionality continues to work.

## References

* OWASP Top 10 — A03: Injection
* OWASP SQL Injection Prevention Cheat Sheet

## Notes

This document is a finding template until a SQL Injection vulnerability has been verified. Do not report the issue as confirmed without sufficient evidence.
