# Guide to secure software development by @CodingCrisis
## Goal 
Ensure unified and successful completion of software construction by providing a shared understanding of how to develop a secure solution. 
## Security by design 
Security by design is an approach to software development that seeks to make systems as free of vulnerabilities and impervious to attack as possible through such measures as continuous testing, authentication safeguards and adherence to best programming practices. 
Security assurance should be a vital part of all stages of software development. This guide focuses on tips related to software construction. It assumes that any activities performed both earlier (e.g., modeling) and later (e.g., testing) are also executed with security in mind.
## Practical Secure development tips 
1. Leverage the security infrastructure provided by the platform being used (e.g., .NET). Apply secure coding guidelines if provided ([Security in .NET](https://learn.microsoft.com/en-us/dotnet/standard/security/)) 
1. Use safe communication techniques:
    * Reuse existing security solutions if possible 
    * Do not use methods/protocols considered unsafe (e.g., .NET remoting, TLS 1.0/1.1). 
    * New communication method/protocol should be always consulted with architects and analyzed in terms of security 
1. While considering 3rd Party components investigate: 
    * Level of available support (or at least active development) 
    * Potential vulnerabilities e.g. [Vulmon](https://vulmon.com/searchpage?q=*&sortby=bydate), [CVE](https://cve.mitre.org/)
    * Means of keeping up with updates/patches 
1. Always encrypt any sensitive data and communication channels; use secure ciphers 
1. Ensure credential security: 
    * Enforce strong passwords 
    * Prevent reusing passwords 
    * Avoid using common passwords 
    * Use multi-factor authentication 
    * Use secure error messages during log-in process 
1. All keys, passwords, and certificates need to be safely stored and protected: 
    * Only store salted & hashed user passwords 
    * Do not hardcode credentials in your code 
    * Use integrated authentication whenever possible 
    * Use respective credentials/certificate storage solutions specific to your type of project (Windows Certificate Store, DPAPI, Azure Key Vault etc.). 
1. Protect against top application security risks, as specified by OWASP; use techniques like: 
    * Validate any input to your application 
    * Use parameterized queries 
    * Carry out output data encoding (XML, JSON..) for presentation 
1. Employ proper means of session management, including safe cookies (OWASP Session Management) 
1. Pay attention to security-related compiler warnings 
1. Always check and inspect the security notes/issues/warnings provided by employed Code Quality Assurance Tools (e.g., SonarQube). 
