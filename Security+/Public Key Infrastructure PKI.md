## PKI
- Policies, procedures, hardware, software, people
  - Digital certificates: create, distribute, manage, store, revoke
- This is a big, endeavor
- Also refers to the binding of public keys to people or devices
  - The certificate authority
  - All about trust
 
## Symmetric Encryption
- A single, shared key
  - Encrypt and decrypt with the same key
- Secret Key Algorithm
  - A shared secret
- Does not scale well and can be challenging to distribute
- Very fast to use
  - Less overhead than asymmetric encryption
  - Often combined with asymmetric encryption

## Assymetric Encryption
- Public Key Cryptography
  - Two or more mathematically related keys
- One is the Private Key
- And the other is the Public Key, accessible to al
- The private key is the only key that can decrypt data encrypted with the public key

## The Key Pair
- Asymmetric encryption
  - Public Key Cryptography
- Key Generation
  - Build botht he public and private key at the same time
  - Lots of randomization
  - Large prime numbers

## Key Escrow
- Someone else holds your decryption keys
  - Your private keys are in the hands of a 3rd-party
  - This may be within your own organization
- This can be a legitimate business arrangement
  - A business might need access to employee information
  - Government agencies may need to decrypt partner data
