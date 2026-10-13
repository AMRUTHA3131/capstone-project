## Overview

This document summarizes the web application security issues investigated during the local DVWA assessment.

Severity must be based on confirmed behavior, potential impact, exploitability, and the tested configuration. The ratings below are placeholders until the findings have been verified.

| Finding | Severity | Status |
|---|---|---|
| SQL Injection | Low | Confirmed |
| Cross-Site Scripting (XSS) | Low | Confirmed |
| HTTP Security Headers | Informational | Observation |

## Severity Definitions

- Critical: Could enable exceptionally severe compromise of the application or its environment.
- High: Could cause significant unauthorized access or exposure of sensitive information.
- Medium: Could have meaningful impact but may require specific conditions or privileges.
- Low: Limited impact or difficult-to-exploit weakness.
- Informational: An observation that does not, by itself, establish a vulnerability.

## Risk Assessment Notes

### WEB-01: SQL Injection

Potential impact: Unauthorized database access or manipulation, depending on the vulnerable query and database permissions.

### WEB-02: Cross-Site Scripting

Potential impact: Unintended browser-side script execution and possible compromise of user interactions.

### WEB-03: HTTP Security Headers

Potential impact: Depends on the header and application behavior. A missing header alone does not necessarily demonstrate an exploitable vulnerability.

## Recommended Priority

Prioritize confirmed vulnerabilities that could allow unauthorized access to data or execution of untrusted code. Address the underlying application code first, then apply supporting security controls and perform retesting.
