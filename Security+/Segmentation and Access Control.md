## Segmenting the network
- Phyisical, logical, or virtual segmentation
  - Devices, VLANs, virtual networks
- Performance
  - High- bandwidth applications
- Security
  - Users should not talk directly to database servers
  - The only applications in the core are SQL and SSH
- Compliance
  - Mandate Segmentation (PCI Compliance)
 
## Access Control Lists ACLs
- Allow or disallow traffic
  - Grouping of categories
  - Source IP, Destination IP, port number, time of day, application, etc.
- Restrict access to network devices
  - Limit by IP address or other identifier
  - Prevent regular user / non-admin access
- Be careful, from locking yourself out

## Access Control Lists
- List the permissions
  - A user can read files
  - Another can access the network
  - Another can access a certain VLAN, with certain ports.
- Many OS use ACLs to provide access to files

## Application allow list / deny list
- Any applicaiton can be dangerous
  - Vulnerabilities, trojan horses, malware
- Security policy canc ontrol app execution
  - Allow list, deny/block list
- Allow list
  - Nothing runs unless it´s approved
  - Very restrictive
- Deny List
  - Nothing on the bad list can be executed
  - Anti-virus, anti-malware

## Examples
- Decisions are made in the OS
- Application Hash
  - Only allow applications with this unique identifier
- Certificate
  - Allow digitally signed apps from certain publishers
- Path
  - Only run application in these folders
- Network Zone
  - The apps can only run from this network zone
