# Wireless Security Settings

Every wireless device is basically a radio transmitter and receiver, so anyone within a range can listen. This means a secure wireless network typically relies on three things:

- Authenticating users at all time with a username and password or MFA.
- Keep data confidential by encrypting everything sent over the air.
- Protect integrity so the data is the same across devices. This is done with **MIC** (Message Integrity Check).

## Wireless Encryption

The basic solution to eavesdropping is encryption. All authorized users get a key that allows anyone on this network to send or understand traffic. There exists WPA2 and WPA3. WPA stands for Wi-Fi Protected Area.

## The Problem With WPA2

WPA has been the standard since 2004, encrypting with AES with a mode called CCMP. Under this was a weakness that would lead to its successor, WPA3. Most home or small office networks use WPA2 with a PSK (pre shared key), the Wi-Fi password everyone shares. A device connects via a four way handshake that an attacker could sniff nearby. Although they can only get the hash of the PSK, algorithms exist that can let them brute force the real password. Once they have this, they now have the same decryption key as everyone else with no other security means.

## WPA3 and GCMP

WPA3 was introduced in 2018 and fixes those problems with stronger encryption using frameworks called GCMP and GMAC, as opposed to WPA2's CCMP.

The bigger change is how WPA3 handles shared passwords. The four way handshake is replaced with **SAE (Simultaneous Authentication of Equals)**, or the dragonfly handshake. It uses Diffle-Hellman's key exchange with authentication added into it. Both sides prove they know the password and build a shared session key without ever sending this specific key across the network. Each user gets their own sesssion key that an attacker can't sniff out.

## Wireless Security Modes

When you set up an access point, you pick how people authenticate. There are three main options:

- Open system means no password and anyone can connect. Common for guest / public Wi-Fi.
- WPA3-Personal is typically for homes or smaller offices and follow the PSK formula.
- WPA3-Enterprise / WPA-802.1X authenticates each user against a central authorization server using a protocol named RADIUS. You log in with your own credentials and not a shared password.

## The AAA Framework

Enterprise authentication is built on the triple A framework:

- Authentication is proving that you are a certain person, usually with a password.
- Authorization decides what you can do once you are identified.
- Accounting records what you did: login time, data sent and received, and logout time.

## RADIUS

RADIUS (Remote Authentication Dial-In User Service) is one of the most common AAA protocols. It is used to centralize authentication for nearly everything like routers, switches, firewalls, etc. Almost every server OS can run RADIUS. The point is that user credentials can be checked in one place.

## IEEE 802.1X

802.1X is port-based Network Access Control (NAC). The rule here is simple: You do not get network access until you authenticate. This works with a backend authenticator like RADIUS. IEEE 802.1X handles three roles:

- Supplicant: The client device trying to connect.
- Authenticator: The device (like a switch) that controls access.
- Authentication server: What actually checks your credentials, like RADIUS.

## EAP

EAP (Extensible Authentication Protocol) is the framework that carries the authentication conversation inside 802.1X. It is not one simple method. It is a structue that lots of methods plug into. Manufacturers can make their own. This just ensures the network stays closed during 802.1X until authentication is granted.
