### Ethernet
- Ethernet operates in the data link layer and the phyiscal layer

### Data Link Sublayers
- IEEE 802 LAN/MAN protocols, including Ethernet, use the following two separate sublayers of the data link layer to operate.
- They are the Logical Link Control LLC and the Media Ccess Control MAC. 
- The LLC Sublayer communicates between the networking software at the upper layers and the device hardware at the lower layers. It places information in the frame that identifies which network layer protocol is being used for the frame. This information allows multiple Layer 3 protocols, such as IPv4 and IPv6 to use the same network interface and media.
- MAC Sublayer - This sublayer is implemented in hardware and is responsible for data encapsulation and media access control. It provides data link layer addressing and is integrated with various phyisical layer technologies.

### Ethernet Frame Fields
- The minimum Ethernet Frame size is 64 bytes and the expected maximum is 1518 bytes.
- This includes all bytes from the destination MAC address field through the frame check sequence FCS field. The preamble field is not included when describing the size of the frame.
- Any frame less than 64 bytes in length is considered a collision fragment, or runt frame, and is automatically discarded by receiving stations. Frames with more than 1500 bytes of data are considered jumbo or baby giant frames.
- If the size of a transmitted frame is less than the minimum or greater than the maximum, the receiving drops the frame.
- Dropped frames are likely to be the result of collisions or other unwanted signals. They are considered invalid.
- Jumbo frames are usually supported by most Fast Ethernet and Gigabit Ethernet Switches and NICs.

#### Structure of the Frame
- Preamble and Start Frame Delimiter Fields SFD - 7 bytes + the 1st byte, which is the start of the frame. Are used for sync between the sending and receiving devices. They tell the receivers to get ready to receive a new frame.
- Destination MAC - 6 bytes
- Source MAC Address - 6 bytes
- Type / Length - 2 bytesIdentifies the upper layer protocol encapsulated in the Ethernet Frame. Common values are in hexadecimal for IPv6 and IPv6.
- Data Field - 46-1500 bytes Contains the encapsulated data from  ahigher layer. Can use pads to increase the size.
- Frame Check Sequence Field - 4 bytes Used to detect errors in a frame, using a cyclic redundancy check.

- An Ethernet MAC address consistis of a 48-bit binary value

### Unicast MAC Address
- In Ethernet different MAC addresses are used for layer 2 unicast, broadcast and multicast communications.
- A unicast MAC address is the unique address that is used when a frame is sent from a single transmitting device to a single destination device.

### Broadcast MAC Address
- It has a destination MAC Address of FF-FF-FF-FF-FF-FF in hexadecimal, 48 ones in binary and 255 in the host section of the IPv4 address.
- It is flodded out all Ethernet switch ports expect the incoming port.
- It is not forwarded by a router.

### Multicast MAC Address 
- Received and processed by a group of devices on the Ethernet LAN that belong to the same mutlicast group.
- The destination MAC address of 01-00-5E for a IPv4 multicast packet and 33-33 for a IPv6 multicast packet.
- There are other reserved multicast destination MAC addresses for when the encapsulated data is not IP, such as Spanning Tree Protocol STP and Link Layer Discovery PRotocol LDDP.
- It is flodded out all Ethernet switch ports, expect the incoming port, unless the switch is configured for multicast snooping.
- It is not forwarded by a router, unless the routeris configured to route multicast packets.
- The range of IPv4 is 224.0.0.0 to 239.255.255.255.
- IPv6 address begins with ff00::/8
- Because a multicast address represents a group of addresses, a host group, they can only be used as the destination of a packet. The source will always be a unicast address.

## The MAC Address Table
### Switch Fundamentals
- The MAC address table is sometimes referred to as a content addressable memory CAM table.

### Switch Learning and Forwarding
- By default, most Ethernet switches keep an entry in the table for 5 minutes.
- An exisitng MAC address, but on a new port, is treated as a new entry.
- If the destination MAC address is not in the table, the swithc will forward the frame out all ports expects the incoming port. This is called an unkown unicast.
