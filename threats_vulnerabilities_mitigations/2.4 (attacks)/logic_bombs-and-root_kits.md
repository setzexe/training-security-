# Logic Bombs

These are broad and can do any sort of damage, but these typically are just stored in some way on a computer and only goes off at a specific time, or at a specific user event. These are difficult to identify until they do damage because it is not something that looks out of the ordinary.

On March 19, 2013, South Korean organizations got a bank email that actually had a trojan with malware. It looked normal until 24 hours later, it had activated. It deleted the storage and master boot records for a lot of banking systems. No data was stolen, but they also lost their boot data. That data is not very easy to get back.

The main way to prevent this stuff is just monitoring and truly auditing what type of stuff your company gets. Emails, attachments, installations, etc. 

# Rootkit

This is malware that is very stealthy and works within the OS. These give the threat actors the privileges that a root user (the superuser, or admin) could get. These can be invisible to both the task manager **and** most antiviruses.

Apps and software do exist to remove these. If extensively looking out for malware, if you know how to look for other malware, you will have an easier chance of noticing rootkits. 