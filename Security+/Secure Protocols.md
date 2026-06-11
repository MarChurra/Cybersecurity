## Unencrpyted network data
- Network traffic is important data
  - Everything must be protected
- Some protocols are not encrypted
  - All traffic sent in the clear, such as Telnet, FTP, SMTP, IMAP
- Verify with a packet capture
  - View everything sent over the network
 
## Protocol selection
- Use a secure application control
  - built-in encryption
- A secure protocol may not be available
  - This may be a deal-breaker
- Remote console? Use SSH instead of Telnet
- HTTPS instead of HTTP
- IMAPS instead of IMAP
- SFTP instead of FTP

## Port Selection
- Secure and insecure application connections may be available
  - It´s common to run secure and insecure traffic on different ports
- HTTPS and HTTP
  - HTTP: Port 80
  - HTTPS: Port 443
- The port number does not guarantee security
  - Confirm the sceurity features are enabled
  - Packet captures may be necessary
 
## Transport Method
- Dont rely on the application
  - Encrypt everything over the current network transport
- 802.11 Wireless
  - Open access point: No transporte-level encryption
  - WPA3: All user data is encrypted
- VPN
  - Create an encrypted tunnel
  - ALl traffic is encrypted and protected
  - Often requires a third-party client and service
  - 
