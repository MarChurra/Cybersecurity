## What is an ACL?
- Routers make routing decisions based on information in the packet header. Traffic entering a router interface is routed solely based on information within the routing table. The router compares the destination IP address with routes in the routing table to find the best match and then forwards the packet based on the best match route. That same process can be used to filter traffic using an access control list (ACL).
- An ACL is a series of IOS commands that are used to filter packets based on information found in the packet header. By default, a router does not have any ACLs configured. However, when an ACL is applied to an interface, the router performs the additional task of evaluating all network packets as they pass through the interface to determine if the packet can be forwarded.
- An ACL uses a sequential list of permit or deny statements, known as access control entries (ACEs) / ACL statements.
- When network traffic passes through an interface configured with an ACL, the router compares the information within the packet against each ACE, in sequential order, to determine if the packet matches one of the ACEs. This process is called packet filtering.
- Several tasks performed by routers require the use of ACLs to identify traffic. The table lists some of these tasks with examples.
  - Limit network traffic to increase network performance, such as using ACLs to block video traffic.
  - Provide traffic flow control, to restrict the delivery of routing updates to only those that come from a known source.
  - Provide a basic level of security for network access, to limit access to specified networks
  - Filter traffic based on traffic type
  - Screen hosts to permit or deny access to network services
  - Provide priority to certain classes of network traffic

### Packet Filtering
- Packet filtering controls access to a network by analyzing the incoming and/or outgoing packets and forwarding them or discarding them based on given criteria. Packet filtering can occur at Layer 3 or Layer 4.
- Cisco routers support two types of ACLs:
  - Standard ACLs: Only filter at Layer 3 using the IPv4 source address
  - Extended ACLs: Filter at layer 3 using the source and or destination IPv4 address. Can also filter at Layer 4 using TCP, UDP ports and optional protocol type information.

### Numbered and Named ACLs
- ACLs number 1 to 99, or 1300 to 1999 are standard ACLs while ACLs number 100 to 199, or 2000 to 2699 are extended ACLs

### Named ACLs
- Named ACLs is the preferred method to use when configuring ACLs. Specifically, standard and extended ACLs can be named to provide information about the purpose of the ACL
- The ip access-list global configuration command is used to create a named ACL

### ACL Operation
- ACLs define the set of rules that give added control for packets that enter inbound interfaces, packets that relay through the router, and packets that exit outbound interfaces of the router.
- ACLs do not act on packets that originate from the router itself
- An inbound ACL filters packets before they are routed to the outbound interface. An inbound ACL is efficient because it saves the overhead of routing lookups if the packet is discarded. If the packet is permitted by the ACL, it is then processed for routing.
- Inbound ACLs are best used to filter packets when the network attached to an inbound interface is the only source of packets that need to be examined.
- An outbound ACL filters packets after being routed, regardless of the inbound interface. Incoming packets are routed to the outbound interface and then they are processed through the outbound ACL. Outbound ACLs are best used when the same filter will be applied to packets coming from multiple inbound interfaces before exiting the same outbound interface.
- When an ACL is applied to an interface, it follows a specific operating procedure. For example, here are the operational steps used when traffic has entered a router interface with an inbound standard IPv4 ACL configured:
  1. The router extracts the source IPv4 address from the packet header
  2. The router starts at the top of the ACL and compares the source IPv4 address to each ACE in a sequential order
  3. When a match is made, the router carries out the instruction, either permitting or denying the packet, and the remaining ACEs in the ACL, if any, are not analyzed.
  4. If the source IPv4 address does not match any ACEs in the ACL, the packet is discarded because there is an implicit deny ACE automatically applied to all ACLs.
- The last ACE statement of an ACL is always an implicit deny that blocks all traffic. By default, this statement is automatically implied at the end of an ACL even though it is hidden and not displayed in the configuration.
- An ACL must have at least one permit statement otherwise all traffic will be denied due to the implicit deny ACE statement.

## Wildcard Masking

### Overview
- An IPv4 ACE uses a 32-bit wildcard mask to determine which bits of the addres to examine for a match.
- Wildcard masks are also used by the Open Shortest Path First routing protocol OSPF
- A wildcard mask is similiar to a subnet mask in that it uses ANDing process to identify which bits in an IPv4 address to match.
- However, they differ, in the way they match binary 1s and 0s.
- Wildcard masks use the following rules to match binary 1s and 0s:
  - Wildcard mask bit 0: Match the corresponding bit value in the address
  - Wildcard mask bit 1: Ignore the corresponding bit value in the address

## Configure ACLs
- All access control lists (ACLs) must be planned. However, this is especially true for ACLs requiring multiple access control entries (ACEs).

### Numbered Standard IPv4 ACL Syntax
- To create a numbered standard ACL, use the following global configuration command:
- Router(config)# access-list access-list-number {deny | permit | remark text} source [source-wildcard] [log]
- Use the no access-list to remove a numbered standard ACL.

### Named Standard IPv4 ACL Syntax
- Naming an ACL makes it easier to understand its function. To create a named standard ACL, use the following global configuration command:
- Router(config)# ip access-list standard access-list-name.
- Use the no ip access-list standard access-list-name global configuration command to remove a named standard IPv4 ACL.
- To remove an ACL from an interface, first enter the no ip access-group interface configuration command. To remove the ACL from the router, use the no access-list global configuration command.
- The internal logic applied to the ordering of standard ACL statements does not apply to extended ACLs. The order in which the statements are entered during configuration is the order they are displayed and processed.

## Protocols and Port Numbers
- Extended ACL can be configured via Protocol or Port Number

### TCP Established Extended ACL
- TCP can also perform basic stateful firewall services using the TCP established keyword.
- The keyword enables inside traffic to exit the inside private network and permits the returning reply traffic to enter the inside private network.
- However, TCP traffic generated by an outside host and attempting to communicate with an inside host is denied.
- The established keyword can be used to permit only the return HTTP traffic from requested websites, while denying all other traffic.

### Named Extended IPv4 ACL Syntax
- Router(config)# ip access-list extended access-list-name

### Named Extended IPv4 ACL Example
- Named extended ACLs are created in essentially the same way that named standard ACLs are created.
- The topology in the figure is used to demonstrate configuring and applying two named extended IPv4 ACLs to an interface:
  - Surfing: Permits HTTP and HTTPS traffic to exit to the internet
  - Browsing: Will only permit returning web traffic to the deinside hosts while all other traffic exiting the R1 interfgace is denied.
 
### Implement ACLs
- Ensure the last statement is an implicit deny any or deny ip any any.
- Remember that statement order is important because ACLs are processed top-down.
- As soon as a statement is matched the ACL is exited.
- Always filter from the most specific to the most generic. For example, deny a specific host and then permit all other hosts.
- Remember that only one ACL is allowed per interface, per protocol, per direction.
- Remember that new statements for an existing ACL are added to the bottom of the ACL by default.
- Remember that router-generated packets are not filtered by outbound ACLs.
- Place standard ACLs as close to the destination as possible.
- Place extended ACLs as close to the source as possible.

- Enabling the log parameter on a Cisco router or switch seriously affects the performance of that device. The log parameter should only be used when the network is under attack, and an administrator is trying to determine who the attacker is.

### Where to Place ACLs
- Extended ACLs shoudl be located as close as possible to the source of the fraffic to be filtered. This way, undersirable traffic is denied close to the source network without crossing the network infrastructure.
- Standard ACLs should be located as close to the destinatio. If a standard ACL was placed at the soruce of the traffic, the permit or deny will occur based on the given source address, no matter where the traffic is destined.

## Mitigating ATtacks with ACLs

### Mitigate Spoofing Attacks
- ACLs can be used to mitigate many network threats, such as IP address spoofing and denial of service (DoS) attacks. Most DoS attacks use some type of spoofing. IP address spoofing overrides the normal packet creation process by inserting a custom IP header with a different source IP address. Attackers can hide their identity by spoofing the source IP address.
- There are many well-known classes of IP addresses that should never be seen as source IP addresses for traffic entering an organization’s network. For example, in the figure the S0/0/0 interface is attached to the internet and should never accept inbound packets from the following addresses:
- All zero Addresses
- Broadcast addresses
- Local host addresses
- Automatic Private IP Addressing addresses (169.245.0.0/16)
- IP Multicast address range
- Reserved Private Address

  
