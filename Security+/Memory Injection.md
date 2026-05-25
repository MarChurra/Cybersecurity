## Finding Malware
- Malware runs in memory
  -  Memory forensics can find the malicious code
-  Memory contains running processes
  - DLLs (Dynamic Link Libraries)
  - Threads
  - Buffers
  - Memory Management functions
  - And much more
- Malware is hidden somewhere
  - Malware runs in its own process
  - Malware injects itself into a legitimate process

## Memory Injection
- Add code into the memory of an existing process
  - Hide malware inside of the process
- Get access to the data in that process
  - Have the same rights and permissions as the process it took over
  - Perform a privilege escalation

## DLL Injection
- A windows Library containing code Data
- many applications can use this library
- Attackers inject a path to a malicious DLL
  - Runs as part of the target process
- One of the most p+opular memory injection methods
