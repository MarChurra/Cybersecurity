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
    
