# FINDING-002: Login Admin Challenge

- Target: Local OWASP Juice Shop
- Category: Injection / Authentication
- Status: Challenge solved in intentionally vulnerable training application
- Severity: Not assigned; this is a training result, not a production assessment

## Summary
Juice Shop displayed a success notification confirming completion
of the "Login Admin" challenge.

## Evidence
- Record the scoreboard success notification.
- Capture the relevant request and response from Firefox Network
  tools, removing credentials, cookies, and authorization tokens.

## Security Relevance
If an authentication endpoint accepts crafted input that changes
the intended query logic, an attacker may bypass authentication.
The exact root cause should be confirmed from the challenge's
reproduction steps and request evidence.

## Remediation
Use parameterized database queries, validate input appropriately,
and apply secure authentication and authorization controls.

## Limitations
The challenge completion message alone does not establish the
exact injection mechanism. Preserve the reproduction details
before claiming a confirmed SQL injection finding.

## Retest
Pending evidence capture.
