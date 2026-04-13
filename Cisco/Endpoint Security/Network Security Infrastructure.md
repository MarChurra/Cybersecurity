## Security Devices

### Firewalls
- A firewall is a system, or group of systems, that enforces an access control policy between networks.

- Common Firewall Properties:
  - Firewalls are resistant to network attacks.
  - Firewalls are the only transit point between internal corporate networks and external networks because all traffic flows through the firewall.
  - Firewalls enforce the access control policy.
 
- Firewall Benefits:
  - They prevent the exposure of sensitive hosts, resources, and applications to untrusted users.
  - They sanitize protocol flow, which prevents the exploitation of protocol flaws.
  - They block malicious data from servers and clients.
  - They reduce security management complexity by off-loading most of the network access control to a few firewalls in the network.
 
- Firewall Limitations
  - A misconfigured firewall can have serious consequences for the network, such as becoming a single point of failure.
  - The data from many applications cannot be passed over firewalls securely.
  -  Users might proactively search for ways around the firewall to receive blocked material, which exposes the network to potential attack.
  -  Network performance can slow down.
  -   Unauthorized traffic can be tunneled or hidden as legitimate traffic through the firewall.

### Common Security Architectures
- Firewall design is primarily about device interfaces permitting or denying traffic based on the source, the destination, and the type of traffic. Some designs are as simple as designating an outside network and inside network, which are determined by **two interfaces** on a firewall.
  - Private and Public:
    - With two interfaces the firewall Private and Public is configured as follows:
      - Traffic originating from the private network is permitted and inspected as it travels toward the public network. Inspected traffic returning from the public network and associated with traffic that originated from the private network         is permitted.
      - Traffic originating from the public network and traveling to the private network is generally blocked.
  - Delimitarized Zone:
    - A demilitarized zone (DMZ) is a firewall design where there is typically one inside interface connected to the private network, one outside interface connected to the public network, and one DMZ interface
      - Traffic originating from the private network is inspected as it travels toward the public or DMZ network. This traffic is permitted with little or no restriction. Inspected traffic returning from the DMZ or public network to the private network is permitted.
      - Traffic originating from the DMZ network and traveling to the private network is usually blocked.
      - Traffic originating from the DMZ network and traveling to the public network is selectively permitted based on service requirements.
      - Traffic originating from the public network and traveling toward the DMZ is selectively permitted and inspected. This type of traffic is typically email, DNS, HTTP, or HTTPS traffic. Return traffic from the DMZ to the public network is dynamically permitted.
      - Traffic originating from the public network and traveling to the private network is blocked.
  - Zone'Based Policy Firewalls;
    - Zone-based policy firewalls (ZPFs) use the concept of zones to provide additional flexibility.
    - A zone is a group of one or more interfaces that have similar functions or features.
    - Zones help you specify where a Cisco IOS firewall rule or policy should be applied.
    - By default, the traffic between interfaces in the same zone is not subject to any policy and passes freely
    - However, all zone-to-zone traffic is blocked. In order to permit traffic between zones, a policy allowing or inspecting traffic must be configured.
    - The only exception to this default deny any policy is the router self zone. The self zone is the router itself and includes all the router interface IP addresses.
    - Traffic that should be considered when designing a policy for the self zone includes management plane and control plane traffic, such as SSH, SNMP, and routing protocols.
   
### Firewall Type Descriptions
- Packet Filtering (Stateless) Firewall: Packet filtering firewalls are usually part of a router firewall, which permits or denies traffic based on Layer 3 and Layer 4 information. They are stateless firewalls that use a simple policy table look-up that filters traffic based on specific criteria.
- Stateful Firewall: Stateful firewalls are the most versatile and the most common firewall technologies in use. Stateful firewalls provide stateful packet filtering by using connection information maintained in a state table. Stateful filtering is a firewall architecture that is classified at the network layer. It also analyzes traffic at OSI Layer 4 and Layer 5.
- Application Gateway Firewall: filters information at Layers 3, 4, 5, and 7 of the OSI reference model. Most of the firewall control and filtering is done in software. When a client needs to access a remote server, it connects to a proxy server. The proxy server connects to the remote server on behalf of the client. Therefore, the server only sees a connection from the proxy server.
- Next Generation Firewall: Go beyond stateful firewalls by providing:
  - Integrated intrusion prevention
  - Application awareness and control to see and block risky apps
  - Upgrade paths to include future information feeds
  - Techniques to address evolving security threats
 
- Some other methods of implementing firewalls include:
  - Host-based (server and personal) firewall: A PC or server with firewall software running on it
  - Transparent Firewall: Filters IP traffic between a pair of bridged interfaces.
  - Hybrid Firewall: A combination of the various firewall types. For example, an application inspection firewall combines a stateful firewall with an application gateway firewall.
 
### Intrusion Prevention and Detection Devices
#### IDS and IPS Characteristics
- A networking architecture paradigm shift is required to defend against fast-moving and evolving attacks. This must include cost-effective detection and prevention systems, such as intrusion detection systems (IDS) or the more scalable intrusion prevention systems (IPS). The network architecture integrates these solutions into the entry and exit points of the network.
- A networking architecture paradigm shift is required to defend against fast-moving and evolving attacks. This must include cost-effective detection and prevention systems, such as intrusion detection systems (IDS) or the more scalable intrusion prevention systems (IPS). The network architecture integrates these solutions into the entry and exit points of the network.
- Characteristics of IDS and IPS:
  - Both technologies are deployed as sensors.
  - Both technologies use signatures to detect patterns of misuse in network traffic.
  - Both can detect atomic patterns (single-packet) or composite patterns (multi-packet).
- IDS and IPS technologies are both deployed as sensors. An IDS or IPS sensor can be in the form of several different devices:
  - A router configured with Cisco IOS IPS software
  - A device specificaly designed to provide ddicated IDS or IPS services
  - A network module installed in an adaptive Security Applicance ASA, switch or router.
- A signature is a set of rules that an IDS or IPS uses to detect malicious activity. Signatures can be used to detect severe breaches of security, to detect common network attacks, and to gather information.

### Advantages and Disadvantages of IDS and IPS
- IDS Advantages:
  - An IDS is deployed in offline mode and therefore, it does not impact network performance, does not introduce latency, jitter or other traffic flow issues. It does not affect network functionality if the sensor fails. It only affects the ability of the IDS to analyze the data.
- IDS Disavantages:
  - An IDS sensor cannot stop the packets that have triggered an alert and are less helpful in detecting email viruses and automated attacks, such as worms.
  - Tuning IDS sensors to achieve expected levels of intrusion detection can be very time-consuming. Users deploying IDS sensor response actions must have a well-designed security policy and a good operational uinderstanding of their IDS deployments.
  - An IDS implementation is more vulnerable to network security evasion techniques because it is not inline
- IPS Advantages:
  - An IPS sensor can be configured to drop the trigger packets, the packets associated with a connection, or packets from a source IP address.
  - Because IPS sensors are inline, they can use stream normalization. Stream normalization is a technique used to reconstruct the data stream when the attack occurs over multiple data segments.
- IPS Disadvantages:
  - Because it is deployed inline, errors, failure, and overwhelming the IPS sensor with too much traffic can have a negative effect on network performance.
  - An IPS sensor can affect network performance by introducing latency and jitter.
  - An IPS sensor must be appropriately sized and implemented so that time-sensitive applications, such as VoIP, are not adversely affected.
- Deployment Considerations:
  - You can deploy both an IPS and an IDS. Using one of these technologies does not negate the use of the other. In fact, IDS and IPS technologies can complement each other.
  - For example, an IDS can be implemented to validate IPS operation because the IDS can be configured for deeper packet inspection offline. This allows the IPS to focus on fewer but more critical traffic patterns inline.
 
### Types of IPS
- Host-based IPS:
  - Host-based IPS (HIPS) is software installed on a host to monitor and analyze suspicious activity. A significant advantage of HIPS is that it can monitor and protect operating system and critical system processes that are specific to that host
  - With detailed knowledge of the operating system, HIPS can monitor abnormal activity and prevent the host from executing commands that do not match typical behavior.
  - This suspicious or malicious behavior might include unauthorized registry updates, changes to the system directory, executing installation programs, and activities that cause buffer overflows. Network traffic can also be monitored to prevent the host from participating in a denial-of-service (DoS) attack or being part of an illicit FTP session.
  - HIPS can be thought of as a combination of antivirus software, antimalware software, and a firewall. Combined with a network-based IPS, HIPS is an effective tool in providing additional protection for the host.
  - A disadvantage of HIPS is that it operates only at a local level. It does not have a complete view of the network, or coordinated events that might be happening across the network. To be effective in a network, HIPS must be installed on every host and have support for every operating system.

- Sample IPS Senor Deployment
  - A network-based IPS can be implemented using a dedicated or non-dedicated IPS device. Network-based IPS implementations are a critical component of intrusion prevention. There are host-based IDS/IPS solutions, but these must be integrated with a network-based IPS implementation to ensure a robust security architecture.
  - Sensors detect malicious and unauthorized activity in real time and can take action when required. Sensors are deployed at designated network points. This enables security managers to monitor network activity while it is occurring, regardless of the location of the attack target.

- Specialized Security Applicances
  - AMP:
  - Cisco Advanced Malware Protection is an enterprise-class advanced malware anaLYSIS AND PROTECTION SOLUTION. iT PROVIDES COMPREEHENSIVE MALWARE PROTECTION FOR ORGANIZATIONS BEFORE, DURING, and after an attack.
  - Before an attack, AMP strengthens defenses and protects against known and emerging threats.
  - During an attack, AMP identifies and blocks policy-violating file types, exploit attempts, and malicious files from infiltrating the network.
  - After an attack, or after a file is initially inspected, AMP goes beyond point-in-time detection capabilities and continuously monitors and analyzes all file activity and traffic, regardless of disposition, searching for any indications of malicious behavior. If a file with an unknown or previously deemed “good” disposition starts behaving badly, AMP will detect it and instantly alert security teams with an indication of compromise. It then provides visibility into where the malware originated, what systems were affected, and what the malware is doing.
  - AMP accesses the collective security intelligence of the Cisco Talos Security Intelligence and Research Group. Talos detects and correlates threats in real time using the largest threat-detection network in the world.
- WSA:
  - A Cisco Web Security Appliance (WSA) is a secure web gateway that combines leading protections to help organizations address the growing challenges of securing and controlling web traffic.
  - WSA protects the network by automatically blocking risky sites and testing unknown sites before allowing users to access them. WSA provides malware protection, application visibility and control, acceptable use policy controls, insightful reporting and secure mobility.
  - While WSA protects the network from malware intrusion, it does not provide protection for users who want to connect to the internet directly outside of the protected network, such as at a public Wi-Fi service. In this instance, the user’s PC can be infected with malware which can then spread to other networks and devices. To help protect user PCs from these types of malware infections there is Cisco Cloud Web Security (CWS).
  - CWS together with WSA provides comprehensive protection against malware and the associated impacts. The Cisco CWS solution enforces secure communication to and from the internet and provides remote workers the same level of security as onsite employees when using a laptop issued by the employer. Cisco CWS incorporates two main functions, web filtering and web security, and both are accompanied by extensive, centralized reporting.
- ESA:
  - A Cisco Email Security Appliance (ESA)/ Cisco Cloud Email Security helps to mitigate email-based threats. The Cisco ESA defends mission-critical email systems.
  - The Cisco ESA is constantly updated by real-time feeds from the Cisco Talos, which detects and correlates threats using a worldwide database monitoring system.
  - Utilizes Global Threat Intelligence, SPam Blocking, ADvanced Malware Protection and Outbound message control.
 
## Security Services

### Traffic Control with ACLS
- An Acess Control List is a series of commands that control whether a device forwards or drops packets based on information found in the packet header. When configured, ACLs perform the following tasks:
  - They limit network traffic to increase network performance. For example, if corporate policy does not allow video traffic on the network, ACLs that block video traffic could be configured and applied. This would greatly reduce the network load and increase network performance.
  - They provide traffic flow control. ACLs can restrict the delivery of routing updates to ensure that the updates are from a known source.
  - They provide a basic level of security for network access. ACLs can allow one host to access a part of the network and prevent another host from accessing the same area. For example, access to the Human Resources network can be restricted to authorized users.
  - They filter traffic based on traffic type. For example, an ACL can permit email traffic, but block all Telnet traffic.
  - They screen hosts to permit or deny access to network services. ACLs can permit or deny a user to access file types, such as FTP or HTTP.
  - In addition to either permitting or denying traffic, ACLs can be used for selecting types of traffic to be analyzed, forwarded, or processed. Can be enabled to give priority processing.

### ACLs: Important Features 
- Two types of Cisco IPv4 ACLs are standard and extended. Standard ACLs can be used to permit or deny traffic only from source IPv4 addresses. The destination of the packet and the ports involved are not evaluated.
- Extended ACLs filter IPv4 packets based on several attributes that include:
  - Protocol Type
  - Source IPv4 address
  - Destination IPv4 address
  - Source TCP or UDP ports
  - Destination TCP or UDP ports
  - Optional protocol type information for finer control
- Standard and extended ACLs can be created using either a number or a name to identify the ACL and its list of statements.
- Using numbered ACLs is an effective method for determining the ACL type on smaller networks with more homogeneously defined traffic. However, a number does not provide information about the purpose of the ACL. For this reason, a name can be used to identify a Cisco ACL.
- By configuring ACL logging, an ACL message can be generated and logged when traffic meets the permit or deny criteria defined in the ACL.
- Cisco ACLs can also be configured to only allow TCP traffic that has an ACK or RST bit set, so that only traffic from an established TCP session is permitted. This can be used to deny any TCP traffic from outside the network that is trying to establish a new TCP session.

### SNMP
- Simple Network Management Protocol (SNMP) allows administrators to manage end devices such as servers, workstations, routers, switches, and security appliances, on an IP network.
- It eenables network administrators to monitro and manage network performance, find and solve network problems, and plan for network growth.
- SNMP is an application layer protocol that provides a message format for communication between managers and agents.
- It consists of:
  - SNMP manager that runs SNMP management software.
  - SNMP agents which are the nodes being monitored and managed.
- The Management Information Base (MIB) is a database on the agents that stores data and operational statistics about the device.
- To configure SNMP on a networking device, it is first necessary to define the relationship between the manager and the agent.
- The SNMP manager is part of a network management system (NMS)

### NetFlow
- NetFlow is a Cisco IOS technology that provides statistics on packets flowing through a Cisco router or multilayer switch.
- While SNMP attempts to provide a very wide range of network management features and options, NetFlow is focused on providing statistics on IP packets flowing through network devices.
- NetFlow provides data to enable network and security monitoring, network planning, traffic analysis to include identification of network bottlenecks, and IP accounting for billing purposes.
- NetFlow can monitor that application connection, tracking byte and packet counts for that individual application flow. It then pushes the statistics over to an external server called a NetFlow collector.

### Port Mirroring
- A packet analyzer (also known as a packet sniffer or traffic sniffer) is typically software that captures packets entering and exiting the network interface card (NIC).
- It is not always possible or desirable to have the packet analyzer on the device that is being monitored. Sometimes it is better on a separate station designated to capture the packets.
- Because network switches can isolate traffic, traffic sniffers or other network monitors, such as IDS, cannot access all the traffic on a network segment.
- Port mirroring is a feature that allows a switch to make duplicate copies of traffic passing through a switch, and then send it out a port with a network monitor attached

### Syslog Servers
- When certain events occur on a network, networking devices have trusted mechanisms to notify the administrator with detailed system messages.
- These messages can be either non-critical or significant
- Network administrators have a variety of options for storing, interpreting, and displaying these messages, and for being alerted to those messages that could have the greatest impact on the network infrastructure.
- The most common method of accessing system messages is to use a protocol called syslog.
- Many networking devices support syslog, including routers, switches, application servers, firewalls, and other network appliances. The syslog protocol allows networking devices to send their system messages across the network to syslog servers

### NTP 
- It is important to synchronize the time across all devices on the network because all aspects of managing, securing, troubleshooting, and planning networks require accurate and consistent timestamping. When the time is not synchronized between devices, it will be impossible to determine the order of the events that have occurred in different parts of the network.
- Typically, the date and time settings on a network device can be set using one of two methods:
  - Manual
  - Configuring the Network Time Protocol
- A better solution is to configure the NTP on the network. This protocol allows routers on the network to synchronize their time settings with an NTP server. A group of NTP clients that obtain time and date information from a single source have more consistent time settings. When NTP is implemented in the network, it can be set up to synchronize to a private primary clock or it can synchronize to a publicly available NTP server on the Internet.
- NTP networks use a hierarchical system of time sources. Each level in this hierarchical system is called a stratum. The stratum level is defined as the number of hop counts from the authoritative source. The synchronized time is distributed across the network using NTP.
- NTP servers are arranged in three levels known as strata:
  - Stratum 0:  An NTP network gets the time from authoritative time sources. These authoritative time sources, also referred to as stratum 0 devices, are high-precision timekeeping devices assumed to be accurate and with little or no delay associated with them.
  - Stratum 1: -The stratum 1 devices are directly connected to the authoritative time sources. They act as the primary network time standard.
  - Stratum 2 and lower strata: The stratum 2 servers are connected to stratum 1 devices through network connections. Stratum 2 devices, such as NTP clients, synchronize their time using the NTP packets from stratum 1 servers. They could also act as servers for stratum 3 devices.
  - Smaller stratum numbers indicate that the server is closer to the authorized time source than larger stratum numbers. The larger the stratum number, the lower the stratum level. The max hop count is 15. Stratum 16, the lowest stratum level, indicates that a device is unsynchronized. Time servers on the same stratum level can be configured to act as a peer with other time servers on the same stratum level for backup or verification of time.
 
### AAA Servers
- Authentication: Users and administrators must prove that they are who they say they are., via password and username combinations, challenges, response questions, tokens and so on. It provides a centralized way to control access to the network.
- Authorization: After authentication, authorization defines which resources the authenticated user has access to and actions he can perform.
- Accounting: Accounting records what the user does, including what is accessed, the amount of time the resource is accessed, and any changes that were made. Accounting keeps track of how network resources are used.
- TACAS+ or RADIUS are two options that are utilized to communicate with AAA servers.
- TACAS+ is considered the more secure protocol, since communications are encrpyted. In Radius only the credentials are encrypted.

### VPN
- A VPN is a private network that is created over a public network, usually the internet
- Instead of using a dedicated physical connection, a VPN uses virtual connections that are routed through the internet from the organization to the remote site.
- A VPN is virtual in that it carries information within a private network, but that information is actually transported over a public network. A VPN is private in that the traffic is encrypted to keep the data confidential while it is transported across the public network.
- A VPN is a communications environment in which access is strictly controlled to permit peer connections within a defined community of interest. Confidentiality is achieved by encrypting the traffic within the VPN. Today, a secure implementation of VPN with encryption is what is generally equated with the concept of virtual private networking.
- n the simplest sense, a VPN connects two endpoints, such as a remote office to a central office, over a public network, to form a logical connection. The logical connections can be made at either Layer 2 or Layer 3. Common examples of Layer 3 VPNs are GRE, Multiprotocol Label Switching (MPLS), and IPsec. Layer 3 VPNs can be point-to-point site connections, such as GRE and IPsec, or they can establish any-to-any connectivity to many sites using MPLS.
- IPsec services allow for authentication, integrity, access control, and confidentiality. With IPsec, the information exchanged between remote sites can be encrypted and verified
-  VPNs are commonly deployed in a site-to-site topology to securely connect central sites with remote locations. They are also deployed in a remote-access topology to provide secure remote access to external users travelling or working from home. Both remote-access and site-to-site VPNs can be deployed using IPsec.
