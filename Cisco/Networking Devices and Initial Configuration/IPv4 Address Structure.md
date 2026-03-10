## Network and HOst Portions
- An IPv4 address is a 32-bit hierarchical address that is made up of a network portion and a host portion. To determine which, one must look at the 32-bit stream.
- The bits within the network portion of the address must be identical for all devices that reside in the same network.
- The bits within the host portion of the address must be unique to identify a specific host within a network.
- If two hosts have the same bit-pattern in the specified network portion of the 32-bit stream, those two hosts will reside in the same network.

## Subnet Mask
- IPv4 address - This is the unique IPv4 address of the host.
- Subnet mask- This is used to identify the network/host portion of the IPv4 address.
- The IPv4 subnet mask is used to differentiate the network portion from the host portion of an IPv4 address.
- When an IPv4 address is assigned to a device, the subnet mask is used to determine the network address of the device.
- The network address represents all the devices on the same network.
- Note that the subnet mask does not actually contain the network or host portion of an IPv4 address, it just tells the computer where to look for the part of the IPv4 address that is the network portion and which part is the host portion.
- The actual process used to identify the network portion and host portion is called ANDing.

## Prefix Length
- The number of bits set to 1 in the subnet mask. It is written in slash notation,noted by a /slash.
- 255.0.0.0 - /8
- 255.255.0.0 - /16
- 255.255.255.0 - /24
- 255.255.255.218 - /25

- A network address is also referred to as a prefix or network prefix. Therefore, the prefix length is the number of 1 bits in the subnet mask.
- When representing an IPv4 address using a prefix length, the IPv4 address is written followed by the prefix length with no spaces. For example, 192.168.10.10 255.255.255.0 would be written as 192.168.10.10/24.

## Determining the Network: Logical AND
- A logical AND is one of three Boolean operations used in Boolean or digital logic. The other two are OR and NOT. The AND operation is used in determining the network address.
- In digital logic, 1 represents True and 0 represents False. When using an AND operation, both input values must be True (1) for the result to be True (1).
- To identify the network address of an IPv4 host, the IPv4 address is logically ANDed, bit by bit, with the subnet mask. ANDing between the address and the subnet mask yields the network address.
- The AND operation between an IPv4 host address and subnet mask results in the IPv4 network address for this host.
- In this example, the AND operation between the host address of 192.168.10.10 and the subnet mask 255.255.255.0 (/24), results in the IPv4 network address of 192.168.10.0/24. This is an important IPv4 operation, as it tells the host what network it belongs to.
