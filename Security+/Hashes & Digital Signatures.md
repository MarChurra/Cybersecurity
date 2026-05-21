## Hashes
- Present data as a short string of text
  - A message digest, a fingerprtint
- One-way trip
  - Impossible to recover the orignal message from the digest
  - Used to store passwords / confidentiality
- verify a downloaded document is the same as the original
  - Integrity
- Can be a digital signature
  - Authentication, non-repudiation, and integrity

## SHA256
- Produces 256 bits / 64 hexadecimal characters

## Collision
- Hash Functions
  - Take an input of any size
  - Create a fixed size string
  - Message digest, checksum
- The hash should be unique
  - Different inputs should never create the same hash
  - If they do, it is a collision
- MD5 has a collision problem

## Practical hashing
- Verify a downloaded file
- Hashes may be provided on the download site
- Compare the downloaded file hash with the posted hash value
- Password Storage
  - Instead of storing the password, store a salted hash
  - Compare hashes during the auth process
  - Nobdy ever knows your actual password

## SALT
- Random data added to a password when hashing
- Every user gets their own random salt, commonly stored with the password
- Rainbow tables wont work with salted hashes
- Its a precompiled table of hash values and their original input.
- This slows things down the brute force process

## Salting the hash
- Each user gets a different random hash

## Digital Signatures
- Prove the message was not changed
  - Integrity
- Proves the source of the message
  - Authentication
- Make sure the signature is not fake
  - Non-repudiation
- Sign with the private key
  - The message does not need to be encrypted
  - Nboody else can sign this
- Verify with the public kiey
  - Any change in the message will invalidate the signature
 
## Creating a digital signature
- Thye plaintext goes through a Hashing Algorithm to provide a Hash of Plaintext. This is then combined with a Private Key to create the Digital Signature.
- This then leads to Plaintext and Digital Signature 
