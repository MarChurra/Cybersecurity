- How to share an encryption key across an insecure medium without physically transferring the key
- Out-of-band key exchange
  - Dont send the symmetric key over the net
  - Telephone, courier, in-person, etc
- In-band key exchange
  - On the network
  - Protect the key with additional encryption
  - Use asymmetric encryption to deliver a symmetric key
 
  ## Real-time encryption/decryption
  - There is a need for fast security
    - Without compromising security
  - Share a symmetric session key using assymetric encryption
    - Client encrypts a random symmetric with a servers public key.
    - The server drecrypts this shared key and uses it to encrypt data
    - This is the session key
  - Implement session keys carefully
    - Needs to be change doften, with ephemeral keys
    - Need to be unpredictable
   
  ## Symmetric key from asymmetric keys
  - Use public and private key cryptography to create a symmetric key
  - The Private Key is combined with the Public Key of the destination. Thhis creates the Symmetric Keys.
  - This key will be the same as the sender public key and the destination private key.
