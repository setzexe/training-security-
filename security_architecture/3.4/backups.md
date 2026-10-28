# Backups

Backups, as the name implies, are means of recovery. They can recover important data in case of disaster. **These are essential**. Things go wrong and backups could be the only way of recovery.

There is a lot to consider with backups. You have different amounts of data you might for different things. Backups can come in different types (physical like hard drives, online via snapshots, etc). Where would you store this? How would you securely backup a server if a server is under attack? A lot to consider.

## Onsite vs. Offsite Backups

Onsite backups do not require an internet link and are usually much more immediate and cost efficient then offsite backups. You may have a physical server ready to put in at any point.

Offsite might not be readily available as you would need to access this over a WAN (wide area network). Data restoration could be available from everywhere but it is not as easy as restoring things then and there.

Organizations usually use both. More copies = more proper backups. More options as well for different attacks.

## Frequency

This is extremely important. If you backup data once every year and a system goes under, you will have to use data from a backup from nearly a year back. This alone could have extreme security risks, but also just mess over the data flow.

Backup frequency is important to consider. How often should I update my backups given my budget or ability? Some systems will need this more than others. This would also require a lot of planning, as alot of media would be managed.

In IT, this relates to **Recovery Point Objective**. It's how much data you can afford to lose due to a backup. If your backups are daily and a failure happened 22 hours ago, you only lost 22 hours of data. Can the business handle this? Or is this completely fine?

## Encryption

Backups typically hold extremely valuable information. This can be controlled via encryption. Do not assume that backups would never be reached; they very much might. So instead, have it so no one could see it unless they are properly authorized. This is especially useful with the cloud.

## Snapshots

Snapshots are a very efficient means for backups on a cloud server / virtual machines. It can save the exact configuration and data of the cloud's state, which could then later be restored. This is very efficient and can be done with one mouse click.

## Replication

This is a method of backup that replicates / copies real time data from one location to another or multiple others. This is always available in some shape or form as a copy that could be stored locally or remotely to all users. This makes it easy to access and recover by internal staff. It is very handy for immediate unforeseen disasters.

## Journaling

It is possible in cases that applying a backup could be screwed over due to power being cut out during the backup process. The data that would be applied after the power cut would be corrupt. In this stage, recovery would become complicated. You can not use that corrupted data on a real system, and it needs to be removed accordingly.

A way to help with this is journaling. This is like a 3rd party that assists in the backup process: A journal entry is created for a backup. Data is written into this journal. The end system would not be affected in the process because it is only writing into the journal. If power were to go off, the system only affects the journal. The system, on reboot, it can just look back at the initial journal entry and continue from there.

## Recovery Testing

Recovery testing tests the disaster recovery plan and ensures that a system would actually recover properly in case of diaster. Some organizations test their backups regularly. A simulated disaster, systems used as tests, etc.
