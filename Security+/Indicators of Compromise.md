## Indicators of compromise IOC
- An event that indicates an intrusion
  - Confident is high
  - He is calling from inside the house
- Indicators
  - Unusual amount of network activity
  - Change to file hash values
  - Irregular International Traffic
  - Change to DNS data
- Uncommon login patterns
- Spikes of read requests to certain files

## Account lockout
- Credentials are not working
  - It wasn´t you this time
- Exceeded login attempts
  - Account is automatically locked
- Account was administratively disabled
  - This would be a larger concern
- This may be a part of a larger plan
  - Attacker locks account
  - Calls support line to reset the pasword

## Concurrent session usage
- It´s challenging to be two places at one time
- Multiple account logins from multiple locations
  - Interactive access from a single user
  - You dont have a clone
- This can be difficult tot rack down
  - Multiple devices and desktops
  - Automated processes

## Blocked Content
- An attacker wants to stay as long as possible
  - Your system has been unlocked
  - Keep the doors and windows open
- Blocked content
  - Auto-update connections
  - Links to security patches
  - Third party anti-malware sites
  - Removal Tools

## Impossible Travel
- Authentication logs can be telling
  - Logon and logoff
- If you have a strange login from the same user, from far away, this should be suspicious. Especially when the user is at the office.
- This should be easy to identify
  - Log analysis and automation

## Resource Consumtpion
- Every attacker´s action has an equal and opposite reaction
  - Watch carefully for significant changes
- File transfers use bandwith
  - An unusual spike at 3AM
- Firewall logs show the outgoing transfer
  - IP addresses, timeframes
- Often the first real notification of an issue
  - The attacker may have been here for months

## Resource inaccessbility
- The server is down
  - Not responding
- Network disruption
  - A cover for the actual exploit
- Server outage
  - Result of an exploit gone wrong
- Encrypted Data
  - A potential ransomware attack begins
  - Brute force attack
  - Locks account access
 
## Out-of-cycle logging
- Out-of-cycle
  - Occurs at an unexpected time
- Operating system patch logs
  - Occurring outside of the normal patch day
  - Keep that exploited system safe from other attackers
- Firewall log activity
  - Timestamps of every traffic flow
  - Protocols and apps used

## Missing logs
- Log information is evidence
  - Attackers will try to cover their tracks by removing logs
- Information is everywhere
  - AUthentication logs
  - File access logs
  - Firewall logs
  - Proxy logs
  - Server logs
- The logs may be incriminating
  - Missing logs are suspicious
  - Logs should be monitored

## Published / documented
- The entire attack and data exfiltration may go unnoticed
- Company data may be published online
  - The attacker posts a portion or all data
  - This may be in conjuction with ransomware
- Raw data may be released without context
  - Researches will try to find the source
