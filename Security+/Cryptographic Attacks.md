- Attackers can try to breaqk the safe (the cryptography), since they do not have access to the private keys
- Finding ways to undo the security
  - There are many potential cryptographic shortcomings
  - The problem is often the implementation, where the user element comes in

## Birthday Attack
- In a classroom of 23 students, what is the chance of two students sharing a birthuday
  - About 50%
  - For a class of 30, the chance is about 70%
- In the digital world, this is a hash collision
  - A hash collision is the same has value for two different plaintexts
  - Find a collision through brute force
- The attacker will generate multiple versions of plaintext to match the hashes
  - Protect yourself with a larger hash output size

## Collisions
- Hash digests are supposed to be unique
  - Different input data should not create the same hash
- MD5 hash
  - Message Digest Algorithm 5
  - Collisions identified in 1996, 4 years after being created
- December 2008: Reserachers created CA certificate that appeareed legititamete when MD5 is checked

## Downgrade Attack
- Instead of using perfectly good encryption, use something that´s not so great
  - Force the systems to downgrade their security
- SSL stripping
  - Combines an on-path attack with a downgrade attack
  - Difficult to implement, but big returns for the attacker
  - Attacker must sit in the middle of the conversation
  - Victims browser page inst encrypted
