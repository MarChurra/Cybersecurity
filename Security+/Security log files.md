- Detailed security-related information
  - Blocked and allowed traffic flows
  - Exploit attempts
  - BLocked URL categories
  - DNS sinkhole traffic
- Critical security information
  - Docmentation of every traffic flow
  - Summary of attack infor
  - Correlate with other logs

## Firewall logs
- Traffic flows through the firewall
  - Source/destination IP, port numbers, disposition
- NGFW
  - Logs the application used, URL filtering categories, anomalies and suspicious data
 
## Application Logs
- Specific to the application
  - Information varies widely
- Windows
  - Event viewer / App log
- Linux / macOS
  - var/log
- Parse the log details on the SIEM
  - Filter out uneeded info

## Endpoint logs
- Attackers often gain access to endpoints
  - Phones, laptops, tablets, desktops, servers,etc.
- There is a lot of data on the endpoint
  - Logon events, policy changes, system events, processes, account manageemnt, directory services,etc.
- Everything rolls up to the SIEM
  - Security Information and Event Manager
- Use with correlation of security events
  - Combine IPS event with endpoint status
 
## OS-specific security logs
- OS security events
  - Monitoring apps
  - Brute force, file changes
  - Authentication details
- Find problems before they happen
  - Brute force attacks
  - Disabled services
- May require filtering
  - Do not forward everything

## IPS/IDS logs
- These systems are usually integrated into a NGFW
- Logs contain information about predefined vulnerabilities
  - Known OS vulnerabilities, generic security events
- Common data points
  - Timestamp
  - Type or class of attack
  - Source and destination IP
  - Source and destination port

## Network logs
- Switches, routers, APs, VPN concentrators
  - ANd other infrastructure devices
- Network changes
  - ROuting updates
  - Authentication issues
  - Network security issues

## Metadata
- Data that describes other data sources
- Email
  - Header details, sending servers, destination address
- Mobile
  - Type of phone, GPS location
- Web
  - OS, browser type, IP address
- Files
  - Name, address, phone number, title

## Automated Reports
- Most SIEMs include a report generator
  - Automate common security reports
- May be easy or complex to create
  - The SIEM may have its own report generator
  - Third-party report generators may be able to access the database
- Requires human intervention
  - Someone has to read the reports
- These can be involved to create
  - Huge data storage and extensive processing time

## Dashboards
- Real-time status information
  - GEt summaries on a single screen
- Add or remove information
  - Most SIEMs adn reporting systems allow for customization
  - Shows the most important data
    - Not designed for long-term analysis

## Packet captures
  - Slve complex application issues
    - Get into the details
  - Gathers packets on the network
    - Or in WIFI
    - Sometimes built into the device
  - View detailed traffic information
    - Identify unknown traffic
    - Verify packet filtering and security controls
    - View in plain language
  - 
