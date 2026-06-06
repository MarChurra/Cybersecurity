## Data at Rest
- The data is on a storage device
  - Hard drive, SSD, flash drive, etc.
- Encrypt the data
  - Whole disk Encryption
  - Database encryption
  - File-or folder level-encryption
- Apply permissions
  - Access control lists
  - Only authorized users can access the data

## Data in transit
- Data transmitted over the network, or data-in motion
- Not much protection as it travels
- Use Network-based protection, such as Firewalls or an IPS
- Provide Transport Encryption
  - TLS
  - IPSEC

## Data in use
- Data actively processing in memory
  - RAM, CPU Register and cache
- The data is almost always decrypted
- The attackers can pick the decrypted information out of RAM

## Data Sovereignty
- Data that resides in a country is subject to the laws of that country
- Legal monitoring, court orders, etc.
- Laws may prohibit where data is stored
  - GDPR General Data Protection Regulation
  - Data collected on EU citizens must be stored in the EU
  - A complex mesh of technologies and legalities

## Geolocation
- Location details. Tracks within an localized area
- Many ways to determine location
  - 802.11, mobile providers, GPS
- Can be used to manage data access
  - Prevents access from other countries
- Limit administrative tasks unless a secure area is used
  - Permite enhanced access within a safe zone or space 
