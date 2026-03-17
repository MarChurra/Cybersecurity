## File System
- The file system used i modern version of Windows is the eNew Technology File System NTFS 
- Before there was FAT16 and FAT32 File Allocation Table and HPFS High Performance File System
- FAT partitions are still used today, such as in USB devices, MicroSD cards.
- NTFS is known as a journaling file system.
- In case of a failure, the file systme can automatically repair the folders/file on disk using information stored in a log file. Not possible with FAT.
- Supports files larger than 4GB, whcih fat couldn´t
- Sets specific permissions on folders and files
- Folder and file compression
- Encryption EFS File System

## Permissions
- Full control
- Modify
- Read & Execute
- List folder contents
- Read
- Write

- Another feature of NTS is ADS Alternate Data Streams.
- Its a file attribute specific to Windows NTFS.

- Every file has at least one data stream $DATA, and ADS allows files to contain more than one stream of data.
- Natively Window Explorer (opens in new tab) doesn't display ADS to the user. There are 3rd party executables that can be used to view this data, (opens in new tab) also gives you the ability to view ADS for files
- From a security perspective, malware writers have used ADS to hide data.
- Not all its uses are malicious. For example, when you download a file from the Internet, there are identifiers written to ADS to identify that the file was downloaded from the Internet.

## Windows\ System32 Folders
- The Windows folder ( C:\Windows ) is traditionally known as the folder which contains the Windows operating system.
- This is where environment variables, more specifically system environment variables, come into play.  Even though not discussed yet, the system  environment variable for the Windows directory is %windir% .
- Environment variables store information about the operating system environment. This information includes details such as the operating system path, the number of processors used by the operating system, and the location of temporary folders
- System 32 folder holds the important files that are critical for the opearting system
- You should proceed with extreme caution when interacting with this folder. Accidentally deleting any files or folders within System32 can render the Windows inoperational
- 
