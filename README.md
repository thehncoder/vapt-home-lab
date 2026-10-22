# VAPT Home Lab

A hands-on vulnerability assessment and web security testing
portfolio built with Kali Linux, Docker, and OWASP Juice Shop.

## Objectives
- Practise reconnaissance and service identification.
- Map web application routes and API endpoints.
- Explore OWASP Top 10 vulnerability classes in a controlled lab.
- Capture reproducible evidence and document test outcomes.
- Recommend mitigations and distinguish confirmed findings
  from observations that require further validation.

## Lab Architecture
- Attacker environment: Kali Linux
- Target: OWASP Juice Shop
- Runtime: Docker
- Target URL: http://127.0.0.1:3000
- Network exposure: Bound to localhost

The target is intentionally vulnerable and must remain local.
Do not expose it publicly.

## Tools
Nmap, curl, Firefox Developer Tools, Docker, Git.

## Work Completed
- Initial port and service reconnaissance.
- HTTP header and endpoint enumeration.
- CORS response-header review.
- Review of a profile-route error response.
- Review of the application's Prometheus-style metrics endpoint.
- Juice Shop challenges: DOM XSS, Bonus Payload, View Basket,
  and Login Admin.

## Project Structure
- `evidence/` — captured responses and test output
- `notes/` — scope, reconnaissance, and challenge results
- `reports/` — observations and finding reports
- `scripts/` — space for reproducible assessment scripts

## Reporting Approach
Reports distinguish observations, training challenge completions,
and independently validated vulnerabilities. Severity is not
assigned solely because a challenge is solved or an endpoint
returns a particular HTTP status.

See `notes/scope.md` for scope and safety rules.
See `notes/challenge-results.md` for the challenge summary.
See `reports/` for the current assessments.

## Safety
All testing is limited to the locally deployed training target.
No third-party systems are in scope. Do not commit credentials,
session tokens, cookies, or other secrets.
