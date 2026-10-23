# States of Data

This refers to data at different stages.

## Data at rest

This refers to data on a storage device like a hard drive or SSD. Even unencrypted, it is at rest. But encryption is important. Whole disk, database, etc.

Apply permissions accordingly. Who could access this data at rest? Keep this a consideration when making access control lists / ACLs.

## Data in transit / motion

Data that is transmitted over a network. Not much protection exists as it travels, so external security is necessary. Port switch security, firewalls, IPS, encryption like TLS or IPsec, etc.

Recap: TLS is more suited for applications, as the web easily supports it. IPsec is more ideal for large ranges of data and site-to-site.

## Data in Use

Data that is actively processing in memory (RAM, CPU registers, and cache).

The data is usually always decrypted because the data needs to be seen to be used; this creates a large security risk because attackers know that information is decrypted at this state.

The 2013 Target breach utilized this because credit cards were being processed on point-of-sale RAM.

## Data Sovereignty

This refers to how data that resides in a certain country is subject to the laws of that control. What might be legal in U.S.A might not be allowed in Singapore.

This also includes laws and regulations on how the data itself may be stored. This could vary from area to area. This could also mean that you could not move your data to another country if it does not follow the respective regulations.

### Geolocation

This refers to location details for someone or something. You can use this to create access controls or restrictions on data being accessed or users accessing data. Location can be found in a multitude of ways (802.11, mobile providers, GPS). This is important in situations where data follows different procedures from location to location.
