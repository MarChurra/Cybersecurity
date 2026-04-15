- A hash value is a fixed-size string or characters that is computed by a hash function. A hash function takes an input of an arbitrary size and returns an output of fixed length, i.e., a hash value.

## Hash Functions
- Hash functions are different from encryption. There is no key, and it’s meant to be impossible (or computationally impractical) to go from the output back to the input.
- A hash function takes some input data of any size and creates a summary or digest of that data. The output has a fixed size
- It´s hard to predict the output for any input and vice versa.
- Good hashing algorithms will be relatively fast to compute and prohibitively slow to reverse
- Any slight change in the input data, even a single bit, should cause a significant change in the output.
- The output of a hash function is typically raw bytes, which are then encoded.
- Common encodings are base64 or hexadecimal
- Hashing helps protect data’s integrity and ensure password confidentiality.
- When you login to a website, the server uses hashing to verify your password. A server records the hash values of a password, and not the password itself.
- Whenever you want to log in, it will calculate the hash value of the password you submitted with the recorded hash value.

## Hash Collision
- A hash collision is when two different inputs give the same output. Hash functions are designed to avoid collisions as best as possible.
- Hash functions are designed to prevent an attacker from being able to create, i.e., engineer, a collision intentionally. 
- However, because the number of inputs is practically unlimited and the number of possible outputs is limited, this leads to a pigeonhole effect.
- The pigeonhole effect states that the number of items (pigeons) is more than the number of containers (pigeonholes). Some containers must hold more than one item.
- Collisions are unavoidable. However, a good hash function ensures that the probability of a collision is negligible.
- MD5 and SHA1 1 have been attacked and are now considered insecure due to the ability to engineer hash collisions.
