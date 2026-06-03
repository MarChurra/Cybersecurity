- Reduce the impact of a security event, or a potential one

## Patching
- Incredibly important
  - System Stability, security fixes
- Monthly Updates
  - Incremental and important
- Third-party updates
  - App developers, device drivers
- Auto- update
- Emergency out-of-band updates

## Encryption
- Prevent access to application data files
  - File system encryption
- File Level Encryption
  - Windows EFS
- Full disk encryption
  - Encrypt everything on the drive
  - Bitlocker, FileVault
- Application data Encryption
  - Managed by the app
  - Stored data is protected

## Monitoring
- Aggregate information from devices
  - Built-in sensors, separate devices
  - Integrated into servers, switches, routers, firewalls, etc
- Sensors
  - IPS, firewall logs, authentcation logs, web server access logs, database transaction logs, email logs
- Collectors
  - Propriertary consoles, SIEM consoles, syslog servers
  - Many SIEMs include a correlation engine to compare diverse sensor data

## Least Privilege
- Rights and permissions should be set to the bare minimum
  - You only get what is n eeded for your job
- All users accounts must be limited
  - Appliocations should run with minimal privileges
- Dont allow users to run with administrative privileges
  - Limits the scope of malicious behaviour

## Configuration enforcement
- Perform a posture assessment
  - Each time a device connects
- Extensive Check
  - OS patch version
  - EDR Endpoint Detection and Response Veresion
  - Status of firewall and EDR
  - Certificate Status
- Systems out of compliance are quarantined
  - Private VLAN with limited access
  - Recheck after making corrections

## Decommissioning
- Should be a formal policy
  - Dont throw your data into the thrash
- Mostly associated with storage devices
- Many options for physical devices
  - Recycle the device for use in another system
  - Destroy the device
