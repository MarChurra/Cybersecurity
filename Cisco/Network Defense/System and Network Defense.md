## Physical Security

### Fencing and Physical Barriers 
- Physical Barriers:
  - Perimeter fence system
  - Security gate system
  - Bollards
  - vehicle entry barriers
  - Guard shelters
  - Fencing
 
- Fencing:
  - A barrier that encloses secure areas and designates boundaries.
 
- High-security areas often require a ‘top guard’ such as barbed wire or concertina wire. Top guards act as an additional deterrent and can delay the intruder by causing severe injury. However, attackers can still use a blanket or mattress to alleviate this threat.
- Local regulations may restrict the type of fencing system an organization can use and it’s important to remember that fences require regular maintenance. Animals may burrow under the fence or the earth may wash out, leaving the fence unstable — this would lead to easy access for an intruder. Fencing systems should be inspected regularly.
- Moreover, vehicles should never be parked near a security fence, as this could assist the intruder in climbing over or causing damage to the fence.

### Biometrics
- Biometrics are the physiological or behavioral characteristics of an individual, and there are security practices based on identifying and granting access using biometrics.
- These can include measurement of the face, fingerprint, hand geometry, iris, retina, signature and voice.
- Biometric technologies can be the foundation of highly secure identification and personal verification solutions. The popularity and use of biometric systems have increased because of the rise in security breaches and transaction fraud.
- It is necessary to have into account as factors to consider which one to implement:
  - Accuracy
  - Speed or throughput rate
  - Acceptability to users
  - Uniqueness of the biometric organ and action
  - Ressistance to counterfeiting
  - Reliability
  - Data storage requirements
  - Enrollment time
  - Intrusiveness of the scan
- Accuracy is one of the most important, which is expressed in error types and rates.
- The first error rate is Type I errors or false rejections. These reject a person that registers and is an authorized user.
- However, in many biometric applications, particularly retail or banking, false rejections can have a negative impact on business due to a transaction or sale being lost.
- False acceptance is a Type II error. These allow entry to people who should not have entry meaning a cybercriminal can potentially gain access. These are considered the most important error for a biometric access control system.
- The acceptance rate is also an important concept here. Stated as a percentage, it is the rate at which a system accepts unenrolled individuals or imposters as authentic users. The rate of Type II errors per ttoal instances of granting permission.

### Badges and Access Logs
- An access badge allows an individual to gain access to an area with automated entry points.

### Surveillance
- Many physical access controls, including deterrent and tection systems, ultimately rely on people to intervene and stop the actual attack or intrusion.
- This can also include Video and Electronic Surveillance. These should be placed at all entrances, exits, loading bays, stairwells and refuse collection areas, in highly secure environments.
- Guards and Escorts
- RFID and Wireless Surveillance

## Application Security
- To maintain security at all stages of app development, a robust process needs to be followed:
  - Developing and Testing
  - Staging and production
  - Provisioning and deprovisioning
 
### Security Coding Techniques
- When coding applications, developers use several techniques to validate that all security requirements have been met.
  - Normalization: Organizes data in a DB and help maintain data integrity. Normalizaion converts an input string to its simplest known form to ensure that all strings have unique binary representations and that any malicious input is identified.
  - Stored procedure: A stored procdure is a group of precompiled SQL statements stored in a DB that executes a task. If you use a stored procedure to accept input parameters from clients using different input data, you will reduce network traffic and get faster results.
  - Obfuscation and camouflage: A developer can use obfuscation and camouflage to prevent software from being reverse engineered. Obfuscation hides original data with random characters or data. Camouflage replaces sensitive data with realistic ficitonal data.
  - Code reuse: Using existing software to build new software, saving time and development costs. Care must be taken, to avoid introduction of vulnerabilities.
  - SDKs: Third-party libraries and SDKs provide a repository of useful code to make app development faster and cheaper. The downside is that any vulnerabilities in SDKs or 3rd party libraries can potentially affect many applications.
 
### Input Validation
- Controlling the data input process is key to maintaining database integrity.
-  Many attacks run against a database and insert malformed data.
-  Such attacks can confuse, crash or make the application divulge too much information to the attacker.
-  Customers fill out a web application form to subscribe to a newsletter. A database application automatically generates and sends email confirmations back to the customers. When customers receive the email with a URL link to confirm their subscription, attackers have modified the URL link.
-  These modifications can change the username, email address or subscription status of the customers when they click to confirm their subscription. This way, when the email is returned to the host server, it receives bogus information, which it might not be aware of if it does not check each email address against subscription information.
-  Hackers can automate this attack to flood the web application with thousands of invalid subscribers to the newsletter database.

### Validation Rules
- A validation rule checks that data falls within the parameters defined by the database designer. A validation rule helps to ensure the completeness, accuracy and consistency of data.
- The criteria used in a validation rule include the following:
  - Size: Checks the numbers of characters in a data item
  - Format: Checks that the data conforms to a specific format
  - Consistency: Checks for the consistency of odes in related data items.
  - Range: Checks that data lies within a minimum and maximum value
  - Check digit: provides for an extra caltucation to generate a check digit for error detection.
 
### Integrity Checks
- Compromised data can threaten the security of your devices and systems.
- An inteigty check can measure the consistency of data in a file, to ensure that it has not been corrupted.
- The inteigrty check performs a hash function, to take a snapshot of data and then uses this snapshot to ensure data has remained unchanged.
- A cheksum is an example of a hash function.
- Use of version control, meaning that two users cannot update the same object, at the exact same time. While keeping a log of past versions of the file.
- The utilization of Backups (need to be verified regularly) and Authorization.

### Other Application Security Practices
- Code Signing: Helps prove that a piece of software is authentic. Executables designed to install and run on a device are digitally signed to validate the author´s identity and provide assurance that the software code has not changed since it was signed.
- Secure Cookies: Protect information stored in cookies from hackers. This means using HTTPS tow ork with cookies.

## Network Hardening: Services and Protocols

### Network and Routing Services
- Cybercriminals use vulnerable network services to attack a device or to use it as part of an attack. To check for insecure network services, use a port scanner to detect open ports on a device. A port scanner sends a message to each port and waits for a response, which indicates how the port is used and whether it is open.
- But beware, cybercriminals also use port scanners for this same reason! Securing network services ensures that only necessary ports are exposed and available.
- Here are some precautions to ensure:
  
  - DHCP:
    - Secure the DHCP server physically, apply software patches.
    - Locate the DHCP server behind a firewall
    - Minitor DHCP activity by reviewing DHCP logs.
    - Maintain a strong antirivurs solution
    - Uninstall any unusued services and applications
    - Close unsued ports
      
- DNS:
  - Attackers can target DNS servers to deny access to network recoures or redirect traffic to rogue websites.
  - Use secure service and authentication between DNS servers to protect them from these attacks.
  - DNS Security Extensions uses digital signatures to strengthen authentication and protect against threats to the DNS.
  - Keep the DNS software up to date.
  - Prevent version string from revealing information.
  - Separate internal and external DNS servers.
  - Restrict allowed transactions by client IP address
  - Use transaction signatures to authenticate transactions.
  - Disable or restrict zone transfers and dynamic updates.
  - Enable logging and analyze logs
  - Use Domain Name SYstem Security Extensions
  - Sign Zones
 
- ICMP:
  - Network device uses ICMP to send error messages, that a requested service is not available or the host could not reach the router.
  - The ping command is a network utility that uses ICMP to test the reachability of a host on a network. Ping sends ICMP messages to the host and waits for a reply. Cybercriminals can alter the use of ICMP to run reconnaissance, denial of service (DoS) and covert channel attacks. Many networks filter ICMP requests to prevent such attacks.
- Routing Information Protocol RIP:
  - RIP is a routing protocol that limits the number of hops from source to destination that are allowed in a network path. The maximum number of hops allowed for RIP is fifteen. RIP is used to exchange routing information about which networks each router can reach and how far away those networks are.
  -  RIP calculates the best route based on hop count, but cybercriminals can also target routers and the RIP protocol. Such attacks on routing services can affect performance and availability, some attacks can even result in traffic redirection. Use secure services with authentication and implement system patching and updates to protect routing services.
- NTP:
  - Having the correct time within networks is important. Correct timestamps accurately track network events such as security violations. Additionally, clock synchronization is critical for the correct interpretation of events within syslog data files as well as for digital certificates.
  - Network Time Protocol (NTP) is a protocol that synchronizes network computer system clocks. NTP allows network devices to synchronize their time settings with an NTP server. Cybercriminals attack timeservers to disrupt secure communication that depends on digital certificates and to hide attack information. Use NTP Authentication to verify that the server is trusted.
 
### Telnet, SSH, and SCP
- Secure Shell (SSH) is a protocol that provides a secure (encrypted) remote connection to a device. Telnet is an older protocol that uses unsecure plaintext when authenticating a device (user name and password) and transmitting data. SSH should be used rather than Telnet to manage connections, as it provides strong encryption. SSH uses TCP port 22. Telnet uses TCP port 23.
- Secure copy (SCP) securely transfers files between two remote systems. SCP uses SSH for data transfer and authentication, ensuring the authenticity and confidentiality of the data in transit.

## Network Hardening: Segmentation

### Virtual Local Area Networks
- A VLAN segments the network and creates a secure area for the sensitive data.
- VLANs provide a way to group devices within a LAN and on individual switches.
- VLANs are based on logical connections, while LANs are based on physical connections.
- Other ports can be used to physically interconnect switches and allow multiple VLAN traffic between switches. These ports are called trunks.
- The network is segmented, based on factors such as function, project team or application. Devices within a VLAN act as if they are in their own independent network, even though they share a common infrastructure with other VLANs on the same LAN. A VLAN can separate groups of devices that host sensitive data from the rest of the network, decreasing the chances of confidential information breaches.
- VLANs provide a way to limit broadcast traffic in a switched network.

### Demilitarized Zone
- A DMZ is a small network between a trusted private network and the internet.
- Web servers and mail servers are usually placed within the DMZ to allow users to access an untrusted network, such as the Internet, without compromising the internal network.
- Most networks have two to four zones of risk , the trusted private LAN, the DMZ, the Internet and an extranet. Each zone has its own risk and trust meter.
- Firewalls manage east-west traffic (traffic that goes between servers within the organizations data center) and north-south traffic (data moving into and out of the organization network).
- To protect its network, an organization can implement a Zero Trust Model. Automatically trusting users and endpoints within the organization can put any network at risk, as trusted users can move throughout the network to access data. Zero trust constantly monitors all users on the network, regardless of status and role.

## Hardening Wireless and Mobile Devices
- WPA servers as an upgrade to the defunct WEP standard. WPA-PSK (Pre-Shared Key) is the most common WPA configuration. The keys used by WPA are 256-bit, a significant increase over the 64-bit and 128-bit keys used in the WEP system.
- First, WPA provided message integrity checks (MIC), which could detect if an attacker had captured and altered data passed between the wireless access point and a wireless client.
- Another key security enhancement was Temporal Key Integrity Protocol (TKIP). The TKIP standard helped to better handle, protect and change encryption keys. Advanced Encryption Standard (AES) superseded TKIP, for even better key management and encryption protection.

### Authentication
- The best way to secure a wireless network is to use authentication and encryption. The original wireless standard, 801.11, introduced two types of authentication:
  - Open System Authentication: Any wireless device can connect to the wireless network.
  - Shared Key authentication: Provides mechanism to authenticate and encrypt data between a wireless client and AP or wireless router.

### Authentication Protocols
- The EAP Extensible Authentication Protocol is an authentication framework used in wireless networks.
  1. The user requests to connect to the wireless network through an access point.
  2. The access point requests identification data (username) from the user, which is then sent to an authentication server.
  3. The authentication server requests proof that the ID is valid.
  4. The access point requests proof that the ID is valid from the user, in the form of a password.
  5. The user supplies the access point with their password. The access point sends this back to the authentication server.
  6. The server confirms the username and password are correct, and passes this information on to the access point and user.
  7. The user connects to the wireless network.
 
- These are four protocols used with EAP to provide authentication for wireless networks:
  - EAP-TLS: Requires Client and Server certificates. Difficult to deploy and has high security
  - PEAP: Only requires server certificate. Moderate to deploy and medium security.
  - EAP-TTLS: Same as above
  - EAP-FAST: Does not require certificates. Easy to deploy, medium security.
 
### Mutual Authentication
- Your wireless network and its sensitive data are susceptible to unauthorized access by hackers using a wireless connection. But what can you do to prevent an attack?
- An access point is any hardware device that enables other wireless devices to connect to a wired network. Any device that has a wireless transmitter and hardwired interface to a network can potentially act as a rogue or unauthorized access point.
- The rogue access point will often imitate an authorized access point, allowing users to connect to the wireless network but potentially stealing their data or conducting other nefarious activity in the process.
- When you connect to a rogue access point, the imposter who set it up can request and copy data from your device. This type of man-in-the-middle attack is very difficult to detect and can result in stolen login details and data.
- Mutual authentication is two-way authentication that can prevent rogue access points. It is a process in which both entities in a communications link authenticate each other before they connect. This enables clients to detect rogue access points and prevent such MitM attacks.

### Communiucation Methods
- Wi-fi and Bluetooth
- NFC: These chips sue electromagnectic fields to enable contactless payments.
- Infrared: A short-range communication using an IR Rreceiver.
- USB communication

### Mobile Device Management
- A mobile device issued by an organization can contain both personal and organizational data. It can be corporate-owned or corporate-owned personally enabled COPE.
- An organization can also implement BYOD options.
- Security and data protection policies need to be applied when there is sensitive corporate information on a user’s device.
- Storage segmentation and containerization allow you to separate personal and work content on a device. It provides an authenticated, encrypted area that sepparates sensitive company information from the user-s personal data. It also allows to isolate apps, control app functions, delete contaioner information, remotely wipe the device.
- Content Management: An organization needs to consider the security risks involved in using applications that share data — for example, Dropbox, Box, Google Drive and iCloud. An identity-management security system can be used to control what data a user can access.
- Application Management: Whitelisting allows you to digitally sign applications so that you can authorize which applications users can install. This helps to ensure that installed applications come from a trusted source.

### Mobile Device Protections
- Jailbreaking removes the restriction that only Apple-authorized apps may run on the device. Rooting bypasses Android’s security architecture to allow complete, administrative access to the device. Both pose a risk to the organization.
- Solutions are available that can detect a jailbroken or rooted device. A device is then marked as noncompliant and removed from the network or denied access to organizational apps.
- Third-party app stores can also pose a risk for organizations because the apps they provide access to have not been evaluated properly. Sideloading occurs when the user goes around the approved app settings to install unapproved apps. This is less invasive than jailbreaking or rooting, but it is still a risk.
- Safeguards against mobile device threats include Screen locks, Biometric authentication, Context-aware authentication (uses machine learning to determine access based on a users normal behavior), remote wiping and Full Device encryption.

### GPS Tracking
- Global Positioning System (GPS) uses satellites and computers to determine the location of a device. GPS technology is a standard feature on smartphones and provides real-time position tracking that can typically pinpoint a location to within approximately 5 meters.
- Some apps use geofencing or geolocation, which use radio-frequency identification (RFID) to determine a geographic area instead.

## Cybersecurity Resilience

### High Availability
- The term ‘high availability’ describes systems designed to avoid downtime as much as possible. The continuous availability of information systems is imperative, not only to organizations but to modern life, as we are all using and relying on computer and information systems more than ever before.
- High availability systems typically are based on three design principles.
  - Eliminating Single points of Failure: The first principle that defines high availability systems starts with identifying all system devices and components whose failure would result in system-wide failure. Methods to eliminate single points of failure include replacing or removing hot stand-by devices, redundant components and multiple connections or pathways.
  - Providing for Reliable Crossover: Redundant power supplies, backup power systems and backup communications systems all provide for reliable crossover — the second design principle.
  - Detecting Failures as they occur: The third principle is active device and system monitoring to detect many types of events including system and device failures. Monitoring systems may even trigger the backup system in the case of failure.
 
### The Five Nines
- One of the most popular high availability goals is often called ‘five nines.’ It gets its name from its aim to achieve an availability rate of 99.999%, which is five nines in a row. In practice, this means that downtime is less than 5.26 minutes per year.
- This is accomplished by:
  - Standardized Systems: Systems standardization provides for systems that use the same components. As a result, parts inventories are easier to maintain and it is possible and easy to swap components, even during an emergency.
  - Clustering: Multiple devices grouped together provide a service that, to users, appears to be a single entity. If one device in a cluster fails, the other devices remain available and can step in.
  - Shared Component Systems: Systems are built so that a complete system can stand in for one that failed.
 
### Single Points of Failure
- Single points of failure are weak links in the chain that can cause disruption of the organization's operations. A single point of failure is any part of the operation of the organization whose failure means complete failure of the entire system — in other words, if it fails, the entire system fails.
- A single point of failure can be a specific piece of hardware, a process, a specific piece of data, or even an essential utility. Generally, the solution to a single point of failure is to modify the critical operation so that it does not rely on any single element. The organization can also build redundant components into the operation to take over the process should one of these points fail.

### N+1 Redundancy
- N+1 Redundancy helps ensure system availability in the event of a component failure. It means that componetns N need to have at least one backup component +1,
- A good way to think about this is that a car has four tires (N) and a spare tire (+1) in the trunk in case of a flat.
- Although a system using N+1 architecture contains redundant equipment, it is not a fully redundant system.

### RAID
- Raid Level 0: Min of 2 Drives. Data striping without redundancy. has highest performance, but no data protection.
- Raid Level 1: Min of 2 Drive, uses disk mirroring. Highest performance, high data protection because data is duplicated. Has an higher cost of implementation
- Raid Level 2: Error-Correcting Coding: No longer used, same performance can be acheved at a lower cost with Raid 3.
- Raid Level 3: Min of 3 Drives. Byte level data striping with dedicated parity. It is for large, sequential data requests. Does not support multiple simultaneous read and write requests.
- Raid Level 4: Block-level data striping with dedicated parity . Supports multiple read requests. If a disk fails, the deicated parity disk is used to create a replacement disk. Write request are bottlecked due to the dedicated parity drive.
- Raid level 5: Combination of data striping and parity. Suppports multiple simultaneouus reads and writes, but sllower performance.

- Raid takes data that is normally stored on a single disk and spreads it out among several drives. Except for RAID 0, if any single disk is lost, the user can recover data from the other disks where the data also resides.
- RAID can also increase the speed of data recovery as multiple drives will be faster retrieving requested data than one disk doing the same.
- A RAID solution can be either hardware-based or software-based. A hardware-based solution requires a specialized hardware controller on the system that contains the RAID drives, while software RAID is managed by utility software in the OS.
- The following terms describe the various ways RAID can store data in the array of disks.
- Mirroring — Stores data, then duplicates and stores the same on a second drive.
- Striping — Writes data across multiple drives so that consecutive segments are stored on different drives.
- Parity — More precisely, striping with parity. After striping, checksums are generated to check that no errors exist in the striped data. These checksums are stored on a third drive.

### Spanning Tree
- Redundancy increases the availability of the infrastructure by protecting the network from a single point of failure, such as a failed network cable or a failed switch.
- But when designers build physical redundancy into a network, loops and duplicate frames occur. Loops and duplicate frames have severe consequences for a switched network
- The Spanning Tree Protocol (STP) addresses these issues. Its basic function is to prevent loops on a network when switches interconnect via multiple paths. STP ensures that redundant physical links are loop-free and only one logical path runs between all destinations on the network. To do this, STP intentionally blocks redundant paths that could cause a loop.
- Blocking the redundant paths is critical to preventing loops on the network. The physical paths still exist to provide redundancy, but STP disables these paths to prevent the loops from occurring. If a network cable or switch fails, STP recalculates the paths and unblocks the necessary ports to allow the redundant path to become active.

### Router Redundancy
- The default gateway is typically the router that provides devices access to the rest of the network and/or to the internet. If there is only one router serving as the default gateway, it is a single point of failure. To avoid this, an organization can choose to install an additional standby router.
- A redundancy protocol determines which router should take the active role in forwarding traffic; the forwarding router or the standby router? Each is configured with a physical IP address and a virtual router IP address. End devices use the virtual IP address as the default gateway, which is 192.0.2.100.
- The forwarding router and the standby router use their physical IP addresses to send periodic messages. The purpose of these messages is to make sure both are still online and available.
- If the standby router stops receiving these periodic messages from the forwarding router, it realizes it is the only router available and assumes the forwarding role for itself. Meanwhile, because the PCs on the network still communicate with the virtual router at 192.0.2.100, they stay online despite everything that has happened, since the virtual router now forwards to what was previously the standby router.
- The ability of a network to dynamically recover from the failure of a device acting as a default gateway is known as first-hop redundancy,

### Location REdundancy
- Synchronous Replication: Syncronizes both locations in real time. Requires high bandiwdth. Locations must be close together.
- Asynchronous Replication: Not synced in real time, but close ot it. Requires less bandiwdth. Sites can be further apert.
- Point in Time Replication: Updates the backup data location priodically, at certain points in time.
- More bandiwdth conservative because it does not require a constant connections.

### Resilient Design
- Resiliency is the name given to the methods and configurations used to make a system or network tolerant of failure.
- An example of resiliency is a network having redundant links between switches running STP. Although STP does provide an alternate path through the network if a link fails, the switchover may not be immediate if the configuration is not optimal, so these redundant links together with STP provide more resiliency.
- Routing protocols also provide resiliency, but fine-tuning can improve the switchover so that network users do not notice. Administrators should investigate non-default settings in a test network to see if they can improve network recovery times, thus leading to minimal disruption.
- As seen in the above examples, resilient design is about more than just adding redundancy. It is critical to understand the business needs of the organization and then incorporate redundancy to create a resilient network.
- Application REsilience: Application resilience is an application’s ability to react to component problems while still functioning. Application errors or infrastructure failures can cause downtime, but an administrator will eventually need to shut down applications for patching, version upgrades, or to deploy new features.
- There are three availability solutions to address app resilience. AS the availability factor of each solution increases, so does the complexity and cost.
- Fault tolerant hardware: A system designed by building multiples of all critical components into the same computer.
- Cluster Architecture: A group of servers acting like a single system.
- Backup and restore: Copying files for the purpose of being able to restore them if data loss occurs.

### System and Data Backups
- An organization can lose data if cybercriminals steal it, if equipment fails, or if a disaster or other error occurs, so it’s important to back up data regularly.
- A data backup stores a copy of the information from a computer to backup media. When such media is removable, the operator then stores this backup media in a safe place.
- Backing up data is one of the most effective ways of protecting against data loss. If the hardware fails, the user can restore the data from the backup once the system is functional again, or even when moving to a new system.
- Frequency: Recommended to make full backups monthly or weekly and then do frequent partial backups. However, having many partial backups increases the amount of time needed to restore the data.
- Storage: For extra security, transport backups to an approved off-site storage.
- Security: Protect backups with passwords
- validation: Validade backups to ensure integrity.

### Designing High Availability Systems
- High availability incorporates three major principles to achieve the goal of uninterrupted access to data and services.
  - Elimination or Reduction of Single Points of Failure
  - Fault Tolerance
  - System REsiliency
 
### Power
- A critical issue in protecting information systems is electrical power systems and power considerations. A continuous supply of electrical power is essential for today’s massive server and data storage facilities.
- Here are some general rules in building effective electrical supply systems:
  - Data centers should be on a different power supply from the rest of the building.
  - Use redundant power sources — two or more feeds coming from two or more electrical substations.
  - Implement power conditioning.
  - Backup power systems
  - UPS available
  - Power Excess: Spike a momoentary high voltage and Surge a prolonged high voltage
  - Power Loss, caused by a Fault or Blackout
  - Power Degradation: Sag/dip a momentary low voltage. Brownout, a prolonged low voltage. Inrush current , a initial surge of power.

### Heating, Ventilation and Air Conditioning
- HVAC systems are critical to the safety of people and information systems in an organization's facilities. When designing modern IT facilities, these systems play a very important role in the overall stability and security.

## Embedded and Specialized Systems

### Threats to Key Industry Sectors
- Over the last decade, cyber attacks like Stuxnet proved that malware attacks could successfully destroy or interrupt critical infrastructures. The Stuxnet worm targeted Supervisory Control And Data Acquisition (SCADA) systems used to control and monitor industrial processes. SCADA and other Industrial Control Systems (ICSs) are used in manufacturing, production, energy and communications systems.

### The Emergence of IoT
- The Internet of Things (IoT) is the collection of technologies that enable various devices to connect to the Internet. The technological evolution associated with IoT is changing commercial and consumer environments.
- IoT technologies enable people to connect billions of devices, such as cars, industrial machines, robots, appliances, locks, motors and entertainment devices, to name just a few. This technology affects the amount of data that needs to be protected. As users need to access these devices remotely, they are placed online, which increases the number of potential entry points to that local network in general.
- Moreover, with the emergence of IoT, there is much more data to be managed and secured. All these devices, plus the expanded storage capacity and storage services offered through the cloud and virtualization, have led to the exponential growth of data. This data expansion created a new area of interest in technology and business called ‘Big Data.’
- IoT devices greatly expand the cyber attack surface. In the IoT, thousands of new devices require access to networks in order to submit data and be managed and operated. Internet-connected smart devices have been infected with malware and used to launch some of the largest DDoS attacks in history. Therefore, IoT device security is extremely important. First, all IoT devices should be evaluated to ensure that they are able to update their firmware with security patches, preferably over wireless networks. In addition, default administrator credentials on these devices should always be changed from the default settings because these settings are publicly known.

### Embedded Systems
- Embedded systems capture, store and access data. They pose unique security challenges due to their widespread adoption by both the corporate and the consumer world. They are used in smart TVs, HVAC control systems, medical devices and even automobiles.
- One technique to protect these devices from side-channel attacks, is to use System on Chip SOC technology.
- Thios is a SFF hardware module, such as the raspberry pi or Arduino.
- These are single-board computers that can be implmeneted using a Field-Programmable Gate Array, an integrad circuit that can be programmed or modified in the field. Meaning the user can make changes after deploying the device.
- SoC integrates a microcontroller, an application or microprocessor and peripherals such as a GPU, a WI-fi module or a coprocessor. These can run many different OS.
- These however, have poor authentication and are not upgraded or patched, requiring a degree of trust.
- These devices can use a Real Time Operating System RTOS, a small OS that allows for rapid switching of tasks, than ofcus on timing, rather than throughput. They run with precise timing and high reliability.
- However, they have some vulnerabilities, such as Code Injection, DoS attacks and priority inversion.

### VoIP Equipment
- Uses internet to make and receive phone calls.
- It requires an internet connection and a phone for VoIP.
- A traiditional phone with an adapter (the adapter acts as a hardware interface, between a traditional anlog phone and a digital VoIP line)
- A VoIP enabled phone
- VoIP software installed on a computer.
- VoIP security is only as reliable as the underlying network security.
- Cybercriminals target these systems to gain access to free phone services, to eavesdrop on phone calls, or to affect performance and availability
- To protect VoIP, you can:
  - Encrypt voice message packets to protect against eavesdropping.
  - Use SSH to protect gateways and switches.
  - Change the default passwords
  - Use an intrusion detection system to detect attacks such as ARP poisoning.
  - USe strong authentication to mitigate registration spoofing. cybercriminals routing all incoming calls for the victim to themselves),
  - proxy impersonating (tricking the victim into communicating via a rogue proxy set up by the cybercriminals)
  - and call hijacking (intercepting and rerouting calls to a different path before reaching their destination)
  - Implement firewalls that recognize VoIP to monitor streams and filter abnormal signals.
