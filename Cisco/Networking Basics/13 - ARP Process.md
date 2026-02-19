## Destination on Same Network
- Layer 2 physical addresses (Ethernet MAC addresses) are used to deliver the data link frame with the encapsulated IP packet from one NIC to another NIC that is on the same network. If the destination UP address is on the same network, the destination MAC address will be that of the destination device.
- Physical address (the MAC address) – Used for NIC-to-NIC communications on the same Ethernet network.
- Logical address (the IP address) – Used to send the packet from the source device to the destination device. The destination IP address may be on the same IP network as the source, or it may be on a remote network.

## Destination on Remote Network
- When the destination IP address is on a remote network, the destination MAC address will be the address of the host default gateway.
- Since they are not on the same network, the router determines the best path to forward the IPv4 Packet, by de-encapsulating the Layer 2 information. Using the destination IPv4 address, it determines the next-hop device, and then encapsulates the IPv4 packet in a new data link frame for the outgoing interface.
- For IPv4 MAC ADdress resolution, we have ARP and for IPv6 packets, the proccess is ICMPv6 Neightbor Discovery
