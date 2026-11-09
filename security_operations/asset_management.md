# Asset Management

Asset management covers the lifecycle of everything an organization owns. From how a thing is bought, to how it is eventually destroyed when retired. You can not protect what you do not know you have. Security problems can show up at every stage (a laptop nobody tracked could be compromised).

## Aquisition and Procedurement

Procedurement is the proper purchasing process, the steps an organization follows to acquire goods. It normally starts with the request from a user along with budget list and approval criteria. Next comes negotiating with supppliers. Finally comes purchasing, with the invoice and payment process.

## Assignment and Accounting

Once an asset arrives, its entered to a central asset tracking system that different parts of an organization share. Two key ideas apply here.

- Ownership means linking a specific person to a specific asset. This is who is responsible for that asset.
- Classification means labeling what type of asset it is.

## Monitoring and Asset Tracking

The organization needs to keep inventory of EVERY asset. Obvious ones like desktops but also smaller things like cables. Inventory can be taken deeper by also tracking information like what software is installed on a machine.

**Enumeration** means listing every part that makes up an asset, like CPU, keyboard, etc. That way if a component was swapped out / missing, it would be noticed.

Physical assets typical get an asset tag, which is a visible tracking / identification code like an RFID. The tag ties the physical device to its record in the inventory system as a simple methods of ownership checking.

## Media Sanitization

When a system is retired, the data needs to be COMPLETELY removed. The use case decides how. You might want to wipe a hard drive but keep it usable, while maybe completely destroying another SSD. Either way, sanitization is one-way for the data.

In case physical destruction is needed:

- Shredders / pulveriziers grind the device into pieces.
- Drills and hammers do similar physical damage.
- Degaussing is using a strong electromagnet to wipe out magnetic fields on a drive, wiping out the data and making them unusable typically. Breaking Bad famously did this.
- Incineration just burns the media.

## Certificate of Destruction

Most organizations do not own these toools, so destruction is usually done by a third party service; albiet this creates a trust problem since they have your data. Certificates of destruction's help establish trust. These are official documents confirming exactly what was destroyed and how.

## Data Retention

Knowing what to keep (if necessary) is an essential thing to know. How long would this data need to be kept for, and where would you put it? This covers backups, giving the data a planned lifecycle.

Retention is driven by two things:

- Legal and regulatory compliances. Some industries require you to keep certain data like an email for years.
- Operational needs, like being able to recover from a disaster.
