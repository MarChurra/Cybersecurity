## Password Complexity and Length
- Make your password strong
  - Resist guessing or brute-force attack
- INcrease password entropy
  - No single words, no obvious passwords
  - Mix upper and lower case leters, numbers, and special characters
- Stronger passwords are commonly at least 8 characters
  - These requirements change as processing speed gets faster
- Consider a phrase or set of words

## Password age and expiration
- Password age
- Password Expiration
  - Password works for a certain amount of time
  - 30, 60, 90 days,
  - After the expliration date, the password does not work
  - System remembers password history, requires unique password
- Critical systems might change more frequently

## Password Managers
- Important to use different passwords for each account
  - Remembering all of them would be impractical
- Store all of your passwords in a single database
  - Encrypted, protected
  - Can include multifactor tokens
- Built-in to many OS
  - And some browsers
- Enterprise password managers
  - Cenntralized management

## Passwordless Authentication
- Many breaches are due to poor password control
  - Weak passwords, insecure implementation
- Authenticate without a password
  - This solves many password management issues
- You may already be passwordless
  - Facial recognition, security key, etc.
- Passwordless may not be the primary authentication method

## Just in-time permissions
- In many organizations, the IT team is assigned admin/root elevated account rights
- Grant admin access for a limited time
  - No permanent administrator rights
  - The principle of least privilege
- A breached user account never has elevated rights
  - Narrow the scope of a breach
- Request access from a central clearinghouse
  - Grants or denies based on predefined security policies
- Password vaulting
  - Primary credentials are stored in a password vault
  - The vault controls who get access to credentials
- Accounts are temporray
  - Just in time process creates a time limited account
  - Administrator receives ephemeral credentials
  - Primary passwords are never released
  - Credentials are used for one session then deleted 
