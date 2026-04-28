## Benefits of a ZPF
- Basic Security Zone Topology
  - Classic Firewall: Traditional configuration model in which a firewall policy is applied on interfaces
  - Zone-Based Policy Firewall: Model in which interfaces are assigned to security zoens, and firewall policy is applied to traffic moving between the zones.
- The primary motivations for network security professionals to migrate to the ZPF model are structure and ease of use. The structured approach is useful for documentation and communication. The ease of use makes network security implementations more accessible to a larger community of security professionals.
- There are several benefits of a ZPF:
  - It is not dependent on ACLs.
  - The router security posture is to block unless explicitly allowed.
  - Policies are easy to read and troubleshoot. C3PL is a structured method to create traffic policies, based on events, conditions and actions. This provides scalability because one policy affects any given traffic, instead of needing multiple ACLs and inspection actions for different types of traffic.
  - Virtual and phyisical interfaces can be grouped into zones
  - Policies are applied to unidirectional traffic between zones
 
## ZPF Design
1. Determine the zones: The administrator focuses on the separation of the network into zones. Zones establish the security borders of a network. A zone defines a boundary where traffic is subjected to policy restrictions as it crosses to another region of the network. For example, the public network would be one zone and the internal network would be another zone.
2. Establish policies between zones: For each pair of 'source-destination' zones, define the sessions that clients in the source zones can request from servers in destination zones. For traffic that is not based on the concept of sessions, the administrator must define unidirectional traffic flows from source to destination and vice versa. Policies are unidirectional and are defined based on source and destination zones, which are known as zone pairs. 
3. Design the physical intrastructure: After the zones have been identified, and the traffic requirements between them documented, the administrator must design the physical infrastructure. The administrator must take into account security and availability requirements when designing the physical infrastructure. This includes dictating the number of devices between most-secure and least-secure zones and determining redundant devices.
4. Identity subsets within zones and merge traffic requirements: For each firewall device in the design, the administrator must identify zone subsets that are connected to its interfaces and merge the traffic requirements for those zones.

## ZPF Operation

### ZPF Actions
- Policies identify actions that the ZPF will perform on network traffic. Three possible actions can be configured to process traffic by protocol, source and destination zones (zone pairs), and other criteria.
  - Inspect: This performs Cisco IOS stateful packet inspection
  - Drop: Analogous to a deny statement in an ACL. A log option is available
  - Pass: Analogous to a permit statement in an ACL. Does not track the state of connections or sessions within the traffic.

### Rules for Transit Traffic
- The rules depend on whether or not the ingress and egress interfaces are members of the same zone:
  - If neither interface is a zone member, then the resulting action is to pass the traffic.
  - If both interfaces are members of the same zone, then the resulting action is to pass the traffic.
  - If one interface is a zone member, and the other is not, then the resulting action is to drop the traffic, regardless of whether a zone-pair exists.
  - If both interfaces belong to the same zone-pair and a policy exists, then the resulting action is inspect, allow or drop, as defined by the policy.

### Basic Security Zone Topology
- Traffic transiting through router interfaces is subject to several rules governing interface behavior.

### Rules for Traffic to the Self Zone
- The self zone is the router itself and includes all of the IP addresses assigned to the router interfaces
- This is traffic that originates at the route ror is addressed to a router interface.
- Specifically, the traffic is either for device management, such as SSH, or traffic forwarding control, such as routing protocol traffic.
- The rules for a ZPF are different for the self zone.
- The rules depend on whether the the router is the source or the destination of the traffic. If the router is the source or destination, then all traffic is permitted. The only expection is if the source and destination are a zone-apri with a specific service-policy. In that case, the policy is applied to all traffic.

## Configure a ZPF

### Zone-Based policy Firewall Configuration Steps
1. Create the zones
2. Identify traffic with a class-map
3. Define an action with a policy-map
4. Identify a zone pair and match it to a policy-map
5. Assign zones to the appropriate Interfaces

### Create the Zones
- Which itnerfaces should be included in the zones?
- What will be the name for each zone?
- What traffic is necessary between the zones in which direction?

- Router(config)# zone security zone-name

### Identify Traffic
- The second step is to use a class-map to identify the traffic to which a policy will be applied. A class is a way of identifying a set of packets based on its contents using “match” conditions. Typically, you define a class so that you can apply an action to the identified traffic that reflects a policy. A class is defined with class-maps.
- There are several types of class-maps. For a ZPF configuration, use the inspect keyword to define a class-map. Determine how packets are evaluated when multiple match criteria exist. Packets must meet one of the match criteria (match-any) or all of the match criteria (match-all) to be considered a member of the class.

- Router(config)# class-map type inspect [match-any | match-all] class-map-name

### Define an Action
- The third step is to use a policy-map to define what action should be taken for traffic that is a member of a class.

- R1(config)# policy-map type inspect policy-map-name
- R1(config-pmap)# class type inspect class-map-name
- R1(config-pmap-c)# {inspect | drop | pass}

### Identify a Zone-Pair and Match to a Policy
- The fourth step is to identify a zone pair and associate that zone pair to a policy-map.
- Create a zone-pair with the zone-pair security command. Then use the service-policy type inspect command to attach a policy-map and its associated action to the zone-pair.

- Router(config)# zone-pair security zone-pair-name source {source-zone-name | self} destination {destination-zone-name | self}
- Router(config-sec-zone-pair)# service-policy type inspect policy-map-name

### Assign Zones to Interfaces
- The fifth step is to assign zones to the appropriate interfaces. Associating a zone to an interface will immediately apply the service-policy that has been associated with the zone. If no service-policy is yet configured for the zone, all transit traffic will be dropped. Use the zone-member security command to assign a zone to an interface.

### Considerations
- When configuring a ZPF with CLI, there are some factors to consider:
  - The router never filters the traffic between interfaces in the same zone.
  - An interface cannot belong to multiple zones. To create a union of security zones, specify a new zone and appropriate policy map and zone pairs.
  - ZPF can coexist with Classic Firewall although they cannot be used on the same interface. Remove the ip inspect interface configuration command before applying the zone-member security command.
  - Traffic can never flow between an interface assigned to a zone and an interface without a zone assignment. Applying the zone-member configuration command always results in a temporary interruption of service until the other zone-member is configured.
  - The default inter-zone policy is to drop all traffic unless otherwise specifically allowed by the service-policy configured for the zone-pair.
  - The zone-member command does not protect the router itself (traffic to and from the router is not affected) unless the zone- pairs are configured using the predefined self zone.
