## Destination on Same Network
- Layer 2 physical addresses (Ethernet MAC addresses) are used to deliver the data link frame with the encapsulated IP packet from one NIC to another NIC that is on the same network. If the destination UP address is on the same network, the destination MAC address will be that of the destination device.
- Physical address (the MAC address) – Used for NIC-to-NIC communications on the same Ethernet network.
- Logical address (the IP address) – Used to send the packet from the source device to the destination device. The destination IP address may be on the same IP network as the source, or it may be on a remote network.

## Destination on Remote Network
- When the destination IP address is on a remote network, the destination MAC address will be the address of the host default gateway.
- Since they are not on the same network, the router determines the best path to forward the IPv4 Packet, by de-encapsulating the Layer 2 information. Using the destination IPv4 address, it determines the next-hop device, and then encapsulates the IPv4 packet in a new data link frame for the outgoing interface.
- For IPv4 MAC ADdress resolution, we have ARP and for IPv6 packets, the proccess is ICMPv6 Neightbor Discovery

## Broadcast Domains
- When a host receives a message address to the broadcast address, it accepts and processes the message as though the message was directly addressed to it.
- When a host sends a broadcast message, switches forward the message to every connected host within the same local network.For this reason, a LAN, a network with one or more Ethernet Switches, is also referred to as a broadcast domain.
- If too many hosts are connected to the same broadcast domain, broadcast traffic can become excessive.
- The number of hosts and the amount of network traffic that can be supported on the local network, is limited by the capabilities of the switches used to connect them.
- To improve performance as the network scales, it is often necessary to divide one local network into multiple networks, or broadcast domains.
- Routers are used to divide the network into multiple broadcast domains

## Access Layer Communication
- On a LAN a NIC only acccepts a frame if the destination address is either the broadcast MAC address or else corresponds to the MAC address of the NIC
- Most network applications, however, rely on the logical destination IP address to identify the location of the servers and clients.
- In this scenario, where the host only knows the logical destination IP address, to identify the destination MAC address, the sending host can use ARP to discover the MAC addres of any host on the same local network, or ND for IPv6.
