# BACnet-Segmentation
Modules related to BACnet Segmentation
Points to cover. Order of importance.

* BACnet Network Segmentation - not a heading but the first point.... no heading.\
* BACnet Application Level Firewall
* BACnet System Monitoring
* BACnet Certificate Management
* BACnet Packet Capture
* VPN Access to private network
* Adheres to IT Best Practices

KC: The device and system capabilities for description: 

1. BACnet network segmentation : 
Physically separate Ethernet
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
Protocol. Ip address. Port. Url within the above. 
For example because pure sc is all the way to URL, it can coexist with bip or Ethernet pure because it is segmented. Segmentation can also allow different extensions to be separated. Like poe or multi drop or...
Show with SbC3200 B3075 SbC3100.

2. Appliance/BNSD firewall like 3200 (or whichever has best firewall)

3. Appliance system monitoring. 

4. Onboarding Appliance and others with SC certificates. 
Signing requests. CA. Bootstrapping... etc
Distinguish between SC certs and public webserver certs.

5. Wireshark and quick packet analysis. 
Wireshark capture of ip and sc. What to do with sc keys. Escrow and proxy. Really handing out the keys to other trust. Make it a player in secret domain.

6. Openvpn. Community client. Ovpn file loads in client. Server hands out .ovpn. Show in UI of products.

7.  Sc ip ports urls. Ipv6. Certificates and keys. Syslog. NTP. DNS. DHCP. BBMD. Radius. VPN again.
