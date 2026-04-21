## Physical Security

### Fencing and Physical Barriers 
- Physical Barriers:
  - Perimeter fence system
  - Security gate system
  - Bollards
  - vehicle entry barriers
  - Guard shelters
  - Fencing
 
- Fencing:
  - A barrier that encloses secure areas and designates boundaries.
 
- High-security areas often require a ‘top guard’ such as barbed wire or concertina wire. Top guards act as an additional deterrent and can delay the intruder by causing severe injury. However, attackers can still use a blanket or mattress to alleviate this threat.
- Local regulations may restrict the type of fencing system an organization can use and it’s important to remember that fences require regular maintenance. Animals may burrow under the fence or the earth may wash out, leaving the fence unstable — this would lead to easy access for an intruder. Fencing systems should be inspected regularly.
- Moreover, vehicles should never be parked near a security fence, as this could assist the intruder in climbing over or causing damage to the fence.

### Biometrics
- Biometrics are the physiological or behavioral characteristics of an individual, and there are security practices based on identifying and granting access using biometrics.
- These can include measurement of the face, fingerprint, hand geometry, iris, retina, signature and voice.
- Biometric technologies can be the foundation of highly secure identification and personal verification solutions. The popularity and use of biometric systems have increased because of the rise in security breaches and transaction fraud.
- It is necessary to have into account as factors to consider which one to implement:
  - Accuracy
  - Speed or throughput rate
  - Acceptability to users
  - Uniqueness of the biometric organ and action
  - Ressistance to counterfeiting
  - Reliability
  - Data storage requirements
  - Enrollment time
  - Intrusiveness of the scan
- Accuracy is one of the most important, which is expressed in error types and rates.
- The first error rate is Type I errors or false rejections. These reject a person that registers and is an authorized user.
- However, in many biometric applications, particularly retail or banking, false rejections can have a negative impact on business due to a transaction or sale being lost.
- False acceptance is a Type II error. These allow entry to people who should not have entry meaning a cybercriminal can potentially gain access. These are considered the most important error for a biometric access control system.
- The acceptance rate is also an important concept here. Stated as a percentage, it is the rate at which a system accepts unenrolled individuals or imposters as authentic users. The rate of Type II errors per ttoal instances of granting permission.

### Badges and Access Logs
- An access badge allows an individual to gain access to an area with automated entry points.

### Surveillance
- Many physical access controls, including deterrent and tection systems, ultimately rely on people to intervene and stop the actual attack or intrusion.
- This can also include Video and Electronic Surveillance. These should be placed at all entrances, exits, loading bays, stairwells and refuse collection areas, in highly secure environments.
- Guards and Escorts
- RFID and Wireless Surveillance

## Application Security
- To maintain security at all stages of app development, a robust process needs to be followed:
  - Developing and Testing
  - Staging and production
  - Provisioning and deprovisioning
 
### Security Coding Techniques
- When coding applications, developers use several techniques to validate that all security requirements have been met.
  - Normalization: Organizes data in a DB and help maintain data integrity. Normalizaion converts an input string to its simplest known form to ensure that all strings have unique binary representations and that any malicious input is identified.
  - Stored procedure: A stored procdure is a group of precompiled SQL statements stored in a DB that executes a task. If you use a stored procedure to accept input parameters from clients using different input data, you will reduce network traffic and get faster results.
  - Obfuscation and camouflage: A developer can use obfuscation and camouflage to prevent software from being reverse engineered. Obfuscation hides original data with random characters or data. Camouflage replaces sensitive data with realistic ficitonal data.
  - Code reuse: Using existing software to build new software, saving time and development costs. Care must be taken, to avoid introduction of vulnerabilities.
  - SDKs: Third-party libraries and SDKs provide a repository of useful code to make app development faster and cheaper. The downside is that any vulnerabilities in SDKs or 3rd party libraries can potentially affect many applications.
 
### Input Validation
- Controlling the data input process is key to maintaining database integrity.
-  Many attacks run against a database and insert malformed data.
-  Such attacks can confuse, crash or make the application divulge too much information to the attacker.
-  Customers fill out a web application form to subscribe to a newsletter. A database application automatically generates and sends email confirmations back to the customers. When customers receive the email with a URL link to confirm their subscription, attackers have modified the URL link.
-  These modifications can change the username, email address or subscription status of the customers when they click to confirm their subscription. This way, when the email is returned to the host server, it receives bogus information, which it might not be aware of if it does not check each email address against subscription information.
-  Hackers can automate this attack to flood the web application with thousands of invalid subscribers to the newsletter database.

### Validation Rules
- 
  - 
