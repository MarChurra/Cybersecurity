## Operating System
- Coordinates everything happening on a computer.
- It sits between the user, applications and the system´s physical hardware, acting as the manager of the system.

## System Privilege Layers
- Kernel Space - THe privileged, locked-down core of the OS. This is where the kernel, the part of the opeating system that directly manages hardware and system resources, runs. It has unrestricted access to the CPU, storage and all hardware components.
- User Space - Where all standard applications run. Applications in the user space are deliberately prevented from acessing hardware directly. They must make a system call and request that the kernel acts on their behalf.

## Opearting System Duties
- Process Management - Creates, schedules, prioritizes and terminates running programs.
- Memory Management - Allocate RAM to processes and protects the app´s memory from other processes and reclaims memory when an app is closed. When RAM is low, the OS uses virtual memory to keep your system stable.
- File System Management - Organizes files and handles their metadata and permissions
- User Management - Handles multiople user accounts, authentication and permissions
- Device Management - Load drivers and provides a universal interface

## Operating System Security
- Authentication
- Permissions - Controls what each user and app is allowed to rwx
- Isolation - Keeps every process in its own protected box, kernel and user space separation.
- System Protection - Safeguards critical system files and settings from unauthorized changes

## OS Interfaces
- Divided between GUI Graphical User Interface and CLI Command-Line Interface
