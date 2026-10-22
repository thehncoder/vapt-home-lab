# FINDING-001: Horizontal Access to Another User's Basket

- Target: Local OWASP Juice Shop
- Feature: View Basket
- Category: Broken Access Control
- CWE: CWE-639 (Authorization Bypass Through User-Controlled Key)
- Status: Demonstrated in intentionally vulnerable training application
- Severity: Provisional; assess business impact before assigning a final rating

## Summary
The local Juice Shop View Basket challenge was marked solved.
During the test, the authenticated session returned basket data
for basket ID 6, associated with UserId 25.

## Evidence
- Basket 6 response: HTTP 200, status "success", id 6, UserId 25
- Second test account's own basket: id 7, UserId 26
- Juice Shop scoreboard displayed the View Basket challenge as solved

## Reproduction Context
Two test accounts were created in the locally hosted training
application. Their basket identifiers were 6 and 7. The View
Basket challenge was solved in the lab.

## Limitations
The captured response establishes the returned basket data and
the lab's challenge completion. Preserve the authenticated
cross-account request and response as supporting evidence before
treating this report as a fully reproducible independent finding.

## Impact
If an application allows an authenticated user to retrieve another
user's basket without an ownership check, basket contents and
associated data may be exposed.

## Remediation
Enforce server-side object-level authorization on every basket
read and update. Derive the permitted user from the authenticated
session and reject requests for baskets not owned by that user.
Do not rely solely on client-controlled basket identifiers.

## Retest
Pending independent verification of the ownership check.
