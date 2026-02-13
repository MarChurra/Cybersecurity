## Static IPv4 Address Assignment
- IPv4 can be assigned either statically or dynamically.
- With static assignement, the network administrator must manually configure the network information for a host, including the fixed IP address, Subnet mask and Default Gateway.

## Dynamic IPv4 Address Assignment
- The IPv4 are assigned via a protocol known as Dynamic Host Configuration Protocol.
- Addresses are leased for a period of time, taken from a pool.

## DHCP Servers
- There can be a server dedicated for this purpose, or a home router, which acts as an server and client for DHCP.
- The DHCP cliente makes a request to a DHCP server, to request the IP address.
- The client sends a broadcast packet called as a DHCP Discover, to query for a DHCP server that can assign him an IPv4 Address
- When the server receives the request, it then sends an DHCP offer, containing the IP address, subnet mask and default gateway.
- The host will then use DHCP Request to request those configurations.
- It finishes with a DHCP ACK from the DHCP server. 
