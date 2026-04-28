## Firewall Operation 
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
- Firewall Limitations:
  - A misconfigured firewall can have serious consequences for the network, such as becoming a single point of failure.
  - The data from many applications cannot be passed over firewalls securely.
  -  Users might proactively search for ways around the firewall to receive blocked material, which exposes the network to potential attack.
  -  Network performance can slow down.
  - Unauthorized traffic can be tunneled or hidden as legitimate traffic through the firewall.

## Types of Firewalls
- Packet Filtering (Stateless) Firewall: Usually part of a router firewall, which permits or denies traffic based on Layer 3 and Layer 4 information. Use a simple policy table look-up that filters traffic based on specific criteria.
- Stateful Firewall: The most versatile and most common firewalls. These provide stateful packet filtering by using connection information maintained inn a state table. Stateful filtering is a firewall architecture that is classified at the network layer, while also analyzing Layer 4 and 5.
- Application Gateway Firewall: An application gateway firewall (proxy firewall), filters information at Layer 3, 4, 5 and 7 of the Osi model. Most of the firewall control and filtering is done in software. When a client accesses a remote server, it connects to a proxy server, which connecs to the remove server on behalf of the client. Therefore, the server only sees a connection from the proxy server.
- Next Generation Firewall: These go beyond stateful, by providing Integrated IPS, Application awareness and control to see and block risky apps, Upgrade paths to include future information feeds and Techniques to address evolving security threats.
- Other methods of implementing firewalls include:
  - Host-Based (server and personal) firewall
  - Transparent Firewall: Filters IP traffic between a pair of bridged interfaces
  - Hybrid Firewall: A combination of the various firewall types. For example, an application inspection firewall combines a stateful firewall with an application gateway firewall.
 
## Packet FIltering Firewall Benefits and Limitations
- Packet filtering firewalls are usually part of a router firewall, which permits or denies traffic based on Layer 3 and Layer 4 information.
- They are stateless firewalls that use a simple policy table look-up that filters traffic based on specific criteria
- For example, SMTP servers listen to port 25 by default. An administrator can configure the packet filtering firewall to block port 25 from a specific workstation to prevent it from broadcasting an email virus.
- These allow for simple rule sets, have low impact on network performance, are easy to implement and widely supported by most routers. Provide an initial degree of security at the network layer and perform almost all the tasks of a high-end firewall at a lower cost.
- SInce they do not represent a complete firewall solution, the packet filters are suspectible to IP spoofing, as long as the packets meet ACL criteria.
- Packet filters do not reliably filter fragmented packets, since the TCP header is in the first fragment.
- Packet filters use complex ACLs which can be difficult to implement and maintain
- Packet filters cannot dynamically filter certain services, such as sessions that use dynamic port negotiations.

## Stateful Firewall Benefits and Limitations
- Often used as a primary means of defense by filtering unwanted, unnecessary or undesirable traffic.
- Strengthen packet filtering by providing more stringent control over security
- Improve performance over packet filters or proxy servers.
- Defend against spoofing and DoS attacks by determining whether packets belong to an existing connection or are from an unauthorized source.
- Provide more log information

- However, these firewalls cannot prevent application layer attacks, because they do not examine the actual contents of the HTTP connection.
- Not all protoocls are stateful. UDP and ICMP do not generate connection information for a stable table, and do not have as much support for filtering.
- It is difficult tot rack connections that use dynamic port negotiation. Some applications open multiple connections.
- They do not support user authhentication

## Firewalls In Network Design

### Common Security Architectures
- Firewall design is primarily about device interfaces permitting or denying traffic based on the source, the destination, and the type of traffic. Some designs are as simple as designating an outside network and inside network, which are determined by two interfaces on a firewall.
- Private and Public: The public network (outside) is untrusted and the private network (inside) is trusted. It allows to send inspected traffic from the inside to the outside. It allows replied traffic to the inside, but blocks all the other traffic.
- DMZ: There is one inside interface connected to the private network, one outside interface connected to the public network, and one DMZ interface.
- Zone-based Policy Firewalls: ZPFs use the concept of zones to provide additional flexibility. A zone is a group of one or more interface that have similar functions or features. Zones help you specify where a Cisco IOS firewall rule or policy should be applied.

## Layered Defense
1. Network Core security: Protects against malicious software and traffic anomalies, enforces network policies, and ensures survivability
2. Perimeter security: Secures boundaries between zones
3. COmmunication Security: Provides information assurance
4. Endpoint Security: Provides identity and device security policy compliance

- A layered defense uses different types of firewalls that are combined in layers to add depth to the security of an organization.
- Policies can be enforced between the layers and inside the layers. These policy enforcement points determine whether traffic is forwarded or discarded.
- A bastion host is a hardened computer that is typically located in the DMZ
- The traffic moves to the internal destination host only after successfully passing through all policy enforcement points between the outside router and the inside network. This type of DMZ setup is called a screened subnet configuration.
- A layered defense approach is not all that is needed to ensure a safe internal network. A network administrator must consider many factors when building a complete in-depth defense:
  - Firewalls typically do not stop intrusions that come fromh osts within a network or zone
  - Firewalls do not protect against rogue access point installations
  - Firewalls do not replace backup and disaster recovery mechanisms resulting from attack or hardware failure
  - Firewalls are no substitute for informed administrators and users
- Position firewalls at security boundaries.
- Deny all traffic by default
- Permit only services that are needed
- Enesure that physical access to the firewall is controlled
- Regularly monitor firewall logs
- Practice change management for firewall configuration changes
- Remember that firewalls primarily protect from technical attacks originating from the outside.
