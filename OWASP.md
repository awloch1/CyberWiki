**Model IAAA:**
- Identity - the unique account
- Authentication - proving the identity
- Authorisation - what that identity is allowed to do 
- Accountability  - recording and alerting on who did what

### A01: Broken Access Control
Access control is broken when a user can access or modify data they should not have access to.
- **Horizontal** - access to another user's data without gaining extra privileges.
- **Vertical** - access to functions or actions intended for higher-privileged users (e.g., admin).

### A02: Security misconfiguration
Security misconfigurations happen when systems, servers, or applications are deployed with unsafe defaults, incomplete settings, or exposed services.
-  Unnecessary services or endpoints exposed to the internet
- Misconfigured cloud storage or permissions
- Unrestricted API access or missing authentication/authorisation

### A03: Software Suppply Chain Failures
Software supply chain failures happen when applications rely on components, libraries, services, or models that are compromised, outdated, or improperly verified.
- Using unverified or unmaintained libraries and dependencies
- Automatically installing updates without verification
- Insecure build pipelines or CI/CD processes that allow tampering

### A04 Cryptograpic Failures
Cryptographic failures happen when encryption is used incorrectly or not at all. This includes weak algorithms, hard-coded keys, poor key handling, or unencrypted sensitive data.
- Hard-coded secrets in code or configuration
- Poor key rotation or management practices
- Using deprecated or weak algorithms like MD5, SHA-1, or ECB mode

### A06 Insecure Design
Insecure design happens when flawed logic or architecture is built into a system from the start.
- Weak business logic controls, like recovery or approval flows
- Missing guardrails for LLMs and automation agents

### A07: Authentication F ailures
Authentication Failures happen when an application can’t reliably verify or bind a user’s identity. Common issues include
- No account lockout or rate limiting (brute-force attacks)
- Sessions that never expire
- No re-authentication for sensitive actions

### A09:  Logging & Alerting Failures
Security Logging and Monitoring Failures occur when applications fail to adequately log, monitor, or alert on security-related events. As a result, attacks may go undetected, making incident investigation and response difficult.
**Examples:**
- Missing logs for login attempts
- No alerts for suspicious activity
- Logs not monitored or reviewed
