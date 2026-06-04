## Attacks can happen anywhere
- Two categories for IT security
  - The on-premises data
  - The cloud-based data
- Cloud-based security is centralized and costs less
  - No dedicated hardware, no data center to secure
  - A third-party handles everything
- On premises puts the security burden on the client
  - Data center security and infrastructure costs

## On-premises security
- Customize your security posture
  - Full control when everything is in-house
- On-site IT tema can manage security better
  - The local team can ensure everything is secure
  - A local team can be expensive and difficult to staff
- Locl tema maintians uptime and availability
  - Systme checks can occur at any time
  - No phone call to support
- Security changes can take time
  - New equipment, configurations, and additional costs

## Centralized vs decentralized
- Most organiaztions are physically decentralized
  - Many locations, cloud providers, OS, etc.
- Difficult to manage and protect so many diverse systems
  - Centralize the security management
- A centralized approach
  - Correlated alert
  - Consolidated log file analysis
  - Comprehensive system status and maintenance/patching
- Not perfect
  - Single point of failure, potential performance issues

## Virtualization
- Run many different OS on the same hardware
- Each app instance has its own opearting system
  - Adds overhead and complexity
  - Virtualization is relatively expensive

## Application Containerization
- Container
  - Contains everything you need to run an application
  - Code and dependencies
  - A standardized unit of software
- An isolated process in a sandbox
  - Self-contained
  - Apps cant interact with each other
- Container image
  - A standard for portability
  - Lightweight, uses the host kernel
  - Secure separation between applications
 

## Virtualized vs. containerized
- Virtualized requires an Hypervisor
- In a Container Environment, there is an Docker, sitting above the the Host OS

## IoT Internet of Things
- Sensors
  - Heating and cooling, ligthing
- Smart devices
  - Home automation, video doorbells
- Wearable Technology
  - Watches, health monitors
- Facility automation
  - Temperature, air quality, ligthing
- Weak defaults
  - IOT manufacturers are notsecurity professionals

## SCADA / ICS
- Supervisory Control and Data Acquisition System
- Industrial Control System ICS
- Large scale, multi site ICS
- PC manages equipment
  - Power generation, refining, manufacturing equipment
  - Facilities, industrial, eergy, logistics
- Distributed control system
  - Real-time information
  - System control
- Requires extesnive segmentation
  - No access from the outside
 
## RTOS Real-Time Operating System
- An operating system with a deterministic processing schedule
  - No time to wait for other processes
  - Industrial equipment, automobiles
  - Military environments
- Extremely sensitive to security issues
  - Non-trivial systems
  - Need to always be available
  - Difficult to know what type of security is in place

## Embedded Systems
- Hardware and software designed for a specific function
  - Or to operate as part of a larger system
- Is built with only a singlet ask in mind
  - Can be optimized for size and/or cost
- Common examples:
  - Traffic light controllers
  - Digital watches
  - Medical imaging systems

## High Availability
- Redundancy does not always mean always available
  - May need to be powered on manually
- HA (High availability)
  - Always on, always available
- May include many different components working together
  - Active/Active can provide scalability advantages
- Higher availability almost always means higher costs
  - There is always another contigency you could add
  - Upgraded power, high-quaity server components, etc.
