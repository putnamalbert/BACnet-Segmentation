## Appliance #1

IP address: 10.14.140.111
Device:     14100
Network:    1414


## Appliance #2

IP address: 10.14.150.111
Device:     14200
Network:    1415


## Appliance #3

IP address: 10.14.160.111
Device:     14300
Network:    1416

## Appliance #4

IP address: 10.14.170.111
Device:     14400
Network:    1417

All configured to use BACnet/SC, each one has its own HTTPS and SC certificates issued by itself.

You can use https://[IP address] or https://sbcappliance.local to access the user interface.
Do not use the https://sbcappliance.local if more than one appliances are online in the same phisical network (for obvious reason).

You can use your credentials from the test LAN at the Mill, if you forgot your password use admin/admin1 credentials.
You can just use it or you can reset your password using that admin account.

If the test device would ready (but it is not) and you have "default" firewall rules uploaded into the 3100 (which you do not have), the steps to use that device would look like:

1. Start the Cimetrics BACnet Explorer on the laptop connected to IP network
2. Select "Explore Everything"
3. Locate and select device 99099 in the local network
4. Expand the device
5. Locate a Multi State object 14101 with with name "Action write-property to 14100"
6. Write value 2 into Present Value of the Multi State object 14101
7. Open the Appliance interface and go to the "Issues"
8. A new issue should be created under the "Security" branch of the issues tree, the name of the issue will be like "unexpected confirmed traffic - sc network access"
9. Select that issue and take a look into the details there
