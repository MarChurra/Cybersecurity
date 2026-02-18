## Routetrs as Gateways
- The router provides a gateway through which hosts on one network can communicate with hosts on different networks. Each interface on a router is connected to a separate network.
- The IPv4 address assigned to the interface identifies which local network is connected directly to it.
- Every host on the network must use the router as a gateway to other networks. Each host must know the IPv4 address of the router interface, connected to the host´s network. This address is known as the default gateway address, which can be static or received dynamically by DHCP.
- When a wireless router is configured to be a DHCP server for the local network, it automatically sends the conrrect interface IPv4 address to the hosts as the default gateway address. In this manner, all hosts on the network can use that Ipv4 address to forward messages to hosts located at the ISP and get access to host on the internet.

## Routers as Boundaries Between Networks
  - The wireless router acts as a DHCP server for all local hosts attached to it.
  - Since the DHCP server assigns internal or private IP addresses to the hosts in the local network, it ensures, by default, the internal network is not directly acessible from the internet.
  - The DHCP server is typically the first host address on that network, the default gateway.
  - It also provides the subnet mask information and its own interface IPv4 address as the default gateway.
  - Many ISP also use DHCP servers to provide IPv4 address to the internet side of the wireless router installed at their customer sites. Referred as the internet side of the wireless router.
  - The router, when connected to the ISP, acts like a DHCP client to receive the correct external network IPv4 address for the internet interface. ISP usually provide an intenret routable address, which enables hosts connected to the wireless router to have access to the internet.

## Network Address Translation NAT
- Once a request goes to the router, directed to an address outside the local network, the router uses NAT to translate the source local IP address to an public one, encapsulating the request with that public address.
