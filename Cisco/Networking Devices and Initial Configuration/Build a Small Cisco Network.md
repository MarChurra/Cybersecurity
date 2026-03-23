## Basic Switch Configuration Steps
- The Cisco switch only needs to be assigned basic security information before being connected to the network.
-  Elements that are usually configured on a LAN switch include: host name, management IP address information, passwords, and descriptive information.
-  The switch host name is the configured name of the device.
-  It is helpful if the device name includes the location where the switch will be installed. An example might be: SW_Bldg_R-Room_216.
-  A management IP address is only necessary if you plan to configure and manage the switch through an in-band connection on the network.
-  A management address enables you to reach the device through Telnet, SSH, or HTTP clients
-  The IP address information that must be configured on a switch is essentially the same as you configure on a PC: IP address, subnet mask, and default gateway.
-  In order to secure a Cisco LAN switch, it is necessary to configure passwords on each of the various methods of access to the command line.
-  The minimum requirements include assigning passwords to remote access methods, such as Telnet, SSH and the console connection. Y
-  You must also assign a password to the privileged mode in which configuration changes can be made.

### Swtich Virtual Interface Configuration
- To access the switch remotely, an IP address and a subnet mask must be configured on the switch virtual interface (SVI). To configure an SVI on a switch, use the interface vlan 1 global configuration command.
- Vlan 1 is not an actual physical interface but a virtual one.
- Next, assign an IPv4 address using the ip address ip-address subnet-mask interface configuration command
- Finally, enable the virtual interface using the no shutdown interface configuration command.

Sw-Floor-1# configure terminal
Sw-Floor-1(config)# interface vlan 1
Sw-Floor-1(config-if)# ip address 192.168.1.20 255.255.255.0
Sw-Floor-1(config-if)# no shutdown
Sw-Floor-1(config-if)# exit
Sw-Floor-1(config)# ip default-gateway 192.168.1.1

## Configure Initial Router Settings

### Basic Router Configuration Steps
1. Configure the device name
  - **hostname {hostname}**
2. Secure priviliged EXEC mode
  - **enable secret password**
3. Secure user EXEC mode
  - **line console 0** > **password {password}** > **login**
4. Secure Remote Telnet / SSH Access
  - **line vty 0 4** > **password {password}** > **login** > **transport input {ssh | telnet | none | all}**
5. Secure all passwords in the config file
  - **exit** > **service password-encryption**
6. Provide legal notification
  - **banner motd delimiter message delimiter**
7. Save the configuration
  - **copy running-config startup-config**


  
