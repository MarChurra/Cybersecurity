## RSA
- A public key encryption algorithm that enables secure data transmission over insecure channel.
- it uses a public and a private key.
- It relies on the mathematical problem of factorising very large prime numbers, into their original parts.
- The public key is known to all correspondents and is used for encryption, while the private key is protected and used for decryption,

## Diffie-Hellman Key Exchange 
- Key exchange aims to establish a shared secret between two parties. It is a method that allows two parties to establish a shared secret over an insecure communication channel without requiring a pre-existing shared secret and without an observer being able to get this key.
- Consequently, this shared key can be used for symmetric encryption in subsequent communications.
- We need to make some assumptions. Firstly, whenever we combine secrets, they’re practically impossible to separate.
- Secondly, the order in which they’re combined doesn’t matter
- Alice and Bob will combine their secrets with the common material to form AC and BC
- They will then send these to each other and combine the received part with their secret to create two identical keys, both ABC. Now, they can use this key to communicate.
- Diffie-Hellman Key Exchange is often used alongside RSA public key cryptography.
- Diffie-Hellman is used for key agreement, while RSA is used for digital signatures, key transport, and authentication, among many others.
- For instance, helps prove the identity of the person you’re talking to via digital signing, as you can confirm based on their public key. This would prevent someone from attacking the connection with a man-in-the-middle attack against Alice by pretending to be Bob.
- In brief, Diffie-Hellman and are incorporated into many security protocols and standards to provide a comprehensive security solution.

## SSH
- The SSH client confirms whether we recognise the server’s public key fingerprint, whioch is the public-key.
- This warning is because a man-in-the-middle attack is probable; a malicious server might have intercepted the connection and replied, pretending to be the target server.
- At some point, one will surely hit a machine with configured with key authentication instead. This authentication uses public and private keys to prove the client is a valid and authorised user on the server. By default, keys are RSA keys. You can choose which algorithm to generate and add a passphrase to encrypt the key.
- ssh-keygen is the program usually used to generate key pairs.
- Digital Signature Algorithm DSA - A public key cryptography algorithm specifically designed for digital signatures.
