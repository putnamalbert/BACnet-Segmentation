# Common Issues
## Segementation supports different "ways" in each network.
  However, internal support of that way is left largely to that segment.
  Examples: 
  * a BNSD is not a server for any of the following
  DHCP, DNS, NTP, Syslog server... the only exceptions we have are
  an OpenVPN supplicant and we are planning on changing to an agent.
  Webservers for configuration and access
* Support for different datalink variations are left to the segment.
  Examples: Power over Ethernet. Single Pair Ethernet and most pertinet Loop based
  Loop or daisy chain networks need their own switch to support that way of working with Ethernet.
