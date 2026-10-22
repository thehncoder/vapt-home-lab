# OBS-001: Permissive CORS Response Headers

- Target: Local OWASP Juice Shop
- Endpoint: /
- Additional endpoint: /rest/products/search?q=apple
- Observation: Both endpoints returned
  Access-Control-Allow-Origin: *
- Test origin: https://attacker.example
- Severity: Informational
- Status: Observed; security impact not demonstrated

## Evidence
See evidence/cors-check.txt.

## Analysis
The application permits cross-origin reads of the tested
responses. The observed content consisted of the public
homepage and product search results.

The wildcard header alone does not establish a vulnerability.
No exposure of sensitive information or authenticated
cross-origin action was demonstrated.

## Recommendation
Restrict cross-origin access to trusted origins where
cross-origin access is not intended. Review sensitive and
authenticated endpoints separately.

## Retest
Pending further testing.
