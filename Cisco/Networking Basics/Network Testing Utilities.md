## Troubleshooting Commands
- ipconfig - Displays IP configuration information
- ping - Tests Connections to other IP hosts
- netstat - Displays network connections
- tracdert - Displays the route taken to the destination
- nslookup - Directly queries the name server for information on a destination domain

## ipconfig
- ipconfig /all - Adds information about MAC address and DNS Servers. Shows if DHCP is active and its information.
- ipconfig /release & ipconfig /renew

## Ping
- When a ping is sent to an IP address, a packet known as an echo request is sent across the network to the specified IP address.
- If the host receives the echo request, it responds with a packet known as an echo reply.
- If ping command is sent to outside the LAN, a packet is first sent to a DNS server to resolve the name to an IP address.
- If a ping tot eh IP works, but not to the hostname, there is likely a problem with the DNS.
- If neither ping is successful, then network connectivity along the path to the destination is most likely the problem.
- If this occurs, it is common practice to ping the default gateway. If the ping to the default gateway is successful, the problem is not local.
- If the ping to the default gateway fails, the problem resides on the local network.
- In some cases, the ping may fail but network connectivity is not the problem. A ping may fail due to the firewall on the sending or receiving device, or a router along the path that is blocking the pings.
