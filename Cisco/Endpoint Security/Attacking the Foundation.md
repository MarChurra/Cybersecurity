## IP PDU Details

### IPv4 and IPv6
- IP was designed as a Layer 3 connectionless protocol. It provides the necessary functions to deliver a packet from a source host to a destination host over an interconnected system of networks.
- The protocol was not designed to track and manage the flow of packets. These functions, if required, are performed primarily by TCP at Layer 4.
- IP makes no effort to validate whether the source IP address contained in a packet actually came from that source. For this reason, threat actors can send packets using a spoofed source IP address.
- In addition, threat actors can tamper with the other fields in the IP header to carry out their attacks. Therefore, it is important for security analysts to understand the different fields in both the IPv4 and IPv6 headers.

### IPv4 Packet Header
- Version: Contains a 4-bit binary value set to 0100 that identifies this as an IPv4 packet.
- Internet Header Length: A 4-bit field containing the length of the IP header. The minimum length of an IP header is 20 bytes.
- Differentiated Services or DiffServ DS: Formerly called the Type of Service (ToS) field, the DS field is an 8-bit field used to determine the priority of each packet. The six most significant bits of the DiffServ field are the Differentiated Services Code Point (DSCP). The last two bits are the Explicit Congestion Notification (ECN) bits.
- Total Length: Specifies the length of the IP packet including the IP header and the user data. The total length field is 2 bytes, so the maximum size of an IP packet is 65,535 bytes; however, packets are much smaller in practice.
- Identification, Flag, and Fragment Offset: As an IP packet moves through the internet, it might need to cross a route that cannot handle the size of the packet. The packet will be divided, or fragmented, into smaller packets and reassembled later. These fields are used to fragment and reassemble packets.
- Time To live TTL: Contains an 8-bit binary value that is used to limit the lifetime of a packet. The packet sender sets the initial TTL value, and it is decreased by one each time the packet is processed by a router. If the TTL field decrements to zero, the router discards the packet and sends an Internet Control Message Protocol (ICMP) Time Exceeded message to the source IP address.
- Protocol: Field is used to identify the next level protocol. This 8-bit binary value indicates the data payload type that the packet is carrying, which enables the network layer to pass the data to the appropriate upper-layer protocol. Common values include ICMP (1), TCP (6), and UDP (17).
- Header Checksum: A value that is calculated based on the contents of the IP header. Used to determine if any errors have been introduced during transmission.
- Source IPv4 Address: Contains a 32-bit binary value that represents the source IPv4 address of the packet.Always a unicast address.
- Destination IPv4 Address: Contains a 32-bit binary value that represents the destination IPv4 address of the packet.
- Options and Padding:This is a field that varies in length from 0 to a multiple of 32 bits. If the option values are not a multiple of 32 bits, 0s are added, or padded, to ensure that this field contains a multiple of 32 bits.

### IPv6 Packet Header
- 40 Bytes vs 20 Bytes
- Version: This field contains a 4-bit binary value set to 0110 that identifies this as an IPv6 packet.
- Traffic Class: This 8-bit field is equivalent to the IPv4 Differentiated Services (DS) field.
- Flow Label: This 20-bit field suggests that all packets with the same flow label receive the same type of handling by routers.
- Payload Length: This 16-bit field indicates the length of the data portion or payload of the IPv6 packet.
- Next Header: This 8-bit field is equivalent to the IPv4 Protocol field. It indicates the data payload type that the packet is carrying, enabling the network layer to pass the data to the appropriate upper-layer protocol.
- Hop Limit: This 8-bit field replaces the IPv4 TTL field.
- Source IPv6 Address: 128 bit
- Destination IPv6 Address: 128 bit
- An IPv6 packet may also contain extension headers (EH) that provide optional network layer information. Extension headers are optional and are placed between the IPv6 header and the payload. EHs are used for fragmentation, security, to support mobility, and more.
- Unlike IPv4, routers do not fragment routed IPv6 packets.

### IP Vulnerabilities
- - There are different types of attacks that target IP. Some of the more commmon ones are:
  - ICMP attacks: Threat actors use Internet Control Message Protocol (ICMP) echo packets (pings) to discover subnets and hosts on a protected network, to generate DoS flood attacks, and to alter host routing tables.
  - DoS Attacks: Threat actors attempt to prevent legitimate users from accessing information or services.
  - DDoS Attacks: Similar to a DoS attack, but features a simultaneous, coordinated attack from multiple source machines.
  - Address Spoofing Attacks: Threat actors spoof the source IP address in an attempt to perform blind spoofing or non-blind spoofing.
  - Man-in-the-middle-attack: Threat actors position themselves between a source and destination to transparently monitor, capture, and control the communication. They could simply eavesdrop by inspecting captured packets or alter packets and forward them to their original destination.
  - Session Hijacking: Threat actors gain access to the physical network, and then use an MiTM attack to hijack a session.
 
### ICMP Attacks:
  - Threat actors use ICMP for reconnaissance and scanning attacks. This enables them to launch information-gathering attacks to map out a network topology, discover which hosts are active (reachable), identify the host operating system (OS fingerprinting), and determine the state of a firewall.
  - Threat actors also use ICMP for DoS and DDoS attack
  - ICMP Flood:
    - ICMP echo request and echo reply: This is used to perform host verification and DoS attacks.
    - ICMP unreachable: This is used to perform network reconnaissance and scanning attacks.
    - ICMP mask reply: This is used to map an internal IP network.
    - ICMP redirects: This is used to lure a target host into sending all traffic through a compromised device and create a MiTM attack.
    - ICMP router discovery: This is used to inject bogus route entries into the routing table of a target host.
  - ICMP for IPv4 (ICMPv4) and ICMP for IPv6 (ICMPv6) are susceptible to similar types of attacks.

### Amplification and Reflection Attacks
- Threat actors often use amplification and reflection techniques to create DoS attacks.
- Amplification: Sends an ICMP request from an client to several hosts
- Reflection: That clients receives the ECHO replys from the Echo request.
- Newer forms of amplification and reflection attacks such as DNS-based reflection and amplification attacks and Network Time Protocol (NTP) amplification attacks are now being used.
- Threat actors also use resource exhaustion attacks. These attacks consume the resources of a target host to either to crash it or to consume the resources of a network.

### Address Spoofing Attacks:

#### Threat Actor Spoofs a Server´s MAC Address
- IP address spoofing attacks occur when a threat actor creates packets with false source IP address information to either hide the identity of the sender, or to pose as another legitimate user
- The threat actor can then gain access to otherwise inaccessible data or circumvent security configurations. Spoofing is usually incorporated into another attack such as a Smurf attack.
- They can be:
  - Non-blind spoofing: The threat actor can see the traffic that is being sent between the host and the target. The threat actor uses non-blind spoofing to inspect the reply packet from the target victim. Non-blind spoofing determines the state of a firewall and sequence-number prediction. It can also hijack an authorized session.
  - Blind spoofing:  The threat actor cannot see the traffic that is being sent between the host and the target. Blind spoofing is used in DoS attacks.
- MAC address spoofing attacks are used when threat actors have access to the internal network. Threat actors alter the MAC address of their host to match another known MAC address of a target host
- The attacking host then sends a frame throughout the network with the newly-configured MAC address. When the switch receives the frame, it examines the source MAC address.
- The switch overwrites the current CAM table entry and assigns the MAC address to the new port. It then forwards frames destined for the target host to the attacking host.

## TCP and UDP Vulnerabilities

### TCP Segment Header
- While some attacks target IP, this topic discusses attacks that target TCP and UDP.
- CP segment information appears immediately after the IP header.
- The Control Bits in the TCP Header are:
  - URG - Urgent pointer field
  - ACK - Acknowledgement field significant
  - PSH - Push function
  - RST - Reset the connection
  - SYN - Syncronize sequence numbers
  - FIN - No more data from sender
 
### TCP Attacks

#### TCP SYN Flood Attack
- Network applications use TCP or UDP ports. Threat actors conduct port scans of target devices to discover which services they offer.
- The TCP SYN Flood attack exploits the TCP three-way handshake.
- The threat actor continually sending TCP SYN session request packets with a randomly spoofed source IP address to a target.
- The target device replies with a TCP SYN-ACK packet to the spoofed IP address and waits for a TCP ACK packet. Those responses never arrive. Eventually the target host is overwhelmed with half-open TCP connections, and TCP services are denied to legitimate users.

#### Terminating a TCP Connection 
- TCP Reset Attack: A TCP reset attack can be used to terminate TCP communications between two hosts.
- TCP uses a four-way exchange to close the TCP connection using a pair of FIN and ACK segments from each TCP endpoint.
- A TCP connection terminates when it receives an RST bit. This is an abrupt way to tear down the TCP connection and inform the receiving host to immediately stop using the TCP connection. A threat actor could do a TCP reset attack and send a spoofed packet containing a TCP RST to one or both endpoints.

- TCP Session Hijacking: TCP session hijacking is another TCP vulnerability. Although difficult to conduct, a threat actor takes over an already-authenticated host as it communicates with the target. The threat actor must spoof the IP address of one host, predict the next sequence number, and send an ACK to the other host. If successful, the threat actor could send, but not receive, data from the target device.

 ### UDP Segment header and Operation
- UDP is commonly used by DNS, DHCP, TFTP, NFS, and SNMP. It is also used with real-time applications such as media streaming or VoIP.
- UDP is a connectionless transport layer protocol. It has much lower overhead than TCP because it is not connection-oriented and does not offer the sophisticated retransmission, sequencing, and flow control mechanisms that provide reliability.
- Although UDP is normally called unreliable, in contrast to TCP’s reliability, this does not mean that applications that use UDP are always unreliable, nor does it mean that UDP is an inferior protocol. It means that these functions are not provided by the transport layer protocol and must be implemented elsewhere if required.
- The low overhead of UDP makes it very desirable for protocols that make simple request and reply transactions. For example, using TCP for DHCP would introduce unnecessary network traffic. If no response is received, the device resends the request.

 ### UDP Attacks
 - UDP is not protected by any encryption. You can add encryption to UDP, but it is not available by default. The lack of encryption means that anyone can see the traffic, change it, and send it on to its destination.
 - Changing the data in the traffic will alter the 16-bit checksum, but the checksum is optional and is not always used.
 - When the checksum is used, the threat actor can create a new checksum based on the new data payload, and then record it in the header as a new checksum. The destination device will find that the checksum matches the data without knowing that the data has been altered. This type of attack is not widely used.

- UDP Flood Attacks: You are more likely to see a UDP flood attack. In a UDP flood attack, all the resources on a network are consumed. The threat actor must use a tool like UDP Unicorn or Low Orbit Ion Cannon. These tools send a flood of UDP packets, often from a spoofed host, to a server on the subnet. The program will sweep through all the known ports trying to find closed ports. This will cause the server to reply with an ICMP port unreachable message. Because there are many closed ports on the server, this creates a lot of traffic on the segment, which uses up most of the bandwidth. The result is very similar to a DoS attack.
