# Vulnerability Findings

This directory contains documented security findings identified during authorized testing.

## Finding Format

Each vulnerability should be documented using the following information:

| Field              | Description                                   |
| ------------------ | --------------------------------------------- |
| Finding ID         | Unique identifier, e.g. `WEB-001`             |
| Title              | Name of the vulnerability                     |
| Severity           | Critical, High, Medium, Low, or Informational |
| OWASP Category     | Relevant OWASP classification                 |
| Affected Component | Page, API, or application component           |
| Description        | Explanation of the security issue             |
| Preconditions      | Requirements needed to reproduce it           |
| Evidence           | Sanitized testing evidence                    |
| Impact             | Potential security consequences               |
| Remediation        | Recommended fix                               |
| Verification       | Whether the fix was retested                  |

## Severity Levels

### Critical

A vulnerability that could result in severe compromise, such as broad unauthorized access or remote code execution.

### High

A vulnerability that could significantly affect confidentiality, integrity, or availability.

### Medium

A vulnerability with a meaningful but more limited security impact.

### Low

A weakness with limited security impact or requiring uncommon conditions.

### Informational

A security observation or improvement that does not represent a directly exploitable vulnerability.

## Finding Naming Convention

Use the following format:

```text id="v9v7pu"
WEB-001
WEB-002
WEB-003
```

## Evidence Requirements

Evidence should be:

* Reproducible
* Minimal
* Sanitized
* Relevant to the finding
* Free of real credentials and personal information

Do not include passwords, session tokens, API keys, or private user information.

## Recommended Finding Files

```text id="4q7j2m"
vulnerabilities/
├── README.md
├── WEB-001-sql-injection.md
├── WEB-002-xss.md
├── WEB-003-csrf.md
├── WEB-004-authentication.md
└── WEB-005-access-control.md
```

Only create a finding after the issue has been verified in an authorized test environment.
