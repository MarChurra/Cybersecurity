## TPM Trusted Platform Module
- A specification for cryptographic functions
  - Cryptography hardware on a device
- Cryptographic Processor
  - Random number generator, key generators
- Persistent Memory
  - Unique keys burned in during manufacturing
- Versatile Memory
  - Storage Keys, hardware configuration information
  - Securely store Bitlocker Keys
- Password Protected
  - No dictionary attacks
 
## Hardware Security Module HSM
- Used in large environments
  - CLusters , redundant power
  - Securely store thousands of cryptographic keys
- High-end Cryptographic hardware
  - Plug-in card or separete hardware device
- Key Backup
  - Secure storage in hardware
- Cryptographic accelerators
  - Offload that CPU overhead from other devices
 
## Key Management System
- Services are everywhere
  - On-premises, cloud-based
  - Many different keys for many different services
- Manage all keys from a centralized manager
  - Often provided as a 3rd party software
  - Separate the encryption keys from the data
- All key amnagement from one console
  - Create keys for a specific vendor or cloud provider (SLL/TLS, SSH(
  - Associate keys with specific users
  - ROtate keys on a regular interval
  - Log key uses
- ManageEngine Key Manager PLus, as an example

## Keeping Data Private
- Our data is located in many different places
  - Phones, cloud, laptops
  - The most private data is often physically closest to us
- Attackers are always finding new techniques
  - A race to stay one step ahead
- Our data is changing constantly
  - How do we keep this data protected

## Secure Enclave
- A protected area for our secrets
  - Often implemented as a hardware processor
  - Isolated from the main processor
  - Many different technologies and names
- Provides extensive security Features
  - has its own boot ROM
  - Monitors the system boot process
  - True random number generator
  - Real-time memory encryption
  - Root cryptographic keys
  - Perform AES encryption in hardware
