## Project Name

Web Application Security Assessment and Incident Response Simulation

## Purpose

The purpose of this project is to practice beginner-level web application security testing, understand common vulnerabilities, recommend mitigations, and review available logs in a controlled lab.

## Objectives

1. Confirm that the local DVWA application is reachable.
2. Record HTTP status codes, redirects, and response headers.
3. Assess selected vulnerabilities using the application's training modules.
4. Record the steps performed, evidence, potential impact, and mitigation.
5. Review Docker and application logs where available.
6. Document the incident-response process.
7. Prepare a final report and organize evidence in GitHub.

## Scope

Target: DVWA running locally at `http://localhost:4280`.

Included activities:
- HTTP response inspection
- Security-header review
- Controlled SQL injection assessment
- XSS assessment
- Risk classification
- Mitigation planning
- Log review and incident-response documentation

Excluded activities:
- Testing public or third-party systems
- Attacking systems without authorization
- Destructive testing
- Collecting real users' credentials or personal information

## Tools

- Kali Linux
- Docker
- DVWA
- cURL
- Burp Suite
- GitHub

## Planned Workflow

1. Verify that DVWA is running.
2. Inspect HTTP responses and headers.
3. Review the application's accessible modules.
4. Perform selected tests in the authorized lab.
5. Save screenshots and observations.
6. Assess severity and business impact.
7. Document mitigations and retesting status.
8. Review available logs.

## Limitations

Results apply only to the tested local DVWA configuration and the tests actually performed. They should not be interpreted as a complete security assessment of a production application.
