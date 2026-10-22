# VAPT Home Lab

A practical Vulnerability Assessment and Penetration Testing
lab built with Kali Linux, Docker, and OWASP Juice Shop.

## Objectives
- Perform network reconnaissance and service identification.
- Explore web application functionality and APIs.
- Practise authorised OWASP Top 10 security testing.
- Collect reproducible evidence.
- Document risk, impact, and remediation.

## Environment
- Attacker: Kali Linux
- Target: OWASP Juice Shop
- Container runtime: Docker
- Target URL: http://127.0.0.1:3000
- Exposure: Localhost only

## Tools
Nmap, curl, Docker, Burp Suite, Git.

## Methodology
1. Confirm scope and authorisation.
2. Verify target availability.
3. Perform reconnaissance and enumeration.
4. Test selected vulnerabilities manually.
5. Validate findings and capture evidence.
6. Document impact and remediation.
7. Retest fixes where possible.

## Evidence
Initial reconnaissance evidence is stored in `evidence/`.
Reports are stored in `reports/`.

Only verified findings will be reported. No vulnerability
is claimed without supporting evidence.

## Safety
Testing is restricted to the local, intentionally vulnerable
target. Do not expose it publicly or test unauthorised systems.
