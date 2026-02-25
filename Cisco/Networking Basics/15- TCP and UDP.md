## TCP and UDP port Numbers
- When a message is delivered using either TCP or UDP, the protocols and services requested are identified by a port number, as shown in the figure.
- A port is a numeric identifier within each segment that is used to keep track of specific convesations between a client and a server.
- Every message that a host sends contains both a source and destination port.
- Ports are assigned and managed by an organization known as the ICANN Internet corporation for Assigned Names and Numbers.
- Ports are broken into three categories and range in number from 1 to 65.535
    - Well-Known Ports - Destination ports that are associated with common network applications are identified as well-lnown ports. These ports are in the range of 1 to 1023.
    - Registered Ports - Ports through 1024 to 49151 can be used as either source or destination ports. Can be used by organizations to register specific applications such as IM applications.
    - Private Ports - Ports 49152 to 65535 are often used as source ports, and used by any application.
- Some appllications amy use both TCP and UDP. For example, DNS uses UDP when clients send requests to a DNS server. However, communication between two DNS servers always use TCP.

## Socket Pairs
- The source and destination poprts are placed within the segment, The segments are then encapsulated within an IP packet.
- The combination of the source IP address and source port number, or the destination IP address and destination port number is known as a socket.
- The request will include the Layer 2 and Layer 3 of the host and the server.
- The host port number is dynamically generated.
- The socket is sued to identify the server and service being request by the client.

## Netstat
- Lists the protocols in use, the local addresses and port numbers, the foreign address and port numbers, and the connection state, of connections made in the computer.
- By default the netstat command will attempt to resolve IP addresses to domain names and port numbers to well-known applications. The n- option can be used to display IP address and port numbers in their numerical form.
