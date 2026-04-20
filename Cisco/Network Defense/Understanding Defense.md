## Defense-in-Depth

### Assets, Vulnerabilities, Threats
- Cybersecurity analysts must prepare for any type of attack. It is their job to secure the assets of the organization’s network. To do this, cybersecurity analysts must first identify:
  - Assets: Anything of value to an organization that must be protected including servers, infrastructure devices, end devices, and the greatest asset, data.
  - Vulnerabilities: A weakness in a system or its design that could be exploited by a threat actor.
  - Threats:  Any potential danger to an asset.

### Identify Assets
- As an organization grows, so do its assets. Consider the number of assets a large organization would have to protect. It may also acquire other assets through mergers with other companies. The result is that many organizations only have a general idea of the assets that need to be protected.
- The collection of all the devices and information owned or managed by the organization are assets. The assets constitute the attack surface that threat actors could target. These assets must be inventoried and assessed for the level of protection needed to thwart potential attacks.
- Asset management consists of inventorying all assets, and then developing and implementing policies and procedures to protect them. This task can be daunting considering many organizations must protect internal users and resources, mobile workers, and cloud-based and virtual services.
- Further, organizations need to identify where critical information assets are stored, and how access is gained to that information.

### Asset Clarification
- Asset classification assigns an organization’s resources into groups based on common characteristics. The most critical information needs to receive the highest level of protection and may even require special handling.
- A labeling system can be used to determine how valuable, how sensitive, and how critical the information is.

  - Step 1: Determine the proper asset identification category:
    - Information assets
    - Software assets
    - Physical assets
    - Services

    - Step 2: Establish asset accountability by identifying the owner of each information asset and each piece of software:
    - Identify the owner for all information assets
    - Identify the owner for all application software

    - Step 3: Determine the criteria for classification:
    - Confidentiality
    - Value
    - Time
    - Access Rights
    - Destruction

    - Step 4: Implement a classification schema:
    - Adopt a consistent way of identifying information to ensure uniform protection and easier monitoring.

### Asset Standardization
- Asset standards identify specific hardware and software products used by an organization.
- When a failure occurs, prompt action helps to maintain both access and security. If an organization does not standardize its hardware selection, personnel may need to scramble to find a replacement component. Non-standard environments require more expertise to manage, and they increase the cost of maintenance contracts and inventory.

### Asset Lifecycle Stages
- For cybersecurity specialists, part of the job is to manage information assets and related systems throughout that asset’s lifecycle.
  - Procurement: The organization purchases the assets based on the needs identified from data gathered to justify the purchase. The asset is added to the organization’s inventory.
  - Deployment: The asset is assembled and inspected to check for defects or other problems. Staff perform tests and install tags or barcodes for tracking purposes.The asset moves from inventory to in-use.
  - Utilization: This is the longest stage of the cycle. The asset’s performance is continuously checked. Upgrades, patch fixes, new license purchases and compliance audits are all part of the utilization stage.
  - Maintenance: Maintenance helps to extend an asset’s productive life. Staff may modify or upgrade the asset.
  - Disposal: At the end of the asset’s productive life, it must be disposed of. All data must be wiped from the asset. Disposal may include dismantling an asset for parts. Any parts that can cause an environmental hazard must be disposed of according to local guidelines.

### Identify Vulnerabilities
- Identified e-banking Threats:
  - Threat identification provides an organization with a list of likely threats for a particular environment. When identifying threats, it is important to ask several questions:
    - What are the possible vulnerabilities.
    - Who may want to exploit those vulnerabilities to access specific information assets.
    - What are the consequences if system vulnerabilities are exploited and assets are lost.
  - The threat identification for an e-banking system would include:
    - Internal System compromise: The attacker uses the exposed e-banking servers to break into an internal bank system.
    - Stolen Customer data: An attacker steals the personal and finacial data of bank customers from the db.
    - Phony Transactions from an external server: An attacker alters the code of the e-banking application and makes transactions by inptersonating a legitimate user.
    - Phony transactions using a solen customer PIN or smart card
    - Insider attack on the system: A bank employee finds a flaw in the system from which to mount an attack
    - Data input errors: A user inputs incorrect data or makes incorrect transaction requests
    - Data center destruction: A cataclysmic event severely damages or destroys the data center.
  - Identifying vulnerabilities on a network requires an understanding of the important applications that are used, as well as the different vulnerabilities of that application and hardware. This can require a significant amount of research on the part of the network administrator.

### Identify Threats
- Defense-In-Depth Approach
  - Organizations must use a defense-in-depth approach to identify threats and secure vulnerable assets. This approach uses multiple layers of security at the network edge, within the network and on network endpoints.
  - One eample topology could be:
    - Edge Router: The first line of defense. It has a set of rules specifying which traffic it allows or denies. It passes all conections that are intended for the internal LAN to the firewall.
    - Firewall: A checkpoint device that performs additional filtering and tracks the state of the connections. It denies the initiation of connections from the outside (untrusted) networks to the inside (trusted), while enabling internal users to establish two-way connections to the untrusted networks. It can also perform user authentication (autehtnication proxy) to grant external remote users access to internal network resources.
    - Internal Router: It can apply the final filtering rules on the traffic before it is forwarded to the destination.
  - Routers and firewalls are not the only devices that are used in a defense-in-depth approach. Other security devices include IPS, AMP (Advanced Malware Protection), web and email content security systems, identity services, network access controls and more.
  - In the layered defense-in-depth security approach, the different layers work together to create a security architecture in which the failure of one safeguard does not affect the effectiveness of the other safeguards.
 - There are two common anolagies that are used to describe a defense-in-depth approach:
   - Security Onion: a threat actor would have to peel away at a network’s defenses layer by layer in a manner similar to peeling an onion. Only after penetrating each layer would the threat actor reach the target data or system.
   - Security Artichoke: Threat actors no longer have to peel away each layer. They only need to remove certain “artichoke leaves.” The bonus is that each “leaf” of the network may reveal sensitive data that is not well secured.

### Defense in Depth Strategies:
- If an organization only has one security measure in place to protect data and information, then cybercriminals only need to get past that one single defense to steal information or cause other harm. To make sure data and infrastructure remain secure, an organization should create different layers of protection.
  - Layering: To make sure data and information remains available, an organization must set up different layers of protection, creating a barrier of multiple defenses that work together to prevent attacks. A good example of layering is an organization storing its top-secret documents on a password-protected server in a locked building that is surrounded by an electric fence.
  - Limiting: Limiting access to data and information reduces the possibility of a security threat. An organization should restrict access so that each user only has the level of access required to do their job.
  - Diversity: If all defense layers were the same, it would not be very difficult for cybercriminals to succeed in an attack. The layers must be different so that if one layer is penetrated, the same technique will not work on all the others which would compromise the whole system. Furthermore, an organization will normally use different encryption algorithms and authentication systems to protect data in different states.
  - Obscurity: Obscuring information can also protect data and information. An organization should not reveal any information that cybercriminals can use to identify which Operating System (OS) a server is running, or the type or make of equipment or software it uses.
  - Simplicity: Complexity does not necessarily guarantee security. If an organization implements complex systems that are hard to understand and troubleshoot, this may backfire. If employees do not understand how to configure a solution properly, such as setting up their account using an unnecessarily complex process, this may make it just as easy for cybercriminals to compromise those systems.
  
