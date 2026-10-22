# Port Security

This is referring to physical ports on a switch, not logical ports.

Port security is a layer 2 (data link) security featured configured on a network switch. The goal of this is to restrict input to a physical switch port by limiting the MAC addresses of devices allowed to connect to the port.

Without this, an attacker could walk into a building and plug a malicious laptop into an open ethernet jack, gaining internal access.

## Learning Addresses

Switches need to learn what MAC addresses are authorized. This can be done in three ways:

- Static: Network administrators manually add the addresses.
- Dynamic: Switches learn on the fly. Resets if a switch is rebooted.
- Sticky MAC: The switch learns the MAC address when a device logs in, but information is saved into its running configuration. This persists after reboots.

## Port Security Violations (What happens on a breach?)

A violation occurs when an unauthorized MAC tries to access a protected port. It can react in three ways:

- Shutdown mode (The default and most secure): This instantly disables a physical port. It goes into `err-disable` (error disabled). The link light goes out too. The port remains dead until an administrator manually resets the interface.
- Protect mode: Silent blocking in a sense that it drops all network packets from the unauthorized device. It does not alert administrators, it just makes that device obselete.
- Restrict mode: The same as protect mode, but this one has a violation counter and also alerts administration.

## Advanced Attack Vector: MAC Flooding

MAC Flooding is a potential attack vector. Switches use an internal memory chart called **CAM (Content Addressable Memory)** for MAC addresses. It is limited in space. This creates a DoS like abilit *but* instead of service being denied, the switch becomes dumb and just broadcasts **all incoming data to every port**. Now, an outsider sniffing traffic to capture all traffic traveling through a building.

Enforcing a maximum MAC limit fixes this, like setting a max of 2 MAC addresses per physical port before shutdown. The port will shut down before the switch can be overloaded.

## Extra Information

**Disabling used ports** is the easiest security step to prevent MAC flooding.

**Looping** is possible where both ends of an ethernet cable can be plugged into the same switch, crashing the network. **STP (Spanning tree protocol)** helps prevent this.

### IEEE 802.1X

A simple but important concept, this is just port-based authentication. MAC addresses can be spoofed by hackers, bypassing security. IEEE 802.1X asks for authentication via credentials or a digital certificate before the switch port will grant them network access.
