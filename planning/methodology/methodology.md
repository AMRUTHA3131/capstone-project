# Methodology

## Preparation and Scope

The assessment was performed against a local DVWA instance running through Docker. The target URL was `http://localhost:4280`.

Before testing, the application and its containers were checked to confirm that the intended lab was running.

## Reconnaissance

The initial review focused on:
- Whether the application was reachable
- HTTP status codes
- Redirect behavior
- Response headers
- Whether authentication was required
- Which modules were accessible

Tools: Browser and CURL.

## HTTP and Header Inspection

The response from the local application was inspected to identify server responses and security-related headers.

The presence or absence of a header was recorded as an observation. A missing header alone was not treated as proof of an exploitable vulnerability.

## Vulnerability Assessment

### SQL Injection

The SQL injection training module was assessed using a controlled test input within DVWA. The response was observed to determine whether input handling affected the database query.

Evidence included the test input, application response, and screenshot where available.

### Cross-Site Scripting (XSS)

The XSS training module was assessed using a harmless test payload within DVWA. The result was recorded only after observing the actual browser behavior.

The assessment distinguished between text being displayed normally and input being executed as browser-side script.

## Risk Assessment

Each finding was evaluated based on:
- Potential impact
- Ease of exploitation in the tested configuration
- Required privileges or access
- Potential confidentiality, integrity, and availability consequences

Severity ratings are preliminary unless a formal scoring method and sufficient evidence are available.

## Mitigation Planning

Recommendations were selected according to the weakness observed. Examples include parameterized SQL queries, context-aware output encoding, input validation, secure session handling, and appropriate security headers.

A recommendation is not considered implemented merely because it appears in this report.

## Incident-Response Simulation

The incident-response exercise followed these general stages:
1. Identify suspicious activity or a potential security issue.
2. Record the time, affected component, and available evidence.
3. Review relevant application and container logs.
4. Assess the potential impact.
5. Identify containment and remediation actions.
6. Retest and document the result.

No production incident was involved. This was a training exercise.

## Limitations

The assessment was limited to the local lab, selected modules, and tests actually performed. The results may differ in other DVWA security levels or application configurations.
