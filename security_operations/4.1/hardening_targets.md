# Hardening Targets

Hardening means making a system harder to attack by minimizing its attack surface, like the ports and services. The catch is the different devices harden differently. One should not guess or make assumptions based on other devices to harden a device. Organizations typically provide guides, like manufacturer guides, STIGs (Security Technical Implementation Guides), and CIS Benchmarks (Center of Internet Security).

## Mobile Devices

Phones and tablets are everywhere, connect to every network, and are easy to lose, making security essential. Hardening them starts with patching. Mobile vendors release updates often which should be installed quickly.

Segmentation is the ideal second piece. This keeps company data seperate from personal data on the same device. If someone's personal apps get compromised, the work-based information is seperate.

**MDM** (Mobile Device Management) lets an organization control an entire mobile device fleet centrally. IT can push policies, have screen locks, app control, etc.

## Workstations

User desktops and laptops are the most common way attackers get in because that is where people open and click attachments / links. The basics like an updated OS and patches come first.

Connecting workstations to an organizations central policy management ensures a workstation is following the same security policy. Finally, remove all unneccessary software. Each installed program is another chance of being attacked.

## Network Infrastructure Devices (switches, routers)

Switches and routers are purpose-built. They run a specific embedded OS and you usually do not get full access to its underlying machine. Hardening here moreso means configuring them correctly and keep firmware updated. Also, change default credentials. These devices often ship with well known, easily exploitable credentials like admin/password.

## Cloud Infrastructure

Cloud is not dealing with physical hardware, so you protect how people access and manage it. Cloud typically has a cloud management workstation that should be secured, as that acts as the root for a cloud server.

Least privilege should be applied to all cloud accounts. An over-privileged cloud user is one of the most common causes of cloud breaches. **EDR (Endpoint Detection and Response)** is essential as well to watch and respond to potential malicious activity.

Always have backups, and have them seperate from the cloud provider in case of emergency.

## Servers

Servers come in many forms, like Windows Server or Linux distros. They hold valuable data.

Hardening them typically covers four main areas:

- Installing OS updates and security patches regularly
- Enforce minimum password length and complexity. Limit what each user can do
- Allow only connections a server would actually need
- Monitor and protect

## SCADA (Supervisory Control and Data Acquisition) / ICS (Industrial Control Systems)

These refer to the computers that run physical infrastructure, like power plants or dams or logistics. These handle serious real world data and an attack on these would not only hurt the data, but real people in the process.

Segmentation is the primary hardening method. You want to ensure this critical data stays securely away from the outside or other accessible data.

## Embedded Systems

An embedded system is hardware and software that does one job, like a SMART washing machine. Their weakness is that they are nearly impossible to upgrade because they are exclusive to the manufacturer. This makes protecting the devices from the outside, like with your own network security, the main means of hardening.

## IoT Devices

Internet of things (IoT) devices cover anything that can connect to a network. This includes SMART lightbulbs, alarms, etc. It is important to note that typically, security might not be a priority for these manufacturers. These can ship with weak default credentials, unnecessary open services, etc.

IoT devices should be kept in their own VLAN because they might be so easy to acccess. Otherwise, changing the default passwords and applying updates when available are a must.
