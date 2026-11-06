# Securing Wireless and Mobile Devices

Wireless and mobile devices are typically harder to secure than wired because wireless is not stopped by boundaries like walls; anyone can interfere. The device can also leave the building, meaning the safety of this device is based on the holder and their circumstances.

## Wireless Site Surveys

A site survey maps out a wireless environment before and after a network is built. Heat maps are typically used for this. Tools channel through an area to find access points and how frequencies / channels are used.

This is not a one time thing and should be updated as neighbors add access points, office furniture gets rearranged, so on so forth.

## Wirelesss Survey Tools

Most operating systems have built-in tools to show nearby networks and signal strengths, but third party tools can go further and build heat maps and full reports. Spectrum analyzer's are a huge one because they detect raw radio frequencies themselves.

## MDM (Mobile Device Management)

MDM is a central system that lets an organization manage every mobile device from one app, whether the company or the user owns it. Policies can be universally applied, apps can be blocked, etc. These can work with an entire device or just specific parts of it.

## Deployment Models

There exists three main deployment models when it comes to organizational devices:

- BYOD (Bring your own device) means employee brings their own personal phone for work. The device has to meet company requirements and is usually the hardest to secure because the scale of what the user could do becomes questionable.
- COPE (Company owned, personally enabled) means the company buys a device and keeps full control of it, although the user can use it for personal things too like a personal email.
- CYOD (Choose your own device) means that the employee can choose the device from a preset approved list, although it'll still end up like COPE. This is COPE with a choice.

## Cellular Networks

Cell phones get their name from how the network works. The land is divided into cells, each cell covered by an antenna using certain frequences. As a phone moves, it is handed from cell to cell. The security concerns follow the visibility / reach / distance between cells. Traffic can be monitored because a network always knows which cell you are connected to.

## Wi-Fi

When a mobile device joins Wi-Fi, it inherits the same risks as any other device. Anyone on a network could grab traffic over the air, so encryption becomes essential. Similarly, attackers can perform an on-path / MITM attack by sitting between you and your network. DOS exists too.

## Bluetooth

Bluetooth is high-speed communication over short distances. It creates a PAN (Personal Area Network), the small bubble of devices around one person. This allows phones to connect to headphones, car systems, speakers, etc. This is also how tethering is applied (sharing your phone's internet with another device).

The short range means not everyone can easily attack it, but it still is discoverable when turned on. This makes standard security practices ideal: Turn it off and make it undiscoverable when not in use, and beware what you connect to.
