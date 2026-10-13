# Reconnaissance Notes

## Target Information

- Application: Damn Vulnerable Web Application (DVWA)
- Target URL: `http://localhost:4280`
- Environment: Local Docker lab
- Purpose: Initial web application inspection

## Checks Performed

### 1. Application Availability

The application was opened in a browser to confirm whether the local DVWA page could be reached.

### 2. HTTP Status and Redirects

The HTTP response was inspected using the `check_http.sh` script.

A redirect may occur when the application sends the browser to a login page or another route. The reason should be confirmed by reviewing the `Location` header and browser behavior.

### 3. HTTP Response Headers

The response headers were inspected using cURL.

Previously observed responses included `X-Content-Type-Options: nosniff`, `X-Frame-Options: SAMEORIGIN`, and `Referrer-Policy: strict-origin-when-cross-origin`. Confirm these again before treating them as the final results.

## Reconnaissance Summary

The reconnaissance stage established the initial behavior of the local application and identified the information required for further testing. The observations are limited to the responses and pages examined during this assessment.
