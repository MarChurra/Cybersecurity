## The Network Layer
- The network layer, or OSI layer 3, provides services to allow end devices to exhcange data across networks.
- IPv4 and IPv6 are the principle network layer communication protocols.
- Other network layer protocols include rouitng protocols such as Open SHortest Path First OSPF and messaging protocols such as ICMP Internet Control Message Protocol.
- To accomplish end-to-end communications across network boundaries, network layer protocols perform four basic operations:
  - Addressing End Devices - with a unique IP address
  - Encapsulation - The Protocol Data Unit PDU from the transport layer is encapsulated into a packet. Performed by the source of the IP packet.
  - Routing - The network layer provides services to direct the packets to a destination host on another network, via a router. Each router in the travel to the destination is called an hop.
  - De-Encapsulation - When the packet arrives ath desinity host, the host checks the IP header of the packet. If the destination IP address within the header matches its own IP address, the IP header is removed from the packet.The resulting layer 4 PDU is passed up to the appropriate service at the transport layer.
- Unlike the transport Layer, the Layer 3 specifies the packet structure and processing used to carry the data from one host to another.
- The data goes to the layert of 4 as Data, gets added an segment, via encapsulation at layer 4, a packet at layer 3 and a frame at layer 2, before going as data.

### IP Encapsulation
- IP encapsulates the transport layer segment or other data by adding an IP header., used to develier teh packet to the destination host.
- The process of encapsulating data layer by layer enables the services at the different layers to develop and scale without affecting each other.
- One characetristic of the media that the network layer considers is the maxiumum size of the PDU tat each medium can transport, referred as the MTU Maximum Transmission Unit.
- The MTU is passewd from the data link to the network layer.
- A device, like a router, may need to fragment the packet, because of the MTU limit.
- IPv6 packets cannot be fragmented by the router.

### IPv4 Packet Header Fields
- Protocl header driagrams whcih are read left ot right, top to bottom, provide a visual to refer to when discussing protocol fields.
- Version - Contains a 4-bit binary value set to 0100 that identifies this as an IPv4 packet.
- Differentiated Services or DiffServ (DS) - Formerly called the type of service (ToS) field, the DS field is an 8-bit field used to determine the priority of each packet. The six most significant bits of the DiffServ field are the differentiated services code point (DSCP) bits and the last two bits are the explicit congestion notification (ECN) bits.
- Time to Live (TTL) – TTL contains an 8-bit binary value that is used to limit the lifetime of a packet. The source device of the IPv4 packet sets the initial TTL value. It is decreased by one each time the packet is processed by a router. If the TTL field decrements to zero, the router discards the packet and sends an Internet Control Message Protocol (ICMP) Time Exceeded message to the source IP address. Because the router decrements the TTL of each packet, the router must also recalculate the Header Checksum.
- Protocol – This field is used to identify the next level protocol. This 8-bit binary value indicates the data payload type that the packet is carrying, which enables the network layer to pass the data to the appropriate upper-layer protocol. Common values include ICMP (1), TCP (6), and UDP (17).
- Header Checksum – This is used to detect corruption in the IPv4 header.
- Source IPv4 Address – This contains a 32-bit binary value that represents the source IPv4 address of the packet. The source IPv4 address is always a unicast address.
- Destination IPv4 Address – This contains a 32-bit binary value that represents the destination IPv4 address of the packet. The destination IPv4 address is a unicast, multicast, or broadcast address.

### IPv6 
- Increased address space - IPv6 addresses are based on 128-bit hierarchical addressing as opposed to IPv4 with 32 bits.
- Improved packet handling - The IPv6 header has been simplified with fewer fields.
- Eliminates the need for NAT - With such a large number of public IPv6 addresses, NAT between a private IPv4 address and a public IPv4 is not needed. This avoids some of the NAT-induced problems experienced by applications that require end-to-end connectivity.
- One of the major design improvements of IPv6 over IPv4 is the simplified IPv6 header.
- For example, the IPv4 header consists of a variable length header of 20 octets (up to 60 bytes if the Options field is used) and 12 basic header fields, not including the Options field and Padding field.
- For IPv6, some fields have remained the same, some fields have changed names and positions, and some IPv4 fields are no longer required, as highlighted in the figure.

  - Version - This field contains a 4-bit binary value set to 0110 that identifies this as an IP version 6 packet.
  - Traffic Class - This 8-bit field is equivalent to the IPv4 Differentiated Services (DS) field.
  - Flow Label - This 20-bit field suggests that all packets with the same flow label receive the same type of handling by routers.
  - Payload Length - This 16-bit field indicates the length of the data portion or payload of the IPv6 packet. This does not include the length of the IPv6 header, which is a fixed 40-byte header.
  - Next Header - This 8-bit field is equivalent to the IPv4 Protocol field. It indicates the data payload type that the packet is carrying, enabling the network layer to pass the data to the appropriate upper-layer protocol.
  - Hop Limit - This 8-bit field replaces the IPv4 TTL field. This value is decremented by a value of 1 by each router that forwards the packet. When the counter reaches 0, the packet is discarded, and an ICMPv6 Time Exceeded message is forwarded to the sending host,. This indicates that the packet did not reach its destination because the hop limit was exceeded. Unlike IPv4, IPv6 does not include an IPv6 Header Checksum, because this function is performed at both the lower and upper layers. This means the checksum does not need to be recalculated by each router when it decrements the Hop Limit field, which also improves network performance.
  - Source IPv6 Address - This 128-bit field identifies the IPv6 address of the sending host.
  - Destination IPv6 Address - This 128-bit field identifies the IPv6 address of the receiving host.
 
