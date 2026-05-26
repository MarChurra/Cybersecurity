## Security in the cloud
- Cloud adoption has been nearly universal
- We´ve put sensitive data in the cloud
- We´re not putting in the rigth protectionsSimple best-practices are not being used, with several unpatched code in production and CVSS of 7.0 or higher

## Attack the Service
- DoS Denial of Service
- A fundamental attack type
- Authentication bypass
  - Take advantage of weak or faulty authentication
- Directory Traversal
  - Faulty configurations put data at risk
- Remote Code Execution
  - Take advantage of unpatched systems

## Attack the application
- Web application attacks have increased
  - Log4j and Spring Cloud Function
  - Easy to exploit, rewards are extensive
- CSS Cross-site Scripting
  - Take advantage of poor input validation
- Out of bounds write
  - Write to unauthorized memory areas
  - Data corruption, crashing, or code execution
- SQL Injection
  - Get direct access to a database 
