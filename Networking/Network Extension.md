## Port Forwarding
- An essential component in connecting applications and services to the internet. Without it, applications and services such as web servers are only available to devices within the same direct network.
- Port Forwading opens specific ports during data transmission.

## Firewalls
- Its a device within a network responsible for determining what traffic is allowed to enter and exit. It can permit or deny traffic from entering, based on predetermined factors.
    - Where Traffic comes from
    - Where the traffic is going
    - What port is the traffic for
    - What protocol is the traffic using
- Firewalls perform packet inspection to determine the answers to these questions.
- They can be dedicated pieces of hardware to residential routers, or softwares such as Snort
- They can be categorized as:
    - **Stateful** - Uses the entire information from a connection, rather than inspecting individual packets. This firewall determines the beahviour of a device based upon the entire connection. Consumes many resources as the decision making is dynamic.
    - **Stateless** - Ues a static set of rules to determine whether or not individual pakcets are acceptable or not. For example, a device sending a bad packet will not necessarily mean that the entire device is blocked. Uses fewer resources, but much simpler. Only as effective as the rules defined. Are great when receiving large amounts of traffic from a set of hosts.

## VPN Basics
- A Virtual Private Network is a technology that allows devices on separate networks to communicate securely by creating a dedicated path between each other over the Internet (**tunnel**). Devices within this tunnel form their own private network.
- It allows, for example, for two remote offices to be connected.
- VPN technologyes uses end-to-end encryption to protect data sent.
- It offers anonymity, since the data is not tracked by an ISP.
    - **PPP** - USed by PPTP to allow for authetnication and provide encryption of data. Work by using a private key a nd a public certificate, similar to SSH. A private key & certificate must match for you to connect. Its a non-routable technology.
    - **PPTP** - Point-To-Point-Tunneling-Protocol is the technology that allows the data from PPP to travel and leave a network. Uses an weaker encryption.
    - **IPSec** - Internet Protocol Security encrypts data using the existing IP framework. More difficult to setup, but stronger protection.

## LAN Networking Devices
- A router connects networks and passes data between them. It does this by using routing.
- Routing is the label given to the process of data travelling across networks. Routing involves creating a path between networks so that this data can be sucessfully delivered.
- They operate at the Layer 3 of the OSI model.

## Switch
- A dedicated networking device responsible for providing a means of connecting to multiple devices. Switches can facilitate many devices using Ethernet Cables.
- Operate at both layer 2 and 3 of the OSI model. These are exclusive.
- A technology called **VLAN** called Virtual Local Area Network, allows specific devices within a network to be virtually split up. This split means they can all benefit from things such as an Internet Connectionn, but are treated separately.
- It adds security, becasue it means that rules in place determine how specific devices communicate with each other.
