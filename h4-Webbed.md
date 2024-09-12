# x) Read and summarize OWASP: OWASP 10 2021


## Broken Access Control Summary:
  - **Found in 94% of applications**, with 318,000+ cases.
  - **Users can perform actions beyond their permissions**.
  - Common issues include:
    - Bypassing controls by changing URLs or parameters.
    - Viewing/editing others' data.
    - Missing API access protections (POST, PUT, DELETE).
    - Privilege escalation (user gaining admin rights).
  - **Prevent by**:
    - Implementing strict server-side controls.
    - Denying access by default.
    - Logging and limiting access attempts.
    - Invalidating session tokens after logout.

## Security Misconfiguration Summary:

    - **Found in 90% of applications**, with over 208,000 occurrences.
    - **Common issues**:
      - Missing security hardening across the stack.
      - Unnecessary features, services, or ports enabled.
      - Default accounts and passwords left unchanged.
      - Exposing overly informative error messages (e.g., stack traces).
      - Outdated or insecure configurations (e.g., server settings, libraries).
      - Missing security headers or directives.
      - Outdated software versions with vulnerabilities.
    
    - **Prevention**:
      - Use a repeatable hardening process across environments (Dev, QA, Production).
      - Remove unnecessary features and components.
      - Regularly review and update configurations, security patches, and cloud permissions.
      - Segment applications and use secure separation (e.g., containers, ACLs).
      - Automate configuration checks and security testing.
    
    - **Example attacks**:
      - Sample apps with security flaws left on production servers.
      - Directory listings not disabled, allowing access to sensitive files.
      - Exposing detailed error messages to users.
      - Cloud storage with default open permissions, allowing unauthorized data access.
