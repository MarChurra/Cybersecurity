** Unicast
- Unicast transmission refers to one device sending a message to one other device in one-to-one communications
- A unicast packet has a destination IP address that is a unicast address, going to a single recipient. A source IP address can only be a unicast address.

** Broadcast
- The broadcast transmission refers to a device sending a message to all the devices on a network in one-to-all communications.
- A Broadcast packet has a destination IP address with all ones in the host porition, or 32 one bits.
- These use IPv4 broadcast packets. There are no broadcast packets with IPv6
- The broadcast packet must be processed by all devices in the same broadcast domain. A broadcast domain identifies all hosts on the same network segment.
- A Broadcast may be directed or limited.
- A directed broadcast is sent to all hosts on a specific network.
- A limited broadcast is sent to 255.255.255.255
- By defaults, routers do not forward broadcasts

** Multicast
- Multicast transmission reduces traffic by allowing a host to send a single packet to a selected set of hosts that subscribe to a multicast group
- This packet has a destination UIP address that is a multicast address. IPv4 has reserver the 224.0.0.0 to 239.255.255.255 adresses as a multicast range
- Hosts that can receive these packets are called multicast clients. These clientes use services requested by a client program to subscribe to the multicast group
- These are called multicast clients. They use services request by a client program to subscribe to the multicast group
- Each multicast group is rpesented by a single IPv4 multicast destination adress
- Routing procols such as OSPF use multicast transmittions and use the multicast address 244.0.0.5 as the destination IPv4 address 
