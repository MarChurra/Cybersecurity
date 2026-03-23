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

## Secure the Devices
### Password Recommendations
- Use a password lenght of 8-10 characters
- Make passwords complex, with a mix of uppercase, lowercase, numbers and special characters
- Avoid passwords based on repetion, common dictionary words, letter or number sequences, suernames relative or pet names.
- Change the password often
- Do not write passwsords down and leave them in obvious places
- On cisco routers, leading spaces are ignored for passwords, but spaces are after the first character are not. This allows you to create a passphrase.

### Secure Remote Access
- One way to acess remotely to the device is to use a PC attached to the console port
- This type fof connection is frequently used for initial device configuration
- Setting a password for console connection access is done in global configuration mode. These commands prevent unauthorized users from accessing user mode from the console port.
- SSH is the preferred method because it is more secure. When the device is accessed through the network, it is considered a vty connection. The password must be assigned to the vty port.
- By default, many Cisco switches support up to 16 vty lines that are numbered 0 to 15.
- The number of vty lines supported on a Cisco router varies with the type of router and the IOS version
- However, five is the most common number of vty lines configured on a router.
- A password needs to be set for all available vty lines. The same password can be set for all connections.
- To verify that the passwords are set correctly, use the show running-config command. These passwords are stored in the running-configuration in plaintext. It is possible to set encryption on all passwords stored within the router so that they are not easily read by unauthorized individuals.
- The global configuration command service password-encryption ensures that all passwords are encrypted.

### Enable SSH
1. Verify SSH support - Show IP SSH CMD
2. Configure the IP Domain - ip domain-name CMD
3. Generate RSA key pairs - SSH version 2 is more secure. Issue the **ip ssh version 2** global configuration mode command. Generating an RSA key pair automatically enables SSH. Use the **crypto key generate rsa** global configuration mode cmd to enable the SSH server on the switch and generate an RSA key pair. To delete the RSA key pair, use the crypto key zeroize rsa global configuration mode command. After the RSA key pair is deleted, the SSH server is automatically disabled.
4. Configure user authentication - The SSH server can authenticate users locally or use an authentication server. To use the local authentication method, create a username and password pair with the username username secret password global configuration mode command
5. Configure the vty lines - Enable the SSH protocol on the vty lines using the transport input ssh line configuration mode command. se the line vty global configuration mode command and then the login local line configuration mode command to require local authentication for SSH connections from the local username database.
6. Enable SSH version 2 - By default, SSH supports both versions 1 and 2. When supporting both versions, this is shown in the show ip ssh output as supporting version 1.99. Version 1 has known vulnerabilities. For this reason, it is recommended to enable only version 2. Enable SSH version using the ip ssh version 2 global configuration command.

  
