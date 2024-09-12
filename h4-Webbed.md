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
    

## Vulnerable and Outdated Components Summary:

  - **Found in 27.96% of applications**, with an average incidence rate of 8.77%.
  - **Common issues**:
    - Using vulnerable, outdated, or unsupported software components.
    - Not knowing the versions of all components or dependencies used.
    - Failing to scan for vulnerabilities or patch components in a timely manner.
    - Not testing the compatibility of updated libraries.
    - Not securing component configurations.
  
  - **Prevention**:
    - Implement a patch management process.
    - Regularly inventory and monitor components and dependencies.
    - Use software composition analysis tools to automate vulnerability detection.
    - Remove unused components and features.
    - Obtain components from official sources and use signed packages.
    
  - **Example attacks**:
    - CVE-2017-5638: Struts 2 remote code execution vulnerability, causing major breaches.
    - IoT devices with unpatched vulnerabilities like Heartbleed are easily exploitable.


## Injection Summary:

  - **Found in 94% of applications**, with 274,000+ occurrences.
  - **Common types of injection**:
    - **SQL Injection (CWE-89)**: Example of vulnerable code:
  
      ```java
      String query = "SELECT * FROM accounts WHERE custID='" + request.getParameter("id") + "'";
      ```
  
      An attacker could modify the `id` parameter to inject SQL, like:
  
      ```http
      http://example.com/app/accountView?id=' UNION SELECT SLEEP(10);--
      ```
  
    - **Cross-site Scripting (CWE-79)**: Inserting malicious scripts in web pages to execute in other users' browsers.
    - **External Control of File Name/Path (CWE-73)**: Using untrusted input to control file paths.
  
  - **Vulnerable when**:
    - User-supplied data is not validated, filtered, or sanitized.
    - Dynamic queries or non-parameterized calls are used.
    - Hostile data is used in queries or commands.
  
  - **Prevention**:
    - Use **parameterized queries** and safe APIs to avoid interpreters.
    
      ```java
      String query = "SELECT * FROM accounts WHERE custID = ?";
      PreparedStatement pstmt = connection.prepareStatement(query);
      pstmt.setString(1, request.getParameter("id"));
      ```
  
    - Validate user input on the **server side**.
    - Escape special characters in dynamic queries.
    - Use SQL controls like `LIMIT` to minimize data exposure in case of injection.
