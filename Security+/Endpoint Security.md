## The endpont
- The user´s access
  - Applications and data
- Stop the attackers
  - Inbound attacks
  - Outbound attacks
- Many different platforms
  - Mobile, desktop
- Protection is multi-faceted
  - Defense in Depth
- Edge vs access control
  - Control at the edge
    - your Internet link
    - Managed primarily through firewall rules
    - Firewall rules rarely change
  - Access control
    - Control from wherever you are
      - Inside or Outside
    - Access can be based on any rules
      - by user, group, lçocation, application
    - Access can be easily revoked or changed

## Posture Assessment
- You cant trust everyones computer
  - BYOD Bring Your Own Device
  - Malware Infections / missing anti-malware
  - Unauthorized applications
- Before connecting to the network, perform a health check
  - Is it a trusted device?
  - Is it running anti-virus?
  - Are the corporate applications installed?
  - Is it a mobile device? Is the disk encrypted?
  - The type of device does not matter

## Health checks / posture assessment
- Persistent agents
  - Permanently installed onto a system
  - Periodic updates may be required
- Dissolvable agents
  - No installation is required
  - Runs during the posture assessment
  - Terminates when no longer required
- Agentless NAC
  - Integrated with active Directory
  - Checks are made during login and logoff
  - Cant be scheduled

## Failing your assessment
- What happens when a posture assessment fails
  - Too dangerous to allow access
- Quarantine network, notify administrators
  - Just enough network access to fix the issue
- Once resolved, try again

## Endpoint Detection and Response EDR
- A different method to threat protection
  - Scale to meet the increasing number of threats
- Detect a threat
  - Signatures arent the only detection tool
  - Behavioral analysis, machine learning, process monitoring
  - Lightweight agent on the endpoin
- Investigate the threat
  - Root cause analysis
- Respond to the threat
  - Isolate the system, quarantine the threat, rollback to a previous config
  - API driven, no user or technician intervention required

## Extended Detection and Response XDR
- An evolution of EDR
  - Improve missed detections, false psoitives, and long investigation times
- Attacks involve more than just the endpoint
- Add netowrk.based detection
- Correlate endpoint, network and cloud data

## User behaviour analytics
- XDR commonly includes user behavior analytics
  - Extend the scope of anomaly detection
- Watch users, hosts, network traffic, data repositories, etc.
  - Create a baseline or normal activity
  - Requires data anylsis over an extended period
- Watch for anything unusual
  - Use a set of rules, pattern matching, statistical analysis
- Real-time detection of unusual activity 
