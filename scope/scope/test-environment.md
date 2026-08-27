# Test Environment Configuration

## Purpose

This document describes the security-testing environments used for the project.

## Environment 1: Internee.pk Staging

The Internee.pk staging environment must only be tested after explicit authorization has been granted.

### Environment Details

| Item                   | Value                          |
| ---------------------- | ------------------------------ |
| Application            | Internee.pk                    |
| Environment            | Staging/Test                   |
| Testing Type           | Authorized Security Assessment |
| Production Testing     | Not Allowed                    |
| Authorization Required | Yes                            |

### Allowed Testing Areas

* Authentication
* User profiles
* Authorized API endpoints
* Input validation
* Session handling
* Access control
* XSS
* SQL injection
* CSRF

## Environment 2: OWASP Juice Shop

OWASP Juice Shop is an intentionally vulnerable web application used for security training and testing.

### Local Deployment

A local instance can be started using Docker:

```bash
docker run --rm -p 3000:3000 bkimminich/juice-shop
```

After starting the application, access it locally at:

```text
http://localhost:3000
```

## Testing Tools

The following tools may be used:

* OWASP ZAP
* Burp Suite Community or Professional
* Browser Developer Tools
* Docker
* Manual testing techniques

## Safety Requirements

* Do not use production credentials.
* Use dedicated test accounts.
* Do not collect unnecessary personal data.
* Do not commit secrets to Git.
* Redact sensitive information from evidence.
* Use non-destructive testing techniques.
* Stop testing if unexpected system instability occurs.

## Test Account Format

Use dedicated accounts such as:

```text
Username: security.test.user
Email: security-test@example.invalid
Password: Stored securely and never committed to Git
```

## Environment Status

| Environment         | Authorization               | Status           |
| ------------------- | --------------------------- | ---------------- |
| Internee.pk Staging | Required                    | Pending Approval |
| OWASP Juice Shop    | Deliberately Vulnerable Lab | Available        |
