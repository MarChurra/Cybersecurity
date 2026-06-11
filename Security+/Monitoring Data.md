## FIM File Integrity monitoring
- Some files change all the time, while some should never change
- Monitor important OS and application files
  - Identify when changes occur
- Windows - FC (System File Check) - Inbuilt Windows Utility for FIM
- Linux - Tripwire
- Many host-based IPS options

## Data Loss Prevention DLP
- Where is your data?
  - Social Security numbers, credit card numbers, medical records
- Stop the data before the attacker gets it
  - Data "leakage"
- So many sources, so many destinations
  - Often requires multiple solutions in different places

## Data Loss Prevention DLP systems
- On your computer
  - Data in use
  - Endpoint DLP
- On your network
  - Data in  motion
  - Can be standalone or within an NGFW
- On your server
  - Data at rest
  - Software running within an server usually

## USB blocking
- DLP on a workstation
  - Allow or deny certain tasks
- All devices had to be updated
  - Local DLP agent handled USB blocing

## Cloud-based DLP
- Located between users and the Internet
  - Watch every byte of network traffic
  - No hardware, no software
- Block custom defined data strings
  - Unique data for your organization
- Manage access to URLs
- Blocks viruses and malware

## DLP and email
- Email continues to be the ost critical risk vector
  - Inbound threats, outbound data loss
- Check every email inbound and outbound
  - Internal system or cloud-based
- Block keywords, identify impostors, quarantine email messages
- Outbound
  - Fake wire transfers, W-2 transmissions, employee information
