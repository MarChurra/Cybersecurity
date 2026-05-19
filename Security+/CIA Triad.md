- Combination of principles
  - The fundamentals of security
  - SOmetimes referenced as the AIC Triad
 
## Confidentiality
- Pretenves disclosure of information to unauthorized individuals or systems
  - Encryption
  - Access Controls
  - MFA Two Factor Authentication 

## Intengrity
- Maintains the integrity of the information
  - Data is stored and transferred as intended
  - Hashing
  - Digital Signatures
  - Certificates
  - Non-repuudiation 
  
## Availability
- Maintains the information available
  - Redundancy (Build services that will always be available)
  - Fault Tolerance (System will continue run, even in an failture)
  - Patching
 

## Non-Repudiation
- Includes a signature, that proves your identity and that you are the author of the data

## Proof of Integrity
- Verify data has not changed in transit
- In cryptography, a hash is used.
- If the data changes, the hash changes
- Does not match data with an individual, only verifies it did not change

## Proof of Origin
- Proves the message was not changed (Integrity)
- Prove the source of the message (Authentication)
- Make sure the signature inst fake (Non-repudiation)
- Sign with the private key
- Verify with the public key
