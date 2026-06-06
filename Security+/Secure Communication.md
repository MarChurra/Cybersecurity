## VPNs
- Virtual Private Networks
  - Encrypted (private) data traversing a public network
- Concentrator
  - Encrpytion / decryption access device
  - Often integrated into a firewall
- Many deployment options
  - Specialized cryptographic hardware
  - Software-based options available
- Used with client software
  - Sometimes built into the OS

## Encrypted Tunnel
- Keep data private across the public internet
- Encrypt youir data
  - Via new headers and trailers
- The originalm information is encapsulated with:
  - New IP Header
  - IPSec Headers
  - IPSec Trailers

  ## SSL/TLS VPN (Secure Sockets Layer VPN)
  - Uses common SSL TLS protocol. (tcp/443)
  - NO big VPN clients
    - usually remote access communication
  - Authenticate Users
    - No requirement for digitail certificates or shared passwords like IPSEC
  - Can be run fro a browser for a usually light VPN client
 
## SSL/TLS VPN
- On-demand access from a remote device
  - Software connects to a VPN concentrator
- Some software can be configured as always-on

## Site-to-site IPsec VPN
- Always on
- Firewalls often act as VPN concentrators

## SD-WAN
- Software Defined Networking in a Wide Area Network
  - A WAN built for the cloud
- The data center used to be in one place
- Cloud-based applications communicate directly to the cloud, instead of a central point

## Secure Access Service Edge SASE
- Update secure access for cloud services
  - Securely connect from different locations
- Secure Access Service Edge SASE
  - A nex generation VPN
- Security TEchnologies are in the cloud
  - Located close to the existing cloud services
- SASE clients on all devices

## Selection of effective controls
- Many different security options
  - Selecting rthe right choice can be challenging
- VPN
  - SSL/TLS VPN for user access
  - IPsec tunnels for site-to-site access
- SD-WAN
  - Manage the network connectivity to the cloud
  - Does not adequately address security concerns
- SASE
  - A complete network and security solution
  - Requires planning and implementation
