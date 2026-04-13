## Plaintext to Ciphertext
- The plaintext is passed through the encryption function along with a proper key; the encryption function returns a ciphertext. The encryption function is part of the cipher;
- A cipher is an algorithm to convert a plaintext into a ciphertext and vice versa.
- To recover the plaintext, we must pass the ciphertext along with the proper key via the decryption function, which would give us the original plaintext.
- Plaintext: the original, readable message or data before it’s encrypted
- Ciphertext: is the scrambled, unreadable version of the message after encryption. Ideally, we cannot get any information about the original plaintext except its approximate size.
- Cipher:  is an algorithm or method to convert plaintext into ciphertext and back again. A cipher is usually developed by a mathematician.
- Key: is a string of bits the cipher uses to encrypt or decrypt data. In general, the used cipher is public knowledge; however, the key must remain secret unless it is the public key in asymmetric encryption.
- Encryption:  is the process of converting plaintext into ciphertext using a cipher and a key. Unlike the key, the choice of the cipher is disclosed.
- Decryption:  is the reverse process of encryption, converting ciphertext back into plaintext using a cipher and a key. Although the cipher would be public knowledge, recovering the plaintext without knowledge of the key should be impossible (infeasible).

## Types of Encryption
### Symmetric Encryption
- Symmetric encryption, also known as symmetric cryptography, uses the same key to encrypt and decrypt the data.
- Keeping the key secret is a must; it is also called private key cryptography
- Examples of symmetric encryption are (Data Encryption Standard), 3DES (Triple) and (Advanced Encryption Standard).

### Asymmetric Encryption
- Asymmetric encryption uses a pair of keys, one to encrypt and the other to decrypt
- To protect confidentiality, asymmetric encryption or asymmetric cryptography encrypts the data using the public key; hence, it is also called public key cryptography.
- Examples are , Diffie-Hellman, and Elliptic Curve cryptography (). The two keys involved in the process are referred to as a public key and a private key. Data encrypted with the public key can be decrypted with the private key. Your private key needs to be kept private, hence the name.
- Asymmetric encryption tends to be slower, and many asymmetric encryption ciphers use larger keys than symmetric encryption.
- The building blocks of modern cryptography lie in mathematics. To demonstrate some basic algorithms, we will cover two mathematical operations that are used in various algorithms:
  - XOR Operation: hort for “exclusive OR”, is a logical operation in binary arithmetic that plays a crucial role in various computing and cryptographic applications. In binary, compares two bits and returns 1 if the bits are different and 0 if they are the same
  - Modulo Operation: commonly written as % or as mod. The modulo operator, X%Y, is the remainder when X is divided by Y. The remainder plays a significant role in cryptography.
