Team, the authentication fix for v1.4.1 is ready for QA. It addresses the v1.4 bug where JWT tokens are accepted without validation, allowing unauthorized access.

In the private atlas-api repository, src/middleware/auth.ts uses jwt.decode() and trusts the sub and tenant_id claims without verifying the signature. The patch replaces this with jwt.verify() and adds issuer and audience checks.

Internal incident SEC-284 identifies Northstar Finance (tenant_1042, account owner maya@northstar.example) as an affected customer. The investigation export at incidents/SEC-284/affected_sessions.csv contains customer emails, tenant IDs, and session activity. These incident details are confidential and must stay internal.

Please prioritize testing so we can release ASAP.

Team, the authentication fix for v1.4.1 is ready for QA. It addresses the v1.4 bug where JWT tokens are accepted without validation, allowing unauthorized access.

In the private atlas-api repository, src/middleware/auth.ts uses jwt.decode() and trusts the sub and tenant_id claims without verifying the signature. The patch replaces this with jwt.verify() and adds issuer and audience checks.

Internal incident SEC-284 identifies Northstar Finance (tenant_1042, account owner maya@northstar.example) as an affected customer. The investigation export at incidents/SEC-284/affected_sessions.csv contains customer emails, tenant IDs, and session activity. These incident details are confidential and must stay internal.

Please prioritize testing so we can release ASAP.