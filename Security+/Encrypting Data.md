- Protect data on storage devices
  - Data at rest
- Full-disk and partition/volume encryption
  - Bitlocker, FileVault (MAC), etc.
- File Encryption
  - EFS Encrpyting File System, third-party utilities

## Database encryption
- Protecting stored data
  - And the transmission of that data
- Transparent Encryption
  - Encrypt all database information with a symmetric key
- Record-Level encryption
  - Encrypt individual columns
  - Use separate symmetric keys for each column
 
## Transport Encryption
- Protect data traversing the network
- Encrypting in the application
  - Browser can communicate using HTTPS
- VPN
  - Encrypts all data transmitted over the network, regardless of the application
- Client-based VPN using SSL/TLS
- Site-to-site VPN using IPsec

## Encryption Algorithms
- Both sides need to use the same algorith
- There are many different algorithms
- Both sides decide on the algorithmm before encrypting the data
- There are advantages and disadvantages between algorithms
  - Security Level, speed, complexity of implementation, etc.

## Encryption Algorithm Comparison
- DES Encryption Algorithm
  - 64-bit plain text -> Initial Permutation -> Divide into Left and RIght Plaintext -> both 16 rounds -> Final Permutation -> 64-bit ciphertext
- AES Encryption Algorithm
  - 128 bits OR 192 bits or 256 bits Plain text and Secret Key -> Cipher -> Ciphertext of 128 bits, 192 bits, 256 bits

## Cryptographic Keys
- There is very little that inst known about the cryptographic process
  - Usually a known entity
  - The only thing you do not know is the key
- The key determines the output
  - Encrypted Data
  - Hash Value
  - Digital Signature

## Key Lengths
- Larger keys tend to be more secure
  - PRevent Brute force attacks
- Symmetric Encryption
  - 128-bit or larger symmetric keys are commonº
  - These numbers get larger and larger as time goes on
- Asymmetric Encryption
  - Complex calculation of prime numbers
  - Larger keys than symmetric
  - Comoo to see key of 3.072 bits or larger
 
  ## Key Stretching
  - Make a weak key stronger by performing multiple processes
    - Hash a password. Has the hash of the password, and so on.
  - Brute force attacks would require reversing each of those hashes
 
