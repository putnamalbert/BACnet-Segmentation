# Certificates for BACnet SC
## Decide
* Clarity: Operational Cerificates for BACnet SC.... not website or service certificates.
  
* Who is CA?:  Enterprise, MSI Vendor, Appliance
* How is each device to submit for certs?: CSR, Secrets to CSR proxy, Doppleganger creation (very bad, but sometimes needed)
* How are certs returned to device?: Packaging. Maybe in a zip of different packages?

## Act
Follow the actions and record such actions (to be repeated/updated later).\
Or... better yet... use the wizards.


## Mechanics
Steps that one would take to

Create an Issuer Certificate for the network.

Create keys and certificates for the SbC3200.

Create key and CSR in the Appliance and then create the certificates for the appliance.
Here is modified bullets list that covers following scenarios:

- Create Issuer Certificate for a Network using the Appliance as a Certificate Authority

- Create and download Operational Certificate for a Device that could not create a CSR (i.e. 3100, 3200)

- Create and download Operational Certificate for a Device that could create a CSR (i.e. the Appliance Device, Siemens Device)

- Installing an Operational Certificate into the Appliance Device

- Create Issuer Certificate for a Network using external Certificate Authority

- Create and download Operational Certificate for a Device that could not create a CSR (i.e. 3100, 3200) using external Certificate Authority (i.e. Siemens tool)

IMPORTANT: The "PFX" file is a container for certificates and private keys, and it may be protected with a password. Because we implemented working with PFX in the Appliance as a "quick patch", the Appliance can only work with PFX files with empty passwords. And all PFX files, the Appliance exports, have empty passwords. 

Some terms, used here:

 - "hamburger menu" - a menu on the right-top of the screen, under the blue circle with three horizontal white lines inside, content is always the same
   
 - "gear menu" - a menu on the left-top of the right panel, under the square blue rounded corners button with a white gear inside, content is always different but always your friend
 - "Expand ... branch" - means "click on a little-little triangle on the left of a branch name". If there is no little-little triangle, you are all set
 - "healthy" - bold roman font
 - "healthy but not too healthy" - normal roman font
 - "sick" - italic gray font
