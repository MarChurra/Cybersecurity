- Pentest
  - Simulate an attack
- Similar to vulnerability scanning
  - Expect we actually try to exploit the vulnerabilities
- Often a compliance mandate
  - Regular penetration testing by a 3rd-party
- National Institute of Standards and Technology Technical Guide to Information Security and Assesment

## Rules of engagement
- An important document
  - Defines purpose and scope
  - Makes everyone are of the test parameters
- Type of testing and schedule
  - On-site physical breach, internal test, external test
  - Normal working hours, after 6PM, etc.
- The rules
  - IP address ranges
  - Emergency contacts
  - how to handle sensitive informaiton
  - In-scope and out-of-scope devices or applications

## Exploiting Vulnerabilities
- Try to break into the system
  - Be careful, since this can cause a DoS or loss of data
  - Buffer overflows can causa instability
  - Gain privilege escalation
- You may need to try many different vulnerability types
  - Password brute-force
  - Social engineering
  - Databse Injections
  - Buffer overflows

## The process
- Initial exploration
  - Get into the network
- Lateral movement
  - Move from system to system
  - The inside of the network is relatively unprotected
- Persistence
  - Once you are there, you need to make sure there is a way back in
  - Set up a backdoor, build user accounts, change or verify default passwords
- The pivot
  - Gain access to system would normally not be acessible
  - Use a vulnerable system as a proxy or relay
 
## Responsible disclosure program
- It takes time to fix a vulnerability
  - software changes, testing, deployment, etc.
- Bug bounty Programs
- A controlled information release
  - Researcher reports the vulnerability
  - Manufacturer creates a fix
  - The vulnerability is announced publicly 
