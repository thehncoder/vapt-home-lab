# OWASP Juice Shop Challenge Results

## Environment
- Target: Local OWASP Juice Shop in Docker
- URL: http://127.0.0.1:3000
- Scope: Intentionally vulnerable local training application
- Date: 2026-10-22

## Completed Challenges
- DOM XSS: solved
- Bonus Payload: solved
- View Basket: solved
- Login Admin: solved

## Access-Control Test
Two local test accounts were used:
- Account 1: basket ID 6, UserId 25
- Account 2: basket ID 7, UserId 26

The View Basket challenge was marked solved by Juice Shop.
The captured response for basket 6 returned HTTP 200 and UserId 25.
The direct unauthenticated request returned HTTP 401 because no
Authorization header was present.

The authenticated cross-account request should be preserved
separately before claiming independent reproduction of the issue.

## XSS Tests
DOM XSS and Bonus Payload were accepted by the training application.
These are lab challenge results, not evidence of a vulnerability
in a production application.

## Login Admin
The training application marked Login Admin as solved.
Capture and preserve the relevant request and response, with
credentials and tokens removed, before asserting the exact
injection mechanism independently.

## Reporting Standard
Challenge completion is not automatically equivalent to a fully
validated standalone vulnerability report. Findings must include
reproducible steps, supporting evidence, impact, and remediation.
