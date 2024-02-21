# BACnet-Segmentation
This GitHub site provides an educational guide related to BACnet Segmentation for the February 2024 IT/OT Summit.

Modules related to aspects of BACnet Segmentation. Points to cover. Order of importance.

Each module will be about ten minutes in duration. They will be cycled through during each session with a half hour Q&A session.

Note this is a public website. Please do not place proprietary information.

All trademarks are property of the holders. Endorsement by ASHRAE or any other standards organization is not implied.
Endorsement by Siemens or Cimetrics is not implied.


* Preparation
* BACnet Network Segmentation   :      Physically separate Ethernet.  Connecting BACnet/IP, BACnet/SC, MSTP
* BACnet Application Level Firewall   :   Rules by packet type. Monitoring. Read only.
* Unit Management    : Status, statistics, management, backup, self-security, and maintenance

* BACnet Packet Capture  : Wireshark agency. SC decryption. Analysis tools and tips.
* VPN Access to Private network : OpenVPN service and clients.
* IT Community Practices   :    DHCP, DNS, NTP, Syslog, VPN, VLAN, Security, IPv6, Server Certs
* BACnet System Monitoring   :   Discovery. Topology. History. Events.
* BACnet Certificate Management   :    SC. Onboarding. Signing. Bootstrapping. CA. Hubs. Devices.      SC certs vs public webserver certs. 
<!---
KC: The device and system capabilities for description: 
1. BACnet network segmentation : 
Physically separate Ethernet.  
Connecting BACnet/IP, BACnet/SC, MSTP

2. BACnet Firewall :
Application layer routing is an intrinsic firewwall in and of itself.
Monitoring Error, Abort, Reject traffic.
Monitoring Device Management traffic.
Blocking Unauthorized Time Sync.
Read-only access into BACnet/SC.
BACnet/SC Hub with NPO diagnostics.

3. System monitoring (BACnet and syslog) :
Device discovery and connection monitoring.
Network discovery and topology.
Device history - firmware updates, database updates, identity change, address change.
Firewall Issues.
Auditable Events - eg. GSA.

4. BACnet/SC certificate management with Cimetrics Appliance and ABT.
5. Remote Packet Capture (including SC decryption).
6. VPN access to private Ethernet.
7. IT friendly features.

KC---------Slides and diagram and/or handout  one for each module - Talk and walk through -------
1. Segmentation.
 Just what it means. Layered and zones. Can be on same write but generally means separating interfaces. Number of interfaces is generally two or more. Same or different. 
Protocol. Ip address. Port. Url within the above. For example because pure sc is all the way to URL, it can coexist with bip or Ethernet pure because it is segmented. Segmentation can also allow different extensions to be separated. Like poe or multi drop or... Show with SbC3200 B3075 SbC3100.

2. Appliance/BNSD firewall like 3200 (or whichever has best firewall)
3. Appliance system monitoring. 
4. Onboarding Appliance and others with SC certificates.  Signing requests. CA. Bootstrapping... etc Distinguish between SC certs and public webserver certs.
5. Wireshark and quick packet analysis.  Wireshark capture of ip and sc. What to do with sc keys. Escrow and proxy. Really handing out the keys to other trust. Make it a player in secret domain.
6. Openvpn. Community client. Ovpn file loads in client. Server hands out .ovpn. Show in UI of products.
7.  Sc ip ports urls. Ipv6. Certificates and keys. Syslog. NTP. DNS. DHCP. BBMD. Radius. VPN again.
-->
