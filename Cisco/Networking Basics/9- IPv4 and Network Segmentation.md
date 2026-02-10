## Unicast
- Unicast transmission refers to one device sending a message to one other device in one-to-one communications
- A unicast packet has a destination IP address that is a unicast address, going to a single recipient. A source IP address can only be a unicast address.

## Broadcast
- The broadcast transmission refers to a device sending a message to all the devices on a network in one-to-all communications.
- A Broadcast packet has a destination IP address with all ones in the host porition, or 32 one bits.
- These use IPv4 broadcast packets. There are no broadcast packets with IPv6
- The broadcast packet must be processed by all devices in the same broadcast domain. A broadcast domain identifies all hosts on the same network segment.
- A Broadcast may be directed or limited.
- A directed broadcast is sent to all hosts on a specific network.
- A limited broadcast is sent to 255.255.255.255
- By defaults, routers do not forward broadcasts

## Multicast
- Multicast transmission reduces traffic by allowing a host to send a single packet to a selected set of hosts that subscribe to a multicast group
- This packet has a destination UIP address that is a multicast address. IPv4 has reserver the 224.0.0.0 to 239.255.255.255 adresses as a multicast range
- Hosts that can receive these packets are called multicast clients. These clientes use services requested by a client program to subscribe to the multicast group
- These are called multicast clients. They use services request by a client program to subscribe to the multicast group
- Each multicast group is rpesented by a single IPv4 multicast destination adress
- Routing procols such as OSPF use multicast transmittions and use the multicast address 244.0.0.5 as the destination IPv4 address 

## Routing to the Internet
### Private IPv4 Addresses and Network Address Translatioon **NAT**
- Most enterprise and home networks, use private IPv4 addresses for addressing all internal devices **intranet** including hosts and routers. However, rpivate addresses are not globallly routable.
- Packets with a private address must be filtered (discarded) or translated to a public address before forwarding the packet to an ISP with NAT.
- This is done on the router that connects the internal network to the ISP network.

## Special Use IPv4 Addresses
- Network addresses and broadcast addresses cannot be assigned to hosts.
- There are also special addresses that can be assigned to hosts, but with restrictions on how those hosts can interact within the network.

  ### Loopback Addresses
  - 127.0.0.0 / 8 or 217.0.0.1 to 127.255.255.254 are commonly indeitfied as only 217.0.0.1
  - These are special addresses used by a host to direct traffic to itself.

  ### Link-Local Addresses
  - 169.254.0.0/16 or 169.254.0.1 to 169.254.255.254 are commonly known as the Automatic Private IP Addressing **APIPA** addresses or self-assigned addresses. They are used by a Windows client to self-configure in the event that the client cannot obtain an IP addressing through other methods. 
