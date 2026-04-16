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

- salting refers to adding a salt, i.e., a random value, to the password before it is hashed.
- A Rainbow Table is a lookup table of hashes to plaintexts, so you can quickly find out what password a user had just from the hash. A rainbow table trades the time to crack a hash for hard disk space, but it takes time to create.
- Automated hash recognition tools such as hashID (opens in new tab) exist but are unreliable for many formats. For hashes that have a prefix, the tools are reliable. Use a healthy combination of context and tools.  If you find the hash in a web application database, it’s more likely to be than (NT LAN Manager). Automated hash recognition tools often get these hash types mixed up, highlighting the importance of learning yourself.

### Linux Passwords
- Password hashes are stored in /etc/shadow, which is normally only readable by root. They used to be stored in /etc/passwd, which was readable by everyone.
- The encrypted password field contains the hashed passphrase with four components: prefix (algorithm id), options (parameters), salt, and hash. It is saved in the format $prefix$options$salt$hash. The prefix makes it easy to recognise Unix and -style passwords; it specifies the hashing algorithm used to generate the hash.
- $y$: yescrypt is a scalable hashing scheme and is the default and recommended choice in new systems
- $gy$: gost-yescrypt uses the GOST R 34.11-2012 hash function and the yescrypt hashing method
- $7$: scrypt is a password-based key derivation function
- $2b$, $2y$, $2a$, $2x$: bcrypt is a hash based on the Blowfish block cipher originally developed for OpenBSD but supported on a recent version of FreeBSD, NetBSD, Solaris 10 and newer, and several Linux distributions
- $6$: sha512crypt is a hash based on SHA-2 with 512-bit output originally developed for GNU libc and commonly used on (older) systems
- $md5: SunMD5 is a hash based on the algorithm originally developed for Solaris
- $1$: md5crypt is a hash based on the MD5 algorithm originally developed for FreeBSD

### MS Windows Passwords
- Windows passwords are hashed using NTLM, a variant of MD4. They are visually identical to MD4 and MD5 Hashes (produces digests as output, reutrns a 128-bit string).
- Passwords are stored in the SAM Security Accounts Manager.
- Tools like mimikatz exist to circumvent MS windows security.
- The hashes found there are split into NT and LM hashes.
