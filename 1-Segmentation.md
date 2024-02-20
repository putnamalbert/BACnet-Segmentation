# Segmentation

Layered and zones. Segmentation can be done logically on the same physical port but generally means separating interfaces. 

Number of interfaces is generally two or more. Same or different: Protocol. IP address. Port. Url within the above. 

Because pure BACnet/SC is all the way to URL, SC can coexist with BACnet/IP or BACnet Ethernet (layer 2) because it is segmented. 

Segmentation can also allow different physical or logical extensions to be separated. Like PoE or multi drop or others.

## BACnet Network Segmentation Devices (BACnet routers) BNSD:
B3075, SbC3200, SbC3100

### BNSD solve the following integration problems:

When IT is unwilling to provide all the IP addresses required for a project.

When the Integrator wants to control the assignment of IP addresses of the BACnet/IP devices.

Increasingly strict IT requirements: IT may not want certain BACnet/IP devices connected to the IT-managed network (for example, devices that don’t support DHCP).

IT may not allow Ethernet ring networks (daisy chained and ring devices) to connect directly to IT-managed network switches.

IT departments do not allow UL864 switches to connect directly to the IT networks.

Integrators are starting to design and deploy Secured BACnet/SC networks. At these sites, they need a solution that can easily segment and filter the unsecure BACnet/IP and BACnet/SC networks from the secure BACnet/SC network.

### SC Certificate Domains

Situations will arise of certificate scenario mismatch. Segmentation will eventually become a mater of matching security domains. Cimetrics will provide a BACnet/SC to BACnet/SC BNSD to bridge this gap.
 
