- No system is secure with the default configurations
- Hardening guides are specific tot he software or platform
- Other general purpose guides are available online

## Mobile Devices
- Always connected mobile technologies
  - Phones, tablets, etc.
  - Hardenind checklists are available from manufacturers
- Updates are critical
- Segmentation can protect data
- Control with an MDM mobile Device Manager

## Workstations
- User desktop and laptops
  - Windows, macOS, Linux, etc.
- Constant monitoring updates
  - OS, applications, firmware, etc.
- Automate the monthly patches
- Connect to a policy management system
- Remove unnecessary software

## Network Infrastructure Devices
- Switches, routers, etc.
- Purpose-built devices
  - Embedded OS, limited OS access
- Configure authentication
  - Do not use defaults
- Check with the manufacturer
  - Security updates
  - Not usually updated frequently, however they are important

## Cloud Infrastructure
- Secure the cloud management workstations
- Least privilege
  - All services, network settings, app rights and permissions
- Configure Endpoint Detection and Response EDR
  - All devices accessing the cloud should be secure
  - Always have backups
    - C2C CLoud to Cloud

## Servers
- Many and varied
  - Windows, Linux, etc
- Updates
  - OS updates/service packs, security patches
- User accounts
  - Minimum password lengths and complexity
  - Accouint limitations
- Network access and security
  - Limit network access
- Monitor and secure
  - Anti-virus, anti-malware

## SCADA/ICS
- Supervisory Control and Data Acquisition System
  - Large-scale, multi-site Industrial Control System ICS
- PC manages equipments
  - Power generation, refining, manufacturing equipment
  - Facilities, industrial, energy, logistics
- Distributed control systems
  - Real-time information
  - System control
- Requires extensive segmentation
  - No access from the outside
 
## Embedded Systems
- Hardware and software designed for a specific function
  - Or to operate as part of a larger system
- Can be difficult to upgrade
- Correct vulnerabilities
  - Security patches remove potential threats
- Segment and firewall
  - Prevent access from unuauthorized users
 
## RTOS Real Time Operating System
- An OS with a deterministic processing schedule
  - No time to wait for other processes
  - Industrial equopment, automopbiles, military environments
- Isolate the system
  - Prevent access from other areas
- Run with the minimum services
  - Prevent potential for exploit
- Use secure communication
  - Protect with a host-based firewall
 
## IoT devices
- Heating and cooling, ligthing, home automation, wearable technology, etc.
- Weak defaults
- Deploy updates quickly
- Segmentation
  - Put these IoT devices in their own VLAN
