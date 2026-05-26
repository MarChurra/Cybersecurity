## Open Permissions
- Very easy to leave a door open
  - The hacker will always find it
- Increasingly common with cloud storage
  - Statistical chance of finding an open permission

## Unsecured Admin Accounts
- The Linux Root Account
  - The Windows Admin or SuperUser account
- Can be a misconfiguration
  - Intentionally configuraring an easy-to-hack password
- Disable direct lgoin to the root account
  - Using the su or sudo option
- Protect accounts with root or administrator access

## Insecure Protocols
- Some protocols are not encrypted
  - All traffic sent in the clear
  - Telnet, FTP, SMTP, IMAP
- Use the encrypted versions
  - SSH, SFTP, IMAPS, etc.

## Default Settings
- Every app and network device has a default login
  - Change these credentials
- Mirai Botnet
  - Takes advantage of default configs
  - Takes over IoT devices
  - Cameras, routers, doorbells, garage door openers, etc.
  -  Has an open source version

## Open ports and services
- Services will open ports
  - It is important to manage access
- Often managed with a firewall
  - Managed traffic flows
  - Allow or deny based on port number or application
- Firewall rulesets can be complex
  - It is easy to make a mistake
- Always test and audit
