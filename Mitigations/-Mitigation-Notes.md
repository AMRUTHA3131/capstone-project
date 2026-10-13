# Mitigation Notes

## Purpose

This document records recommended actions for addressing the weaknesses investigated during the local web application security assessment.

A mitigation is considered verified only after the relevant change has been implemented and retested.

## SQL Injection

### Actions

- Use prepared statements and parameterized queries.
- Do not concatenate untrusted input into SQL statements.
- Validate input according to the expected data type and format.
- Restrict database privileges to the minimum required.
- Avoid exposing detailed SQL errors to users.

### Verification

1. Review the relevant application code, if available.
2. Confirm that database input is parameterized.
3. Repeat the original test in the authorized lab.
4. Confirm that input cannot alter the intended query logic.
5. Record the result and screenshot or code evidence.

## Cross-Site Scripting

### Actions

- Encode output according to its HTML, attribute, JavaScript, or URL context.
- Prefer safe templating mechanisms.
- Avoid unsafe DOM APIs when processing untrusted content.
- Sanitize content if HTML input is intentionally supported.
- Consider Content Security Policy as an additional protective layer.

### Verification

1. Identify the affected input and output location.
2. Implement the appropriate encoding or sanitization.
3. Repeat the original harmless test.
4. Confirm that the browser no longer executes unintended script.
5. Record the result.

## HTTP Security Headers

Review the actual response headers and application requirements.

Possible controls include:
- `Content-Security-Policy`: Helps restrict permitted content sources.
- `X-Content-Type-Options: nosniff`: Helps prevent MIME-type sniffing.
- `Referrer-Policy`: Controls referrer information sent by the browser.
- `Strict-Transport-Security`: Helps enforce HTTPS when the application is deployed over HTTPS and the configuration is appropriate.
- `X-Frame-Options` or an appropriate Content Security Policy `frame-ancestors` directive: Helps control framing.
  
## General Application Hardening

- Keep application dependencies updated.
- Use secure session management.
- Apply least-privilege access controls.
- Disable unnecessary services and debug features.
- Avoid exposing sensitive errors.
- Monitor relevant logs.
- Back up important data and test recovery procedures.

## Conclusion

The recommended controls reduce the likelihood and impact of common web application vulnerabilities. Actual remediation status must be supported by implementation evidence and retesting.
