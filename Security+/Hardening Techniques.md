## System Hardening
- Many and varied
  - Windows, Linux, IOS, Android...
- Updates
  - OS updates / service packs, security patches
- User accounts
  - Minimum password lenghts and complexity
  - Account limitations
- Network Access and security
  - Limit Network access
- Monitor and secure
  - Anti-virus, anti-malware

## Encryption
- Prevent access to applicationd ata files
  - File System encryption
  - Windows Encrypting FIle System EFS
- Full disk encryption FDE
  - Encrypt everything on the drive
  - Windows Bitlocker, macOS Filevault, etc.
- Encrypt all network communication
  - VPN
  - Application encryption

## The Endpoint
- The user´s access
  - App and data
- Stop the attackers
  - Inbound attacks
  - Outbound attacks
- Many different platforms
- Protection is multi-faceted
  - Defense in depth / Layered defense

## Endpoint detection and response EDR
- A different method of threat protection
  - Scale to meet the increasing number of threaths
- Detect a threat
  - Signatures are not the only detectio tool
  - Behavioral analysis, machine learning, process monitoring
  - Lightweight agent on the endpoint
- Investigate the threat
  - Root cause analysis
- Respond to the threat
  - Isolate the system, quarantine the threat, rollback to a previous config
  - API driven, no user or technician intervention required

## Host-based firewall
- Software-based firewall
  - Personakl firewall, runs on every endpoint
- Allow or disallow incoming or outgoing app traffic
  - Controls by app process
  - Views all data
- Identify and block unknown process
  - Stop malware before it can start
- Manage centrally

## Finding intrusions
- Host-based IPS HIPS
  - Recognize and block known attacks
  - Secure OS and app configs, validate incoming service requests
  - Often built into endpoint protection software
- HIPS Identification
  - Signatures, ehuristics, behavioral
  - Buffer overflows, registry updates, writing files to the Windows folder
  - Access to non-encrypted data
 
## Oepn ports and services
- Every open port is a possible entry point
  - Close everything expect required ports
- control access with a firewall
  - NGFW woould be ideal
- Unusued or unknown services
  - Installed with th eOS or from other applications
- Applications with broad port ranges
  - Open port 0 through 65,535
- Use NMAP or similar port scanner to verify
  - Ongoing monitoring is important
 
## Default password changes
- Every network device has a management interface
  - Critical systems, other devices
- Many apps also have management or maintenance interface
  - These can contian sensitive data
- Change default settings
- Add additional security
  - Require additional logon or MFA

## Removal of unnecessary software
- All software contains bugs
  - Some fo those bugs are security vulnerabilities
- Every application seems to have a completely different patching process
  - Can be challenging to manage ongoing updates
- Remove all unsued software
