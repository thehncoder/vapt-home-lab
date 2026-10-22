# Initial Reconnaissance

## Scope
Target: OWASP Juice Shop
Base URL: http://127.0.0.1:3000
Environment: Local Docker container
Authorisation: Self-hosted training target

## Nmap Results
- Host: 127.0.0.1
- Port: TCP/3000
- State: Open
- Service identification: Inconclusive

## Interpretation
The target is reachable and accepts TCP connections on port 3000.
Nmap did not conclusively identify the application protocol.
HTTP response headers and application endpoints are being
examined to confirm the service and map the attack surface.

## Status
Initial reconnaissance only. No vulnerability confirmed yet.
