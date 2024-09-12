# x) Read and summarize OWASP: OWASP 10 2021


## Broken Access Control Summary:
- **Found in 94% of applications**, with 318,000+ cases.
- **Users can perform actions beyond their permissions**.

- **Common issues include**:
  - **Bypassing controls**: Changing URLs or parameters.
    
    ```java
    // Vulnerable code allowing access to other user’s data
    String userId = request.getParameter("userId");
    User user = userService.getUserById(userId);
    ```

  - **Viewing/editing others' data**: Directly accessing data not meant for the user.

  - **Missing API access protections**: Unrestricted access to POST, PUT, DELETE methods.
    
    ```java
    // Example of missing access control on API endpoints
    @PostMapping("/update")
    public ResponseEntity<String> updateData(@RequestBody Data data) {
        dataService.updateData(data);
        return ResponseEntity.ok("Data updated");
    }
    ```

  - **Privilege escalation**: Users gaining unauthorized access or admin rights.

- **Prevent by**:
  - **Implementing strict server-side controls**.
    
    ```java
    // Enforcing access control on server-side
    if (!user.hasPermission("admin")) {
        throw new AccessDeniedException("Access denied");
    }
    ```

  - **Denying access by default**.

  - **Logging and limiting access attempts**.
    
    ```java
    // Logging failed access attempts
    if (accessFailed) {
        logger.warn("Access attempt failed for user: " + userId);
    }
    ```

  - **Invalidating session tokens after logout**.
    
    ```java
    // Invalidate session token after logout
    session.invalidate();
    ```

## Security Misconfiguration Summary:

- **Found in 90% of applications**, with over 208,000 occurrences.

- **Common issues**:

  - **Missing security hardening across the stack**:
    
    ```bash
    # Disable unnecessary services and ports on a Linux server
    sudo systemctl stop <service_name>
    sudo systemctl disable <service_name>
    
    # Example: Disable HTTP service if not needed
    sudo systemctl stop httpd
    sudo systemctl disable httpd
    ```

  - **Unnecessary features, services, or ports enabled**:
    
    ```bash
    # List open ports on a Linux server
    sudo netstat -tuln
    
    # Example: Close an unnecessary open port (e.g., port 8080)
    sudo ufw deny 8080/tcp
    ```

- **Prevention**:

  - **Use a repeatable hardening process across environments (Dev, QA, Production)**.

  - **Remove unnecessary features and components**.
  
  - **Regularly review and update configurations, security patches, and cloud permissions**.
  
  - **Segment applications and use secure separation (e.g., containers, ACLs)**.
  
  - **Automate configuration checks and security testing**.

- **Example attacks**:

  - **Sample apps with security flaws left on production servers**.
    
    ```java
    // Example of insecure code with sample apps included
    // Ensure sample applications and default configurations are removed
    ```

  - **Directory listings not disabled, allowing access to sensitive files**:
    
    ```apache
    # Disable directory listing in Apache configuration
    <Directory /var/www/html>
        Options -Indexes
    </Directory>
    ```

    

## Vulnerable and Outdated Components Summary:

- **Found in 27.96% of applications**, with an average incidence rate of 8.77%.

- **Common issues**:

  - **Using vulnerable, outdated, or unsupported software components**:
    
    ```bash
    # Example: Check for outdated packages on a Debian-based system
    sudo apt list --upgradable
    
    # Update outdated packages
    sudo apt update
    sudo apt upgrade
    ```

  - **Not knowing the versions of all components or dependencies used**:
    
    ```bash
    # Example: List installed Python packages and their versions
    pip freeze
    
    # Example: List npm packages and their versions
    npm list --depth=0
    ```

- **Prevention**:

  - **Implement a patch management process**.
  
  - **Regularly inventory and monitor components and dependencies**.
  
  - **Use software composition analysis tools to automate vulnerability detection**.
  
  - **Remove unused components and features**.
  
  - **Obtain components from official sources and use signed packages**.

- **Example attacks**:

  - **CVE-2017-5638**: Struts 2 remote code execution vulnerability, causing major breaches.
  
  - **IoT devices** with unpatched vulnerabilities like Heartbleed are easily exploitable.


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

### References: OWASP Top 10:2021 (https://owasp.org/Top10/A01_2021-Broken_Access_Control/)
                OWASP Top 10:2021 (https://owasp.org/Top10/A01_2021-Broken_Access_Control/)
                OWASP Top 10:2021 (https://owasp.org/Top10/A01_2021-Broken_Access_Control/)
                OWASP Top 10:2021 (https://owasp.org/Top10/A01_2021-Broken_Access_Control/)
