## Plaintext / unencrypted passwords
- Some applications store passwords "in the clear"
  - No encryption. You can read the stored password
- Do not store passwords as plaintext
  - Anyone with access to the password file or database has every credential
- What to do if your application saves passwords as plaintext
  - Get a better application
 
## Hashing a password
- Hashes represent data as a fixed-length string of text
  - A message digest, or "fingerprint"
- Will not have a collision
- One-way trip
  - Impossible to recover the original message from the digest
  - A common way to store passwords

## Spraying Attack
- Try to login with an incorrect password
- There are some common password lists
- Attack an account with the top three or more passwords
- If they dont work, move to the next account
- No lockouts, no alarms, no alerts


## Brute Force
- Try every possible password combination until the hash is matched
- This might take some time
  - A strong hashing algorithm slows things down
- Brute force attacks - Online
  - Keep trying the login process
  - Very slow
  - Most accounts will lockout after a number of failed attempts
- Brute force the hash - Offline
  - Obtain the list of users and hashes calculate a pasword hash, compare it to a stored hash
  - Large computional resource requirement
- 
