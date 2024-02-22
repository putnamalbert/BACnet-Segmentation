# Common Issues
* Segementation supports different "ways" in each network.
  But the internal support of that way is left largely to that segment.
  Examples: a BNSD is not a server for any of the following
  DHCP, DNS, NTP, Syslog server... teh omly exceptiin we have is an OpenVPN supplicant and we are planning on changing to an agent.
