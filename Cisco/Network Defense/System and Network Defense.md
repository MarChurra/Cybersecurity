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
- A validation rule checks that data falls within the parameters defined by the database designer. A validation rule helps to ensure the completeness, accuracy and consistency of data.
- The criteria used in a validation rule include the following:
  - Size: Checks the numbers of characters in a data item
  - Format: Checks that the data conforms to a specific format
  - Consistency: Checks for the consistency of odes in related data items.
  - Range: Checks that data lies within a minimum and maximum value
  - Check digit: provides for an extra caltucation to generate a check digit for error detection.
 
### Integrity Checks
- Compromised data can threaten the security of your devices and systems.
- An inteigty check can measure the consistency of data in a file, to ensure that it has not been corrupted.
- The inteigrty check performs a hash function, to take a snapshot of data and then uses this snapshot to ensure data has remained unchanged.
- A cheksum is an example of a hash function.
- Use of version control, meaning that two users cannot update the same object, at the exact same time. While keeping a log of past versions of the file.
- The utilization of Backups (need to be verified regularly) and Authorization.

### Other Application Security Practices
- Code Signing: Helps prove that a piece of software is authentic. Executables designed to install and run on a device are digitally signed to validate the author´s identity and provide assurance that the software code has not changed since it was signed.
- Secure Cookies: Protect information stored in cookies from hackers. This means using HTTPS tow ork with cookies.

## Network Hardening: Services and Protocols

### Network and Routing Services
- Cybercriminals use vulnerable network services to attack a device or to use it as part of an attack. To check for insecure network services, use a port scanner to detect open ports on a device. A port scanner sends a message to each port and waits for a response, which indicates how the port is used and whether it is open.
- But beware, cybercriminals also use port scanners for this same reason! Securing network services ensures that only necessary ports are exposed and available.
- Here are some precautions to ensure:
  
  - DHCP:
    - Secure the DHCP server physically, apply software patches.
    - Locate the DHCP server behind a firewall
    - Minitor DHCP activity by reviewing DHCP logs.
    - Maintain a strong antirivurs solution
    - Uninstall any unusued services and applications
    - Close unsued ports
      
- DNS:
  - Attackers can target DNS servers to deny access to network recoures or redirect traffic to rogue websites.
  - Use secure service and authentication between DNS servers to protect them from these attacks.
  - DNS Security Extensions uses digital signatures to strengthen authentication and protect against threats to the DNS.
  - Keep the DNS software up to date.
  - Prevent version string from revealing information.
  - Separate internal and external DNS servers.
  - Restrict allowed transactions by client IP address
  - Use transaction signatures to authenticate transactions.
  - Disable or restrict zone transfers and dynamic updates.
  - Enable logging and analyze logs
  - Use Domain Name SYstem Security Extensions
  - Sign Zones
 
- ICMP:
  - Network device uses ICMP to send error messages, that a requested service is not available or the host could not reach the router.
  - The ping command is a network utility that uses ICMP to test the reachability of a host on a network. Ping sends ICMP messages to the host and waits for a reply. Cybercriminals can alter the use of ICMP to run reconnaissance, denial of service (DoS) and covert channel attacks. Many networks filter ICMP requests to prevent such attacks.
- Routing Information Protocol RIP:
  - RIP is a routing protocol that limits the number of hops from source to destination that are allowed in a network path. The maximum number of hops allowed for RIP is fifteen. RIP is used to exchange routing information about which networks each router can reach and how far away those networks are.
  -  RIP calculates the best route based on hop count, but cybercriminals can also target routers and the RIP protocol. Such attacks on routing services can affect performance and availability, some attacks can even result in traffic redirection. Use secure services with authentication and implement system patching and updates to protect routing services.
- NTP:
  - Having the correct time within networks is important. Correct timestamps accurately track network events such as security violations. Additionally, clock synchronization is critical for the correct interpretation of events within syslog data files as well as for digital certificates.
  - Network Time Protocol (NTP) is a protocol that synchronizes network computer system clocks. NTP allows network devices to synchronize their time settings with an NTP server. Cybercriminals attack timeservers to disrupt secure communication that depends on digital certificates and to hide attack information. Use NTP Authentication to verify that the server is trusted.
 
### Telnet, SSH, and SCP
- Secure Shell (SSH) is a protocol that provides a secure (encrypted) remote connection to a device. Telnet is an older protocol that uses unsecure plaintext when authenticating a device (user name and password) and transmitting data. SSH should be used rather than Telnet to manage connections, as it provides strong encryption. SSH uses TCP port 22. Telnet uses TCP port 23.
- Secure copy (SCP) securely transfers files between two remote systems. SCP uses SSH for data transfer and authentication, ensuring the authenticity and confidentiality of the data in transit.

## Network Hardening: Segmentation

### Virtual Local Area Networks
- A VLAN segments the network and creates a secure area for the sensitive data.
- VLANs provide a way to group devices within a LAN and on individual switches.
- VLANs are based on logical connections, while LANs are based on physical connections.
- Other ports can be used to physically interconnect switches and allow multiple VLAN traffic between switches. These ports are called trunks.
