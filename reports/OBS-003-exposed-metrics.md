# OBS-003: Unauthenticated Application Metrics Exposure

- Target: Local OWASP Juice Shop
- Endpoint: /metrics
- Method: GET
- Observed response: HTTP 200 OK
- Content type: Prometheus text format
- Authentication: No authentication supplied
- Status: Exposure observed; impact assessment pending
- Severity: Informational (provisional)

## Summary
A request to the /metrics endpoint returned application and
runtime telemetry without requiring authentication.

## Evidence
- evidence/metrics-check.txt

## Observed Data
The response included:
- HTTP request counts grouped by status code
- Application startup timings
- Node.js process CPU and memory metrics
- Challenge counts grouped by category and difficulty
- Registered-user and social-interaction counters

## Security Impact
Depending on the deployment and surrounding controls, exposed
metrics may disclose operational details that help an attacker
understand application behavior. No direct compromise or
sensitive individual-user data exposure was demonstrated.

## Recommendation
Restrict metrics endpoints to trusted monitoring systems or
require appropriate authentication and network access controls.
Expose only metrics necessary for monitoring.

## Retest
Pending.
