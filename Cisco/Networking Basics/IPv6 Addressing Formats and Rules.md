- IPv6 has a larger 128-bit address space
- It includes enhancements in comparison to IPv4. One example is Internet Control Message Protocol version 6, which includes address resolution and address autoconfiguration not found in ICMP for IPv4.

## IPv4 and IPv6 Coexistence
- There is no specific data to conclude the migration to IPv6, both will coexist in the near future.
- The IETF has created various protocols and tools to help network administrators migrate their networks to IPv6. These can be divided ionto three different categories:
    - **Dual Stack** - Allows IPv4 and IPv6 to coexist on the same network segment, running both protocols simultaneously.
    - **Tunneling** - Transports an IPv6 packet over an IPv4 network. The IPv6 packet is encapsulated inside an IPv4 packet, similar to other types of data.
    - **Translation** - Network Address Translation 65 allows IPv6 enabled devices to communicate with IPv4 enabled devices using a translation ntechnique similar to NAT for IPv4.
 
## Hexadecimal Number System
- IPv6 are represented using hexadecimal numbers. Uses digits 0 to 9 and letters A to F.
- These 16 digits are represented as hextets allowing us to represent these massive addresses in a much more readable format.
- IPv6 addresses are 128 bits in length and written as a string of hexadecimal values. Every four bits is represented by a single hexadecimal digital, for a total of 32 hexadecimal values. They are not case-sensitive.
- The preferred format for writing an IPv6 address is x:x:x:x:x:x:x:x, with each “x” consisting of four hexadecimal values.
- The term octet refers to the eight bits of an IPv4 address. A hextet is the unofficial term used to refer to a segment of 16 bits, four hexadecimalo values. Each x is a single hextet which is 16 bits of four hexadecimal digits. 
