## Dealing with false information
- False positives
  - A vulnerability is identified that does not really exist
- This is different than a low-severity vulnerability
  - Its real, but it may not be your highest priority
- False negatives
  - A vulnerability exists, but it was not detected
- Update to the latest signatures
  - If you dont know about it, you cant see it
- Work with the vulnerability detection manufacturer
  - They may need to update their signatures in their environement

## Prirotizing Vulnerabilities
- Not every vulnerability shares the same priority
  - Some may not be significant
  - Others may be critical
- This may be difficult to determine
  - The research has probably already been done
- Refer to public disclousres and vulnerability databases
  - The industry is well versed
  -  ONline discussion groups, public disclosure mailing lists
- You can check CVSS National Vulnerability Database
  - Synced with the CVE list
  - Enhanced serach functionality
- Common Vulnerability Scoring System (CVSS)
  - Quantitative scoring of a vulnerability - 0 to 10
  - The scoring standards change over time
  - Different scoring for CVSS 2.0 vs CVSS 3.x
- Induastry collaboration
  - Enhanced feed sharing and automation

## CVE
- The Vulnerabilities can be cross-referenced online
  - Almost all scanners give you a place to go
- National Vulnerability Database
- Common Vulnerabilitie and Exposures (CVE)
- Microsoft Security Bulletins

## Vulnerability Classification
- The scanner looks for everything
- Application scans
- Web application scans
- Network scans
  - Misconfigured firewalls, open ports, vulnerable devices

## Exposure Factor
- Loss of value or business activity if the vulnerability is exploited
  - Usually a percentage
- A small DDoS may limit access to a service
- A buffer overflow may compeltely disable a service: 100% exposure factor
- A consideration when prioritizing

## Environmental variables
- What type of environment is associated with this vulnerability
  - Internal server, public cloud, test lab
- Priorization and patching frequency
  - A device in an isolated test lab
  - A database server in the public clouid
  - Which environment gets priority
- Every environment is different
  - Nubmer and trype of users
  - Revenue generation application
  - Potential for exploit

## Industry / Organizational Impact
- Some exploits have significant consequences
  - The Type of organization is an important consideration

## Risk Tolerance
- The amount of risk acceptable to an organization
  - Its impractical remove all risks
- The timing of security patches
  - Patching immediately does not allow for proper testing
- Testing takes time, meaning you are vulnerable during this time
- There is a middle ground
  - May change based on the severity 
