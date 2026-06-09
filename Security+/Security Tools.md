## Security Content Automation Protocol (SCAP)
- Many different security tools on the market
  - NGFWs, IPS, vulnerability scanners, etc.
  - They all have their own of evaluating a threath
- Managed by the NIST National Institute of Standards and Technology
- Allows tools to identify and act on the same criteria
  - Validate the security configuration
  - Confirm patch installs
  - Scan for a security breach
- Using SCAP
  - SCAP content can be shared between tools
    - Focused on configuration compliance
    - Easily detect applications with known vulnerabilities
  - Especially useful in large environments
  - Many different OS systems and applications
  - This specification standard enables automation
  - Automation types
    - Ongoing monitoring
    - Notification and alerting
    - Remediation of noncompliant systems
  
  ## Benchmarks
    - Apply security best-practices to everything
      - OS, cloud providers, mobile devices, etc.
      - The bare minimum for security settings
    - Mobile Devices
      - Disable screenshots, screen recordings, prevent voice calls when locked, force encyption, backups, so on
    - There are guidelines for these benchmarks

## Agents/agentless
- Check to see if the device is in compliance
  - Install a software agent onto the device
  - Run an on-demand agentless check
- Agents can usually provide more detail
  - Always monitoring for real-time notifications
  - Must be maintained and updated
- agentless runs without a formal install
  - Performs the check, then dissapears
  - Does not require ongoing updates to an agent
  - Will not inform or alert if not running
 
## SIEM
- Security Information and Event Management
  - Logging of security events and information
- Log collection of security alerts
  - Real-time information
- Log aggregation and long-term storage
  - Usually includes advanced reporting features
- Data correlation
  - Link diverse data types
- Forensic analysis
  - Gather details after an event
 
## Anti-virus and anti-malware
- Anti-virus is the popular term
  - Referes to a type of a malware
  - Trokans,worms, macro viruses
- Malware refers to the broad malicious sfotware category
  - Anti-malware stops spyware, ransomware, fileless malware
- The terms are effectively the same these days
  - The names are more of a marketing tool
  - Anti-virus software is also anti-malware software now
 
## Data Loss Prevention DLP
- Where is your data?
  - Social Security numbers, credit card numbers, medical records
- Stops the data before the attacker gets it
  - Data leakage
- So many sources, so many destinations
  - Often requires multiple solutions
  - Endpoint clients
  - Cloud-based systems
 
## SNMP
  - Simple Network Management Protocol
    - A database of data MIB - Management Information Base
    - The database contains OIDs - Object Identifiers
    - Poll devices over udp/161
  - Request statistics from a device
    - Server, firewall, workstation, switch, router, etc.
  - Poll devices at fixed intervals
    - Create historical performance graphs

## SNMP traps
- Most SNMP operations expect a poll
  - Devices thenr espond to the SNMP request
  - This requires constant polling
- SNMP traps can be configured on the monitored device
  - Communicates over udp/162
- Set a treshold for alerts
  - If the number of CRC errors increase by 4, send a trap
  - Monitoring station can react immediately

## NetFlow
- Gather traffic statistics from all traffic flows
  - Shared communication between devices
- netFlow
  - Standard collection method
  - Many products and options
- Proble and collector
  - Probe watches network communication
  - Summary records are sent to the collector
- Usually a separate reporting app

## Vulnerability Scanners
- Usually minimally invasive
- Port scan
- Identify systems
  - And security devices
- Test from the outside and inside
- Gather as much information as possible
