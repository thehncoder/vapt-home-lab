# OBS-002: Profile Route Blocks Request from Docker Client Address

- Target: Local OWASP Juice Shop
- Endpoint: /profile
- Observed response: HTTP 500
- Reported client address: ::ffff:172.17.0.1
- Status: Observed; security impact not demonstrated
- Severity: Informational (provisional)

## Evidence
- evidence/profile-headers.txt
- evidence/profile-response.txt
- Container logs showing the block and stack trace

## Observation
A request to /profile returned an HTTP 500 error page stating
"Blocked illegal activity by ::ffff:172.17.0.1". The stack trace
references build/routes/userProfile.js:69:18.

## Assessment
This establishes that the request was blocked and an error page
was returned. It does not establish a security vulnerability.
The cause and intended behavior have not been independently
verified.

## Recommendation
Review the application's route logic and error handling. Avoid
exposing internal stack traces in production responses.

## Retest
Pending.
