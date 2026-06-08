- Incredibly Important
  - Recover important and valuable data
  - Plan for Disaster
- Many different implementationsº
  - Total amount of data
  - Type of backup
  - Backup media
  - Storage Location
  - Backup and recovery software
  - Day of the week

## Onsite vs. offsite backups
- On site backups
  - No Internet Link required
  - Data is immediately available
  - Generally less expensive than off site
- Off site backups
  - Transfer data over Internet or WAN link
  - Data is avaialble after a disaster
  - Restoration can be performed from anywahere
- Organizations often use both
  - More copies of the data
  - More options when restoring

## Frenquency
- How often do we backup?
- This may be different between systems
  - Some systems may not change much each day
- May have multiple backup sets
  - Daily, weekly, and monthly
- This requires significant planning
  - Multiple backup sets across different days
  - Lots of media to manager
 
## Encryption
- A history of data is on backup media, with some that can be offsite
- This makes it very easy for an attacker
  - All of the data is in one place
- Protect backup data using encryption
  - Everything on the backup media is unreadable
  - The recovery key is required  to restore the data
 
## Snapshots
- Became popular on VM and Cloud environments
- Take a snapshot, making an instant backup of an entire system
  - Save the current configuration and data
  - Take another snapshot after 24 hours
  - Copntains only the changes between snapshots
  - Easier to use. Revert to any snapshot and makes recovery quick.

## Recovery Testing
- It is not enough to perform the backup
  - You have to be able to restore it
- Disaster Recovery Testing
  - Simulate a disaster situation
  - Restore from the backup
- Confirm the restoration
  - Test the restored application and data
- Perform periodic audits
  - Always have a good backup
  - Implement routine checks

## replication
- An ongoing, almost real-time backup
  - Keep data synchronized in multiple locations
- Data is available
  - there is always a copy somewhere
- Data can be stored locally to all users
  - Replicate data to all remote sites
- Data is recoerable
  - Disasters can happen at any time

## Journaling
- Power goes out while data to storage
  - The stored data is probably corrupted
- Recovery could be complicated
  - Remove corrupted files, restore from backup
- Before writing to storage, make a joural entry
  - After the hournal is written, write the data to storage
- After the data is written to the storage, update the journal
  - Clear the entry and get ready for the next use.  
