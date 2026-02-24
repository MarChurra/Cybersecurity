## Need for Routing
- Devices that are beyond the local network segment are known as remote hosts.
- When a source device sends a packet ro a remote destionation device, then the help of routers and routing is needed. Routing is the process of identifying the best path to a destination.
- A router is a networking device that connects multiple Layer 3 IP networks. At the distribution layer of the network, routers direct traffic and perform other functions critical to efficient network operation.
- Routers, like switches, are able to decode and read the messages that are sent to them.
- Switches only make the forwarding decision based on the Layer 2 Mac address, while routers make their decisions based on the Layer 3 IP address.
- The router reads the network portion of the destination IP address and uses it to find which one of the attached networks is the best way to forward the message to the destination.
- Anytime the network portion of the IP addresses of the sources and destination hosts do not match, a router must be used to forward the message.
- The router receives the message, de-encapsulates the Ethernet Frame and then reads the destination IP address in the IP packet. It then determines where to forward the message. It then determines where to forwad the message, it re-encapsulates the packet back into a new frame and forwards the frame on to its destination.

  ## Routing Table Entries
  - Routers use routing tables to store information to move information between local and remote networks.
  - Routing tables contain the addresses of networks and the best path to reach them
  - Entries can be made to the routing table dynamically by information received from other routers in the network, or manually entered by a network administrator
  - Routers use the routing tables to determine which interface to used to forward a message to its intended destination.
  - If the router cannot determine where to forward a message, it will drop it.
  - Network administrators configure a static default route that is placed into the routing table so that a packet will not be dropped due to the destination network not being in the routing table.
  - A default route is the interface through which the router forwards a packet containing an unknown destination IP network address.
  - This default route usually connects to another route that can forward the packet towards its final destination network.

## The Default Gateway
- When a host sends a message to another host located on the same network, it will forward the message directly.
- A host will use ARP to discover the MAC address of the destination host.

- When a host needs to send a message to a remote network, it must use the router. The host includes the IP address of the destination host within the packet, just like before. Hpwever. when the frame it encapsulated, it uses the MAC address of the router as the destination for the frame.
- The host is given the address of the router through the default gateway address configured in its TCP/IP settings.
- The default gateway address is the address of the router interface connected to the same local network as the source host.
- If the default gateway is missconfigured, messages addressed to hosts on remote networks cannot be delivered.

## Local Area Networks
- All local networks within a LAN are under one administrative control, they typically use Ethernet or wireless protocols and they support high data rates.
- Intranet is often used to refer to a private LAn that belongs to an organization, and is designed to be accessible only by the members of the organization, employees or others with authorization.
