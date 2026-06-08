## Secure Coding Concepts
- A balance between time and quality
  - Programming with security in mind is often secondary
- Testing is crucial, in the QA process
- Vulnerabilities will eventually be found

## Input validation
- What is the expected input vs what is sent by the user?
- Document all inputs methods
  - Forms, fields, type
- Check and correct all input normalization
  - A zip code should only be X characters long with a letter in the X
  - Fix any data with improper input
- The fuzzers will find what you missed
  - Dont give them an opening, by allowing them to input random strings of data

## Secure Cookies
- Information stored on your computer by the browser
- Used for tracking, personalization, session manageemnt
  - Not executable, not generally a security risk
  - Unless someone gets access to them
- Secure cookies have a Secure attribute set
  - Browser will only send it over HTTPS
- Sensitive information should not be saved in a cookie

## Static Code Analyzers
- Static Application Security Testing SAST
  - Help to identify security flaws
- mAny security vulnerabilities found easily
  - Buffer overflows, database injections, etc.
- Not everything can be identified via analysis
  - Authentication security, insecure cryptography
  - Dont rely on automation for everything
- Still have to verify each finding
  - False positives are an issue

## Code Signing
- An application is deployed
  - Users run application executable or scripts
- So amyn security questions
  - has the application been modified in any way?
  - Can you confirm that the application was written by a specific developer?
- The application code can be digitally signed by the developer
  - Asymmetric encryption
  - A trusted CA signs the developers public key
  - Developers signs the code with their private key
  - For internal apps, use your own CA

## Sandboxing
- Applications cannot access unrelated resources
  - They play intheir own sandbox
- Commonly used during development
- Can be a useful production technique
- Used in many different deployments and reduces attack surface
  - Virtual Machines
  - Mobile Devices
  - Browser iframes (Inline Frames9
  - Windows UAC
 
## Application Security Monitoring
- Real-time information
  - Application usage, access demographics
- View blocked attacks
  - SQL injection attemtps, patched vulnerabilities
- Audit the logs
  - Find the information gaterhing and hidden attacks
- Anomaly detection
  - Unusual file transfers
  - Increase in client access
