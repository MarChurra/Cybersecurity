## IPS
- Intrusion PRevention Syste
  - Watch network traffic
- Intrusions
  - Exploits against OS, applications, etc.
  - Buffer overflows, cros-site scriptings, others
- Detection vs Prevention
  - IDS alerts, while an IPS blocks
  - Prevention - Stop it before it gets into the network

## Failure Modes
- We hope for 100% uptime
  - Eventually, something will break
- Fail-open
  - When a sytem fails, data continues to flow
- fail-closed
  - When a system fails, data does not flow

## Device Connections
- Active Monitoring
  - System is connected inline
  - Data can be blocked in real-time as it passes by
  - Intrusion prevention is commonly active
- Passive monitoring
  - A copy of the nebtwork traffic is examined using a tap or port monitor, SPAN (Switch Port Analyzer)
  - Data cannot be blocked in real-time
  - Intrusion detection is commonly passive
