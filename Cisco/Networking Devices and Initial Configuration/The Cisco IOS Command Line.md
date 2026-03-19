### The Cisco IOS CLI
- The Cisco IOS command line interface (CLI) is a text-based program that enables entering and executing Cisco IOS commands to configure, monitor, and maintain Cisco devices.
- The Cisco CLI can be used with either in-band or out-of-band management tasks.
- Technicians familiar with the IOS commands and operation of the CLI find it easy to monitor and configure a variety of different networking devices because the same basic commands are used for configuring a switch and a router.

### Primary Command Modes
- All network devices require an OS and that they can be configured using the CLI or a GUI.
- Using the CLI may provide the network administrator with more precise control and flexibility than using the GUI.
- As a security feature, the Cisco IOS software separates management access into the following two command modes:
  - User EXEC Mode - This mode has limited capabilities but is useful for basic operations. It allows only a limited number of basic monitoring commands but does not allow the execution of any commands that might change the configuration of the device. The user EXEC mode is identified by the CLI prompt that ends with the > symbol.
  - Privileged EXEC Mode - To execute configuration commands, a network administrator must access privileged EXEC mode. Higher configuration modes, like global configuration mode, can only be reached from privileged EXEC mode. The privileged EXEC mode can be identified by the prompt ending with the # symbol.

## The Command Structure

### Basic IOS Command Structure
- A Cisco IOS device supports many commands. Each IOS command has a specific format, or syntax, and can only be executed in the appropriate mode
- Keyword - This is a specific parameter defined in the operating system (in the figure, ip protocols).
- Argument - This is not predefined; it is a value or variable defined by the user (in the figure, 192.168.10.5).

### IOS Command Syntax
- A command might require one or more arguments. To determine the keywords and arguments required for a command, refer to the command syntax. The syntax provides the pattern, or format, that must be used when entering a command.

### Common Commands
- show running-config
- show interfaces
- show ip interface
- show arp
- show ip route
- show protocols
- show version 
