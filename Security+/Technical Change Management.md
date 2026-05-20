- Put the cahnge management process into action
  - Execute the plan
- There are no suich things as a simple upgrade
  - Cna have amny moving parts
  - Separeate events may be required
- Change management is often concerned with what needs to change
  - The tech team is concerned with how to change it

## Allow list / Deny list
- Any application can be dangerous
  - Vulnerabilities, trojan horses, malware
- Security policy can control app execution
  - ALlow list, deny / block list
- Allow list
  - Nothing runs unless it is approved
  - Very restrictive
- Deny List
  - Nothing on the bad list can be executed
  - Anti-virus, anti malware

## Restricted Activities
- The scope of a change is important
  - Defines exactly which components are covered
- A change approval is not permission to make any change
  - The change control approval is very specific
- The scope may need to be expanded during the change window
  - It is impossible to prepare for all possible outcomes
- The change amangement process determines the next steps
  - tThere are processes in palce to make the changes sucessfull
 
## Downtime
- Serivces will evetnaully be unavailable
  - the change process can be disruptive
  - Usually scheduled during non-production hours
- If possible, prevent any downtime
  - Switch to secondary system, upgrade the primary, then switch back
- Minimize any downtime events
  - The process should be as automated as possible
  - Switch back to secondary if issues appear
  - Should be part of backout plan
- Send emails and calendar updates

## Restarts
- Common to require a restart
  - Implement the new config
  - Reboot the OS, power cycle the switch, bounce the service
  - Can the system recoverr from a power outage
- Servoces
  - Stop and restart the service or daemon
  - May take seconds or minutes
- Applications
  - Close the app completely
  - Launch a new app instance
 
## Legacy Apps
- Often no longer supported by the developer
  - You are now the support team
- Fear of the unknown
  - Face your fears and document the system
  - It may not be as bad as you think
- May be quickly
  - Create specific processes and proceduresº
- become the expert

## Dependencies
- To complete A, you must complete B
- A Service will not start without other active services
- An app requires a specific library version
- Modifying one component may require chaing or restarting other components
  - This can be challening to manage
- Dependencies may occur across systems
  - Upgrade the firewall code first
  - Then upgrade the firewall management software
 
## Documentation
- It can be challenging to keep up with changes
  - Documentation can become outdated quickly
  - Require with the change management process
- Updating Diagrams
  - Modifications to network configs
  - Address  updates
- Updating policies/ procdures
- Adding new systems may require new procedures

## Version Control
- Track changes to a file or config data over time
  - Easily revert to a previous setting
- Many opportunities to manage versions
  - Router configs
  - Windows OS patches
  - App registry entries
- Not always straightforward
  - Some devices and OS provide version control features
  - May require additioonal management software
