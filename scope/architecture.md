# Security Testing Architecture — Internee.pk

## Objective

The objective of this project is to identify web application vulnerabilities and improve data protection for Internee.pk.

Security testing should be performed only on the **authorized Internee.pk staging environment** or on deliberately vulnerable applications such as **OWASP Juice Shop**.

---

## 1. Testing Architecture

```text
                    ┌──────────────────────┐
                    │   Security Tester    │
                    └──────────┬───────────┘
                               │
                    OWASP ZAP / Burp Suite
                               │
                               ▼
                 ┌─────────────────────────┐
                 │   Staging Web Application│
                 │      Internee.pk        │
                 └────────────┬────────────┘
                              │
              ┌───────────────┼────────────────┐
              │               │                │
              ▼               ▼                ▼
        ┌──────────┐    ┌───────────┐    ┌──────────┐
        │  Login   │    │ User      │    │   APIs   │
        │  Pages   │    │ Profiles  │    │          │
        └──────────┘    └───────────┘    └──────────┘
                              │
                              ▼
                       ┌─────────────┐
                       │  Database   │
                       └─────────────┘
