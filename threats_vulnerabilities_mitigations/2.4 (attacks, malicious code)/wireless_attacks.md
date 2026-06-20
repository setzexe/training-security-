# Wireless Attacks

A very common attack on a wireless network is being connected, and then being disconnected for no reason. You may reconnect after a while, but it'll just be a loop of connecting and disconnecting. This is known as **Wireless Deauthentication**.

## 802.11 management frames

The main vulnerability associated with this are management frames with 802.11. These manage the connectivity from your device to WiFi, primarily through the access points. Unfortunately, older 802.11 models had management frames just be sent out in the open on a network, unencrypted.

IEEE has already addressed this; modern 802.11ac comes updated to prevent this. A lot of services involved with management frames (deauthentication, channel switches, etc) are now encrypted. This does not include everything within 802.11ac.

## Radio Frequency (RF) jamming

Denial of Service via Radio Frequency can happen and affect any device over this wireless frequency. This uses radio to force the users devices to hear radiowaves that they shouldn't, blocking communication with actual waves they might need, thus denying service.

This often is not intentional. Flourescent lights and microwaves have notable cause some effect with this.

## Wireless jamming

Similar concept but maybe not radio waves. Random data and bits at random times, just jamming the network and preventing people from seeing legitimate packets or data they might need.

These people must be local. If this attack is happening, the jamming signal is usually closeby. The term for finding is jammer is called a **foxhunt**.

