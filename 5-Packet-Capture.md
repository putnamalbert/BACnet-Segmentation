# Packet Capture and Analysis
Packet capture and analysis can be used to diagnose problems related to BACnet communication, including BACnet network segmentation.  The Wireshark application is often used for diagnosis, and it can also be used for packet capture.

## Packet Capture
Some Cimetrics BACnet Network Segmentation Devices (BNSD) include a BACnet packet capture agent that can be enabled by the device's administrator.  This packet capture agent produces Wireshark-compatible files. For Cimetrics products with multiple physical network ports, this packet capture agent will capture BACnet network traffice on all physical ports simultaneously and label each packet with the numerical ID of the port from which the packet was captured, typically 0 or 1 (see "frame.interface_id" in Wireshark).

Wireshark can be used to capture packets on a computer where Wireshark is installed.  This is most useful when the computer is actively communicating using BACnet.  If Wireshark is running on a computer that is not actively communicating using BACnet, it will most likely see only BACnet broadcast messages if the computer is connected to an Ethernet switch.  Port mirroring can be enabled on many Ethernet switches in order to enable packet capture of traffic received and sent by a device that cannot run Wireshark or another packet capture agent.

Some networks have a substantial amount of uninteresting network traffic, which can substantially increase the size of packet capture files.  The packet capture agent built into Cimetrics BNSDs block almost all non-BACnet/IP traffic.  When an application like Wireshark is used for packet capture, it may be possible to restrict the traffic that goes into the packet capture file.  An example of a Wireshark capture filter that would be useful for BACnet/IP networks would be "udp port 47808", which restricts the captured traffic to UDP datagrams on port 47808 (the default port for BACnet/IP).

## Network Traffic Analysis and Problem Diagnosis

