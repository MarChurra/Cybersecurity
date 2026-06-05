## Port Security
- We have created many authentication methods through the years
  - A network admin has many chocies
- Use a username and password
- Commonly used on wireless networks, and also wired networks

## EAP 
- Extensible Authentication Protocol
  - AN authentication framework
- Many different ways to authenticate based on RFC standards
  - Manufacturers can build their own EAP methods
- EAP integrates with 802.1X
  - Preventes access to the network until the authentication suceeds

## IEEE 802.1X
- Port-based Network Access Control NAC
  - You dont access to the network until you authenticate
- EAP integrates with 802.1X
  - Extensible Authentication Protocol
  - 802.1X preventes access to the network until authentication is done
- Used in conjuction with an authentication database
  - RADIUS, LDAP TACAS+, Kerberos, etc

## IEEE 802.1X and EAP
- Supplicant - the client
- Authenticator - The device that provides access
- Authentication server- Validates the client credentials 
