# CS305-Portfolio
## Briefly summarize your client, Artemis Financial, and its software requirements.
Artemis Financial is a financial services company managing sensitive client data including savings, retirement, and insurance plans. They needed a vulnerability assessment of their Java Spring Boot application to identify and fix security weaknesses.

## What did you do well when you found your client's software security vulnerabilities? Why is it important to code securely?
I tied each vulnerability to its exact location in the code, such as hardcoded credentials in DocData.java and missing authentication on REST endpoints. Secure coding protects client data, ensures regulatory compliance, and prevents breaches that damage trust.

## Which part of the vulnerability assessment was challenging or helpful?
Running the OWASP Dependency-Check was the most helpful — seeing real CVEs on Bouncy Castle 1.46 made the risk of outdated libraries concrete. Manually reviewing code for logic flaws that static tools miss was the most challenging.

## How did you increase layers of security? In the future, what would you use to assess vulnerabilities?
I recommended upgrading outdated libraries, adding Spring Security with JWT, enforcing input validation, and replacing hardcoded credentials with environment variables. In the future I'd use OWASP Dependency-Check alongside tools like SonarQube or Snyk.

## How did you make certain the code and software application were functional and secure?
Every finding in the mitigation plan maps to a specific vulnerability from either the manual review or the dependency-check report. Re-running the dependency-check after refactoring would confirm no new vulnerabilities were introduced.

## What resources, tools, or coding practices did you use that might be helpful in future assignments?
OWASP Dependency-Check, the NVD for CVE research, Spring Security, Bean Validation, SLF4J logging, and storing secrets in environment variables rather than hardcoding them.

## What might you show future employers from this assignment?
The vulnerability assessment report — specifically the manual review identifying seven vulnerabilities with exact file locations, and the mitigation plan connecting each fix to a specific finding.
