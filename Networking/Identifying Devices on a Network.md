## IP Addresses
-This address is permeable, in contrast with the MAC (Media Access Control)
-An IP is divided between 4 Octets (192.168.1.1) each one with a possibility between 0-255 for an IPV4.
-This number is calculated through a technique known as IP addressing & subnetting.
-Can be allocated to different devices, but can only be allocated to a single device one at a time.
-It can be a public or private IP address, depending if it is an private or public network
-A public address ised to identify the device on the Internet, whereas a private address is used to identify a device amongst other devices, within a local network.
-Data sent from the local IP, will be sent via the i9nternet. Data sent to other LAn devices, will use the private IP. The Public IP is given by the ISP.
-IPv6 is a new iteration of the IP, that can support up to 340 trillion adresses, while IPv4 can withstand 4.29 billion devices.

## MAC Addresses
-Devices on a network will all have a physical NIC (Network Interface Card) which is a microchip board found on the motherboard. This network interface is assigned a unique address at the factory, called a MAC.
-Its a twlve-character, hexadecimal numbersplit into two´s and separated by a colon, known as separators.
-The first six characters represent thae company that made the NIC. The last six is a unique number.
-MAC addresses can be faked or spoofed. It can happen when a networked device pretends to identify as another using its MAC address. When this happens, it can often break poorly implemented security designs that assume that devices talking on a network are trustworthy.


## Ping (ICMP)
-Ping is a fundamental network tool. Ping uses Internet control Message Protocol ICMP packets to determine the performance of a connection between devices. Such as if the connection exists, or is reliable.
-The time taken for ICMP packets travelling between devices is measured by ping, such as in the screenshot below. This measuring is done using ICMP´s echo packet and then ICMP´s echo reply form the target device. 
