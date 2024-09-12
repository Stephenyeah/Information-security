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
