# Packet Capture and Analysis
Packet capture and analysis can be used to diagnose problems related to BACnet network segmentation.  The Wireshark application is often used for diagnosis, and it can also be used for packet capture.

## Packet Capture
Some Cimetrics BACnet Network Segmentation Devices include a BACnet packet capture agent that can be enabled.  This packet capture agent produces Wireshark-compatible files. For Cimetrics products with multiple physical network ports, this packet capture agent will capture BACnet network traffice on all physical ports simultaneously and label each packet with the numerical ID of the port from which the packet was captured ("frame.interface_id" in Wireshark).

Wireshark can be used to capture packets on a computer where Wireshark is installed.  This is most useful when the computer is able to see interesting BACnet traffic, such as when the computer is functioning as a BAS workstation or server that is communicating using BACnet.  If Wireshark is running on a computer that is not actively communicating using BACnet, it will most likely see only BACnet broadcast messages if the computer is connected to an Ethernet switch.  Port mirroring can be set up on some Ethernet switches in order to enable packet capture for a device that cannot run Wireshark or another packet capture agent.

(Capture from all BACnet interfaces for all BACnet traffic (filtered for BACnet).)
