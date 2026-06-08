## Securing a Wireless Network
- An organization´s wireless network can contain confidential info
- Authenticate the users before granting access
  - Who gets access to the the wireless network?
  - Username, password, MFAº
- Ensure that all communication is confidential
  - Encrypt the wireless data
- Verify the integrity of all communication
  - The received data should be identicical to the orignal data
  - A message integrity check MIC is done

## The WPA2 PSK problem
- WPA2 has a PSK brute-force problem
- Listen to the four-way handshake
  - Some methods can derive the PSK hash without the handshake
- Capture the hash
- With the hash, cattackers can brute force the pre-shared key
- This has become easier as technologies improves
  - A weak PSK is easier to brute force
  - GPU processing speeds
  - Cloud-based password cracking
- Once you have the PSK, you have everyone´s wireless key, ther eis no forward secrecy

## WPA3 and GCMP
- Wifi Protected Access 3 WPA3
- GCMP block cipher mode
- Galois Counter Mode Protocol
- A stronger encryption than WPA2
- GCMP security services
  - Data confidentiality with AES
  - Message Integrity Check MIC with Galois Message Authentication Code GMAC
 
## SAE
- WPA3 changes the PSK authentication process
- Includes mutual authentication
- Creates a shared session key, witout sending that key across the network
- No more four-way handshakes, no hashes, no brute force attacks
- Uses a SAE Simultaneous Authentication of Equals
  - A Diffie-Hellman derived key exchange with an authentication component
  - veryone uses a different session key, even with the same PSK
  - An IEEE standard - the dragonly handshake
 
## Wireless authentication methods
- Gain a access to a wireless network
  - Mobile users
  - Temporary access
- Credentials
  - Shared password / pre-shared key PSK
  - Centralized Authentication 802.1X
- Configuration
  - Part of the wireless network connection
  - Prompted during th econnection process

## Wireless Security Modes
- Configure the authentication on your AP or wireless Router
- Open System
  - No authentication password is required
- WPA3-Personal / WPA3-PSK
  - WPA2 or WPA 3 with a pre-shared key
  - Everyone uses the same 256-bit key
- WPA 3 Enterprise / WPA3-802.1X
  - Authenticates users with an authentication server, such as rADIUS

## AAA framework
- Identification
- Authentication 
- Authorization
- Accountability

## Gaining Access
- RADIUS Remote Authentication Dial-in User Service
- One of the more common AAA protocls
  - Supported on a wide variety of platforms and devices
  - Not just for dial-in
- Centralize authentication for users
- RADIUS services are available on almost any server OS

## IEEE 802.1X
- Port-based Network Access Control NAC
- You dont get to access to the network until you authenticate
- Used in conjuction with an access Database
  - RADIUS, LDAP, TACACS+

## EAP
- Extensible Authentication protocol.
  - An authentication framework
- Many different ways to authenticate based on RFCS standards
  - Manufacturers can build their own EAP methods
- EAP integates with 802.1X
  - Prevent access to the network until the authentication succeeds

## IEEE 802.1X and EAP
- Supplicant- the client
- Authenticator - The device that provides access
- Authencation servers - Validates the client credentials
- 
