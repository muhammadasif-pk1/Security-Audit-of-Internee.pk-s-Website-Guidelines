# Security Testing Authorization and Scope

## Purpose

This document defines the authorization, boundaries, and rules for the web application security assessment.

## Target Environments

### Primary Target

**Internee.pk staging/test environment**

Testing is permitted only after written authorization has been obtained from the system owner or authorized representative.

### Training Target

**OWASP Juice Shop**

OWASP Juice Shop may be used as a deliberately vulnerable application for security-testing practice.

## In-Scope Areas

The authorized assessment may cover:

* Login and authentication
* Registration
* Password-reset functionality
* User profiles
* Access-control mechanisms
* API endpoints
* Session management
* Input validation
* XSS testing
* SQL injection testing
* CSRF testing
* Security headers
* Error handling
* General security configuration

## Out-of-Scope Activities

The following activities are prohibited unless explicitly authorized:

* Testing production systems
* Denial-of-service testing
* Destructive database operations
* Deleting or modifying real user data
* Accessing other users' private information
* Credential theft
* Persistence mechanisms
* Malware deployment
* Social engineering
* Attacking third-party services
* Automated high-volume attacks

## Data Handling

Only the minimum data necessary to demonstrate a confirmed vulnerability should be collected.

Sensitive information must be:

* Redacted from screenshots
* Removed from HTTP request/response examples
* Excluded from Git history
* Stored only in approved private locations
* Deleted when no longer required

Examples of information that must not be committed to the repository include:

```text
Passwords
Session cookies
JWT tokens
API keys
Email addresses
Phone numbers
Personal identification data
Database credentials
Private user records
```

## Testing Rules

1. Confirm authorization before testing.
2. Stay within the defined scope.
3. Use non-destructive test cases.
4. Avoid unnecessary collection of sensitive information.
5. Stop testing if unexpected impact occurs.
6. Record findings accurately.
7. Sanitize evidence before storing it.
8. Report critical findings promptly.

## Approval

**Organization:** Internee.pk

**Environment:** Staging/Test

**Authorized By:** ______________________

**Authorization Date:** __________________

**Testing Start Date:** __________________

**Testing End Date:** ____________________

**Tester:** ______________________________

## Status

Authorization status:

`PENDING / APPROVED / COMPLETED`

> Do not begin testing the Internee.pk environment until authorization has been confirmed.
