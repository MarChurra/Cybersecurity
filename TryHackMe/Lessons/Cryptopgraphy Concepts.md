## Cryptography
- It secures information in traffic by using mathematical rules and secret keys to scramble information into gibberish, that only authorised people can unscramble.

### Symmetric Encryption
- Plaintext - A message you can read normally.
- Ciphertext - A scrambled version that is not supossed to make sense.
- Key - The secret ingredient that controls how scrambling and unscrambling works.
- Algorithm - The public recipe, the set of steps that explain how to use the key on the message.
- The sane jey encrypts and decrypts the message.
- Both sender and receiver need a copy of that key.
- The key has to stay secret.
- It´s a fast and efficient encryption.
- It has an issue which is the key distribution problem, how the key is sent over the internet.

### Caesar Ciphes: Algorithm Plus Key
- Shifts each letter in your message, by a fixed number of positions in the alphabet. That fix is the key.

### Sharing Keys Safely: Asymmetric Encryption
- Uses two mathematically linked keys, instead of one.
  - A private key that only one person keeps secret
  - A public key that anyone can known and use
- If something is encrypted with someones public key, only their private key can decrypt it.
- If you encrpyt something with your private key, anyone with your public key can decrypt it (primarily used for digital signatures).
- The two keys are connected by some serious maths, but it would take an ordinary computer a large time to recover the private key from the public key.
- A message is encrypted with a public key and a private key.
- The receiver receives the public key.
- The message is encrypted using that public key.
- The sender decrypts it using his private key.
- The most common use for this encryption is HTTPS

### HTTPS
- THe website sends back its public key wrapped ina  certificate.
- Your browser and the website use asymmetric encryption to agree on a shared secret, a symmetric key. Without anyone else being able to see it.
- From there on, they switch to fast symmetric encryption, using that shared secret for the rest of the session.
- This can be called a hybrid approach:
 - Assymetric encryption - Solves the problem of key distribution
 - Symmetric Encryption - Handles the heavy lifting because its way faster.

 - To make sure the public key really belongs to someone, certificates are used to confirm the identity of the person.
 - A certificate is a digital document that contains someons public key.
 - States who that key belongs to.
 - A trustued authority digitally signs it, called a CA Certificate Authority.
 - Your browser and operating system comes preloaded with a list of trusted CAs.
 - When a wbesite hands over a certificate, your broswer checks that a trusted CA signed it, if it still valid, and then it shows the padlock and trusts the public key.
 - If not, the browser displays a warning and may refuse to connect.
 - Encryption usually done with SHA-256
