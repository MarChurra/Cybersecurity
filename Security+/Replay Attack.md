- Useful information is transmitted over the network
- Need access to the raw network data
  - Network TAP, ARP poisoning, Malware on the victim compuiter
- The gathered information may help the attacker
  - Replay the data to appear as someone else
- This is not an on-path attack
- Can be prevented with salting, for example, in the case of AUth Replay attacks

## Browser cookies and session IDs
- Cookies
  - Information stored on your computer by the browser
- Used for tracking, personalization, session mnanagement
  - Not executable, not generally a security risk
  - Unless someone gets access to them
- Could be considered a privacy risk
- SSession IDS are often stored in the cookie
  - Maintains essions across multiple browser sessions

## Session Hijacking (Sidejacking)
- An attacker rretrieves a Session ID, to establish connections with the Web Server, spoooking the victim connection

## Header Manipulation
- Information gathering
  - Wireshark, Kismet
- Exploits
  - XSS
- Modify Headers
  - tamper, Firesheep, Scapy
- Modify Cookies
  - Cookies Manager+

## Prevent Session Hijacking
- Fully encrypt from end-to-end
  - Unable to capture session ID
  - Additional load on the web server with HTTPS
  - Firefox Extension: HTTPS Everywhere, FOrce-TLS
- Encrypt end-to-somewhere
- At least avoid capture over a LAN
- Still-in-clear for the rest of the journey, after the VPN tunnel.
