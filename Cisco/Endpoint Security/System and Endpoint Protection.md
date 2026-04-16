## Defending Systems and Devices
- Fileless Attacks: Piggyback from regular programs, and run scripts, leaving no traces. Harder to detect, but get remove upon computer shutdown.
- Patches and upgrades are often combined into a service pack.
- Updates can be security updates, critical updates and serivce packs.
- A patch management tool can be used to manage patches locally instead of using the vendors online update service.
- Local computers can instaed receive updates from a local, verified server.

- HIDS: Host Intrusion Detection System software is installed on a device or server to monitor suspicious activity. It stores logs locally and can affect system performance.
- HIPS: Host Intrusion Prevention System is a software that monitors a device for known attacks and anomalies If it detects malicious activity, the tool can send an alarm, log the malicious activity, reset the connection, and drop the packets.
- Endpoint Detection and Response: An integrated security solution that continuously monitors and collects data from an endpoint device.It then analyzes the data and responds to any threats it detects.
- DLP: Data Loss Prevention tools provide a centralized way to ensure that sensitive data is not lost, misused or accessed by unauthorized users.
- Next generation Firewall: A security device that combines a traditional firewall with the other network-device-filtering functions. For example, an application firewall using in-line deep packet inspection DPI or an IPS.

### Boot Integrity
- Ensures that the system can be trusted and has not been altereted while the OS loads.
- Firmware: software instructions about basic computer functions, stored on a small memory chip on the motherboard. The basic input/output BIOS is the first program that runs when you turn on the computer.
- UEFI runs in 64-bit mode.

### Secure boot
- A security standard to ensure that a device boots using trusted software. On boot, the firmware checks the signature of each piece of boot software, including UEFI firmware drivers, UEFI applications and the OS. If the signatures are valid, the system boots and the firmware gives control to the OS.

### Measured Boot
- Provides stronger validation than Secure Boot. It measures each component starting with the firmware through to the boot start drivers, and stores the measurements in the TCMP chip to create a log.
- The log can be tested remotely to verify the boot state of the client.
- It can identify untrusted applications trying to load, and it also allows antimalware to load earlier.

### Antivirus/Antimalware Software
- Can be:
  - Signature-Based: This approach recognizes various characetristics of known malware files
  - Heuristics-Based: This approach recognizes general features shared by various type of malware.
  - Behaviour-based: This approach employs analysis of suspicious behaviour
- Host-based antivirus protection is also known as agent-based. Agent-based antivirus runs on every protected machine.
- Agentless antivirus protection performs scans on hosts from a centralized system.
- Agentless systems have become popular for virtualized environments in which multiple OS instances are running on a host simultaneously-
- One approach to intrusion prevention is the use of distributed firewalls. Distributed firewalls combine features of host-based firewalls with centralized management. The management function pushes rules to the hosts and may also accept log files from the hosts.

### Host-Based Intrustion Detection Architecture 
-  The distinction between host-based intrusion detection and intrusion prevention is blurred. In fact, some sources refer to host-based intrusion detection and prevention systems (HIPDS). Because the industry seems to favor the use of the acronym HIDS,
-  A host-based intrusion detection system (HIDS) is designed to protect hosts against known and unknown malware. A HIDS can perform detailed monitoring and reporting on the system configuration and application activity. It can provide log analysis, event correlation, integrity checking, policy enforcement, rootkit detection, and alerting. A HIDS will frequently include a management server endpoint.
-  A HIDS is a comprehensive security application that combines the functionalities of antimalware applications with firewall functionality. A HIDS not only detects malware but also can prevent it from executing if it should reach a host. Because the HIDS software must run directly on the host, it is considered an agent-based system.

### HIDS Operation
-  Polymorhpism: This means that variations of a type, or family, of malware may be created by attackers that will evade signature-based detections by changing aspects of the malware signature just enough so that it will not be detected.
-  An additional set of strategies are used to detect the possibility of successful intrusions by malware that evades signature detection:
  - Anomaly-based: Host system behavior is compared to a learned baseline model of normal behavior. Significant deviations from the baseline are interpreted as the result of some sort of intrusion.
  - Policy-based: Normal system behavior is described by rules, or the violation of rules, that are predefined. Violation of these policies will result in action by the HIDS

## Application Security

### Attack Surface
- Recall that a vulnerability is a weakness in a system or its design that could be exploited by a threat. An attack surface is the total sum of the vulnerabilities in a given system that is accessible to an attacker.
- The attack surface can consist of open ports on servers or hosts, software that runs on internet-facing servers, wireless network protocols, and even users.
- The attack surface is continuing to expand, as shown in the figure. More devices are connecting to networks through the Internet of Things (IoT) and Bring Your Own Device (BYOD)
- Much of network traffic now flows between devices and some location in the cloud. Mobile device use continues to increase. All of these trends contribute to a prediction that global IP traffic will increase threefold in the next five years.
- The SANS Institute describes three components of the attack surface:
  - Network Attack Surface: The attack exploits vulnerabilities in networks. This can include conventional wired and wireless network protocols, as well as other wireless protocols used by smartphones or IoT devices. Network attacks also exploit vulnerabilities at the network and transport layers.
  - Software Attack Surface: The attack is delivered through exploitation of vulnerabilities in web, cloud, or host-based software applications.
  - Human Attack Surface: The attack exploits weaknesses in user behavior. Such attacks include social engineering, malicious behavior by trusted insiders, and user error.

### Application Block and Allow List
- One way of decreasing the attack surface is to limit access to potential threats by creating lists of prohibited applications. This is known as blocklisting.
- Allow lists are created in accordance with a security baseline that has been established by an organization. The baseline establishes an accepted amount of risk, and the environmental components that contribute to that level of risk. Non-allowlisted software can violate the established security baseline by increasing risk.
- Websites can also be whitelisted and blacklisted. These blacklists can be manually created, or they can be obtained from various security services. Blacklists can be continuously updated by security services and distributed to firewalls and other security systems that use them.

### Sandboxing
- Sandboxing is a technique that allows suspicious files to be executed and analyzed in a safe environment. Automated malware analysis sandboxes offer tools that analyze malware behavior. These tools observe the effects of running unknown malware so that features of malware behavior can be determined and then used to create defenses against it.
- 
