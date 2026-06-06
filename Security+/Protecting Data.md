## Geographic Restrictions
- Network Location
  - Identify based on IP subnet
  - Can be difficult with mobile devices
- Geolocation - determine a users location
  - GPS - mobile devices, very accurate
  - 802.11 wireless, less accurate
  - IP address, not very accurate
- Geofencing
  - Automatically allow or restrict access when the user is within a particular location
  - Dont allows this app to run, when you are outisde of a location

## Protecting Data
- A primary Job Task
  - An organization is out of business without data
- Data is everywhere
  - On a storage drive, on the network, in a CPU
- Protecting the data
  - Encryption, security policies
- Data permissions
  - Not everyone has the same data

## Encryption
- Encode information into unreadable data, from plaintext to ciphertext
- This is a two-way street
  - Convert between one and the other
  - If you have the proper key
 
## hashing
- Represents data as a short string of text
  - A message digest, or a fingerprint
- One-way trip
  - Impossible to recover the original emssage from the digest
  - Used to store passwords / confidentiality
- verify a download document is the same as the original
  - Integrity
- Can be a digital signature
  - Authentication, non-repudiation, and integrity
- Hopefully there are no collisions between two different inputs

## Obfuscation
- Obsfucate
  - Make something difficult to understand
- Take readable code and turn it into nonse
  - The developer keeps the readable code
  - both sets of code perform exactly the same way
- Heps prevent the search for security holes
  - Makes it more difficult to figure out what is happening

## Masking
- A type of obfuscation
  - Hide some fot he original data
- Protects PII and other sensitive data
- Many different techniques
  - Substituting, shuffling, encrypting, masking out
 
## Tokenization
- Replace sensitive data with a non-senstiive placeholder
- Common with credit card processing
  - Use a temporary token during payment
  - An attacker capturing the card numbers cant use them later
- It is not encryption or hasuing
  - The original data and token are not related
  - No encryption overhead
 
## Segmentation
- Many organizsations use a single data source
  - One large database
- One breach puts all of the data at risk
- Separate the data, and store it in different locations
- Sensitive data should have stornger security

## Permission Restrictiopns
- Control access to an account
- The authentication process
  - Password policies
  - Authentcation factor policies
  - Other considerations
- Permissions after login
  - Another line of defense
  - Prevent unauthorized access
