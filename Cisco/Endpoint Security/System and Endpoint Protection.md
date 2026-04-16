## Defending Systems and Devices
- Fileless Attacks: Piggyback from regular programs, and run scripts, leaving no traces. Harder to detect, but get remove upon computer shutdown.
- Patches and upgrades are often combined into a service pack.
- Updates can be security updates, critical updates and serivce packs.
- A patch management tool can be used to manage patches locally instead of using the vendors online update service.
- Local computers can instaed receive updates from a local, verified server.

- HIDS: Host Intrusion Detection System software is installed on a device or server to monitor suspicious activity. It stores logs locally and can affect system performance.
- HIPS: Host Intrusion Prevention System is a software that monitors a device for known attacks and anomalies If it detects malicious activity, the tool can send an alarm, log the malicious activity, reset the connection, and drop the packets.
- Endpoint Detection and Response: An integrated security solution that continuously monitors and collects data from an endpoint device.It then analyzes the data and responds to any threats it detects.
- DLP: Data Loss Prevention tools provide a centralized way to ensure that sensitive data is not lost, misused or accessed by unauthorized users.
- Next generation Firewall: A security device that combines a traditional firewall with the other network-device-filtering functions. For example, an application firewall using in-line deep packet inspection DPI or an IPS.

### Boot Integrity
- Ensures that the system can be trusted and has not been altereted while the OS loads.
- Firmware: software instructions about basic computer functions, stored on a small memory chip on the motherboard. The basic input/output BIOS is the first program that runs when you turn on the computer.
- UEFI runs in 64-bit mode.

### Secure boot
- A security standard to ensure that a device boots using trusted software. On boot, the firmware checks the signature of each piece of boot software, including UEFI firmware drivers, UEFI applications and the OS. If the signatures are valid, the system boots and the firmware gives control to the OS.

### Measured Boot
- Provides stronger validation than Secure Boot. It measures each component starting with the firmware through to the boot start drivers, and stores the measurements in the TCMP chip to create a log.
- The log can be tested remotely to verify the boot state of the client.
- It can identify untrusted applications trying to load, and it also allows antimalware to load earlier.

### Antivirus/Antimalware Software
- Can be:
  - Signature-Based: This approach recognizes various characetristics of known malware files
  - Heuristics-Based: This approach recognizes general features shared by various type of malware.
  - Behaviour-based: This approach employs analysis of suspicious behaviour
- 
