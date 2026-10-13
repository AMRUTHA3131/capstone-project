# Task 5: Web Application Security Assessment and Incident Response Simulation

## Project Overview

This project focuses on assessing a deliberately vulnerable web application in a controlled local lab environment. The objective is to understand common web application security weaknesses, document findings, recommend mitigations, and practice basic incident-response procedures.

The assessment uses Damn Vulnerable Web Application (DVWA), which is designed for security training and practice.

## Objectives

- Identify basic information about the local web application.
- Inspect HTTP responses and security-related headers.
- Test selected web application vulnerabilities in the authorized lab.
- Document evidence, impact, risk, and recommended mitigations.
- Review available application and container logs.
- Practice a simple incident-response workflow.
- Maintain clear technical notes and evidence in GitHub.

## Tools Used

- Kali Linux
- Docker
- DVWA
- Browser
- cURL
- Burp Suite, if available
- Git and GitHub
- Docker container logs

## Lab Scope

- Application: DVWA
- Local URL: `http://localhost:4280`
- Environment: Local Docker lab
- Authorized target: The DVWA instance running on the local machine

Testing is limited to this intentionally vulnerable local application. No third-party websites or systems are targets.

## Repository Structure

- `Planning/` — project objectives, scope, and schedule
- `Methodology/` — testing approach and procedure
- `Scripts/` — scripts for inspecting HTTP responses and headers
- `Reconnaissance/` — initial observations
- `Findings/` — vulnerability assessment notes and risk summary
- `Mitigations/` — recommended remediation measures
- `Incident-Response/` — log review and incident-response notes
- `Screenshots/` — evidence captured during testing
- `Diagrams/` — project and incident-response diagrams
- `Report/` — final assessment report

## How to Use the Scripts

Make the scripts executable:

```
chmod +x Scripts/check_http.sh Scripts/check_headers.sh
```

Run the HTTP response check:

```
./Scripts/check_http.sh
```

Run the security-header check:

```
./Scripts/check_headers.sh
```

These scripts inspect the local DVWA instance. They do not exploit vulnerabilities.

## Key Deliverables

- Project plan and testing methodology
- HTTP response and header observations
- SQL injection and XSS assessment notes
- Risk summary and mitigation recommendations
- Incident-response and log-review notes
- Screenshots and final report

## Results

Actual results and supporting evidence are documented in the relevant folders. Findings should be considered confirmed only when supported by observed behavior or recorded evidence.
