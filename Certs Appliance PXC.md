# Certificates
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

--------------------------------------------------------------


Create Issuer Certificate for a Network NNN using the Appliance as a Certificate Authority

1. Select "Certificate Management" in the "hamburger menu"
2. Locate and expand the "Local" branch in the tree on the left panel
3. Try to locate the "Network NNN" branch as a direct child of the "Local" branch
4. In case of there is no "Network NNN" branch, do following:
    - Select the "Local" branch in the tree
    - Open the "gear menu" and select "Create Network"
    - In the pop-up enter desired network number into corresponding field
    - Click on the "Save" button
    - Go to step #3
5. Expand the "Network NNN" branch in the tree
6. Try to locate the "Issuer Certificate ..." branch as a direct child of the "Network NNN" branch
7. In case of there is more than one "Issuer Certificate ..." branches, locate the closest (from below) to the "Network NNN" one
8. In case of there is no "Issuer Certificate ..." branch, do following:
    - Select the "Network NNN" branch in the tree
    - Open the "gear menu" and select "Create Issuer Certificate"
    - In the pop-up make sure the "Appliance" is selected in the "Issuer Certificate Source" dropdown
    - In the pop-up click on the "Save" button
    - In the next pop-up click on the "Save" button
9. Select located "Issuer Certificate ..." branch and make sure the row right below the "gear menu" reads "Issuer Certificate Source:Appliance"
10. If not, return to step #8 and pretend there is no "Issuer Certificate ..." branch
11. You are all set
----------------------------------------------------------
Create and download Operational Certificate for a Device YYYY in network NNN, that could not create a CSR (i.e. 3100, 3200)

1. Select "Certificate Management" in the "hamburger menu"
2. Locate and expand the "Local" branch in the tree on the left panel
3. Try to locate the "Network NNN" branch as a direct child of the "Local" branch
4. In case of there is no "Network NNN" branch, go to "Create Issuer Certificate for a Network NNN" and execute all steps
5. Expand the "Network NNN" branch in the tree
6. Try to locate the "Issuer Certificate ..." branch as a direct child of the "Network NNN" branch
7. In case of there is no "Issuer Certificate ..." branch, go to "Create Issuer Certificate for a Network NNN" and execute all steps
8. In case of there are more than one "Issuer Certificate ..." branches, locate the closest (from below) to the "Network NNN" one
9. Select located "Issuer Certificate ..." branch and make sure the row right below the "gear menu" reads "Issuer Certificate Source:Appliance"
10. If not, go to "Create Issuer Certificate for a Network NNN" and execute all steps
11. Expand located "Issuer Certificate ..." branch
12. Try to locate the "Device YYYY" branch as a direct child of the "Issuer Certificate ..." branch you just expanded
13. If there is no "Device YYYY" branch, do following:
    - Select the "Issuer Certificate ..." branch you just expanded
    - Open the "gear menu" and select "Create Device"
    - In the pop-up select "Appliance Generated" in the "Operational Key Source" dropdown
    - Then enter desired device instance number into corresponding field
    - Click on the "Save" button
14. If the "Device YYYY" branch is grayed and looks sick, do following:
    - Select the "Device YYYY" branch
    - Open the "gear menu" and select "Change Operational Key Source"
    - Make sure the "Appliance Generated" is selected in the "Operational Key Source" dropdown
    - If not, select "Appliance Generated" and click on the "Save" button
    - Open the "gear menu" and select "Create Operational Key and Certificate"
    - In the pop-up click on the "Save" button
15. If the "Device YYYY" branch is not grayed and looks healthy, do following:
    - Select the "Device YYYY" branch
    - Make sure the row right below the "gear menu" reads "Operational Certificate Source:Appliance Generated"
    - If not, open the "gear menu" and select "Retire" and in the pop-up click on the "OK" button, then go to step #14
16. Select the "Device YYYY" branch
17. Open the "gear menu" and select "Download Certificates"
18. Save somewhere the ZIP archive (the name will be something like "devYYYY_netNNN_certs_yyyy-mm-dd_hh_ss_mm.zip")
19. Go to that somewhere and unpack the downloaded file
20. There will be 4 files you can use:
    - devYYYY_netNNN_cert_yyyy-mm-dd_hh_ss_mm.crt - operational SC certificate
    - devYYYY_netNNN_pkey_yyyy-mm-dd_hh_ss_mm.key - corresponding private key
    - net1111_issuingcert_yyyy-mm-dd_hh_ss_mm.crt - issuing certificate
    - devYYYY_netNNN_cert_yyyy-mm-dd_hh_ss_mm.pfx - all three files above in one PFX container
--------------------------------------------------------------------------------------
Create and download Operational Certificate for a Device YYYY in network NNN, that could create a CSR (i.e. the Appliance Device, Siemens Device)

1. Go to device configuration and download its CSR
2. Come back to the Appliance Web setup
3. Select "Certificate Management" in the "hamburger menu"
4. Locate and expand the "Local" branch in the tree on the left panel
5. Try to locate the "Network NNN" branch as a direct child of the "Local" branch
6. In case of there is no "Network NNN" branch, go to "Create Issuer Certificate for a Network NNN" and execute all steps
7. Expand the "Network NNN" branch in the tree
8. Try to locate the "Issuer Certificate ..." branch as a direct child of the "Network NNN" branch
9. In case of there is no "Issuer Certificate ..." branch, go to "Create Issuer Certificate for a Network NNN" and execute all steps
10. In case of there are more than one "Issuer Certificate ..." branches, locate the closest (from below) to the "Network NNN" one
11. Select located "Issuer Certificate ..." branch and make sure the row right below the "gear menu" reads "Issuer Certificate Source:Appliance"
12. If not, go to "Create Issuer Certificate for a Network NNN" and execute all steps
13. Expand located "Issuer Certificate ..." branch
14. Try to locate the "Device YYYY" branch as a direct child of the "Issuer Certificate ..." branch you just expanded
15. If there is no "Device YYYY" branch, do following:
    - Select the "Issuer Certificate ..." branch you just expanded
    - Open the "gear menu" and select "Create Device"
    - In the pop-up select "Device CSR" in the "Operational Key Source" dropdown
    - Then enter desired device instance number into corresponding field
    - Click on the "Save" button
16. If the "Device YYYY" branch is grayed and looks sick, do following:
    - Select the "Device YYYY" branch
    - Open the "gear menu" and select "Change Operational Key Source"
    - Make sure the "Device CSR" is selected in the "Operational Key Source" dropdown
    - If not, select "Device CSR" and click on the "Save" button
    - Open the "gear menu" and select "Upload CSR"
17. If the "Device YYYY" branch is not grayed and looks healthy, but not too healthy, do following:
    - Select the "Device YYYY" branch
    - Open the "gear menu" and select "Create Operational Certificate"
    - In the pop-up click on the "Save" button
18. If the "Device YYYY" branch is not grayed and looks healthy, do following:
    - Select the "Device YYYY" branch
    - Make sure the row right below the "gear menu" reads "Operational Certificate Source:Device CSR"
    - If not, open the "gear menu" and select "Retire" and in the pop-up click on the "OK" button, then go to step #16
19. Select the "Device YYYY" branch
20. Open the "gear menu" and select "Download Certificates"
21. Save somewhere the ZIP archive (the name will be something like "devYYYY_netNNN_certs_yyyy-mm-dd_hh_ss_mm.zip")
22. Go to that somewhere and unpack the downloaded file
23. There will be 3 files you can use:
    - devYYYY_netNNN_cert_yyyy-mm-dd_hh_ss_mm.crt - operational SC certificate
    - net1111_issuingcert_yyyy-mm-dd_hh_ss_mm.crt - issuing certificate
    - devYYYY_netNNN_cert_yyyy-mm-dd_hh_ss_mm.pfx - both files above in one PFX container
24. Go to device configuration and upload files that device will expect and accept
----------------------------------------------------------------------------
Installing an Operational Certificate for the Appliance Device

1. Select "Settings" in the "hamburger menu"
2. Select "BACnet Port" in the menu on the left
3. Open the "gear menu" and select "Issue New Key and CSR"
4. In the pop-up click on the "Save" button
5. Open the "gear menu" and select "Download CSR"
6. Bring downloaded CSR to the Certificate Authority and ask to sign it (or use the Appliance as a CA)
7. Come back to the Appliance Web setup
8. Select "Settings" in the "hamburger menu"
9. Select "BACnet Port" in the menu on the left
10. Open the "gear menu" and select "Upload New Certificate"
11. If you have a PFX file that contains both operational and issuing certificates, select that file
12. If you have two separate files (one for operational certificate and another for issuing certificate), do following:
    - Select operational certificate file here for uploading
    - Open the "gear menu" and select any of "Upload New Issung Certificate"
    - Select issuing certificate file here for uploading
13. Locate the "Apply Change and Reboot" button somewhere down this page and click on it
-------------------------------------------------------------------------------------
Create Issuer Certificate for Network NNN using external Certificate Authority

1. Select "Certificate Management" in the "hamburger menu"
2. Locate and expand the "Local" branch in the tree on the left panel
3. Try to locate the "Network NNN" branch as a direct child of the "Local" branch
4. In case of there is no "Network NNN" branch, do following:
    - Select the "Local" branch in the tree
    - Open the "gear menu" and select "Create Network"
    - In the pop-up enter desired network number into corresponding field
    - Click on the "Save" button
    - Go to step #3
5. Expand the "Network NNN" branch in the tree
6. Try to locate the "Issuer Certificate ..." branch as a direct child of the "Network NNN" branch
7. In case of there is more than one "Issuer Certificate ..." branches, locate the closest (from below) to the "Network NNN" one
8. In case of there is no "Issuer Certificate ..." branch, do following:
    - Select the "Network NNN" branch in the tree
    - Open the "gear menu" and select "Create Issuer Certificate"
    - In the pop-up make sure the "External" is selected in the "Issuer Certificate Source" dropdown
    - In the pop-up click on the "Save" button
9. Select located "Issuer Certificate ..." branch and make sure the row right below the "gear menu" reads "Issuer Certificate Source:External"
10. If not, return to step #8 and pretend there is no "Issuer Certificate ..." branch
11. You are all set
-----------------------------------------------------------------------------------
Create Operational Certificate for a Device YYYY in network NNN that could not create a CSR (i.e. 3100, 3200) using external Certificate Authority (i.e. Siemens tool)

1. Select "Certificate Management" in the "hamburger menu"
2. Locate and expand the "Local" branch in the tree on the left panel
3. Try to locate the "Network NNN" branch as a direct child of the "Local" branch
4. In case of there is no "Network NNN" branch, go to "Create Issuer Certificate for Network NNN using external Certificate Authority" and execute all steps
5. Expand the "Network NNN" branch in the tree
6. Try to locate the "Issuer Certificate ..." branch as a direct child of the "Network NNN" branch
7. In case of there is no "Issuer Certificate ..." branch, go to "Create Issuer Certificate for Network NNN using external Certificate Authority" and execute all steps
8. In case of there are more than one "Issuer Certificate ..." branches, locate the closest (from below) to the "Network NNN" one
9. Select located "Issuer Certificate ..." branch and make sure the row right below the "gear menu" reads "Issuer Certificate Source:External"
10. If not, go to "Create Issuer Certificate for Network NNN using external Certificate Authority" and execute all steps
11. Expand located "Issuer Certificate ..." branch
12. Try to locate the "Device YYYY" branch as a direct child of the "Issuer Certificate ..." branch you just expanded
13. If there is no "Device YYYY" branch, do following:
    - Select the "Issuer Certificate ..." branch you just expanded
    - Open the "gear menu" and select "Create Device"
    - In the pop-up select "Appliance Generated" in the "Operational Key Source" dropdown
    - Then enter desired device instance number into corresponding field
    - Click on the "Save" button
14. If the "Device YYYY" branch is grayed and looks sick, do following:
    - Select the "Device YYYY" branch
    - Open the "gear menu" and select "Change Operational Key Source"
    - Make sure the "Appliance Generated" is selected in the "Operational Key Source" dropdown
    - If not, select "Appliance Generated" and click on the "Save" button
    - Open the "gear menu" and select "Create Key and CSR"
    - In the pop-up click on the "Save" button
15. If the "Device YYYY" branch is not grayed and looks healthy, do following:
    - Select the "Device YYYY" branch
    - Make sure the row right below the "gear menu" reads "Operational Certificate Source:Appliance Generated"
    - If not, open the "gear menu" and select "Retire" and in the pop-up click on the "OK" button, then go to step #14
16. Select the "Device YYYY" branch
17. Open the "gear menu" and select "Download CSR"
18. Save somewhere the CSR file (the name will be something like "devYYYY_netNNN_csr_yyyy-mm-dd_hh_ss_mm.csr")
19. Bring downloaded CSR to the Certificate Authority and ask to sign it
20. Come back to the Appliance Web setup
21. Select "Certificate Management" in the "hamburger menu"
22. If CA issued one file with a "PFX" extension, containing both operational and issuing certificates, do folowing:
    - Locate and select the "Device YYYY" branch (steps #1-#12)
    - Open the "gear menu" and select "Upload Operational Certificate"
    - Select the PFX file from CA
22. If CA issued two separate files - one for operational certificate and another for issuing certificate, do folowing:
    - Locate and select the "Device YYYY" branch (steps #1-#12)
    - Open the "gear menu" and select "Upload Operational Certificate"
    - Select the operational certificate file from CA
    - Locate and select the Issuer Certificate ..." branch, which is a parent of the parent of the selected "Device YYYY" branch
    - Open the "gear menu" and select "Upload Certificate"
    - Select the issuer certificate file from CA
23. Locate and select the "Device YYYY" branch (steps #1-#12)
24. Open the "gear menu" and select "Download Certificates"
25. Save somewhere the ZIP archive (the name will be something like "devYYYY_netNNN_certs_yyyy-mm-dd_hh_ss_mm.zip")
26. Go to that somewhere and unpack the downloaded file
27. There will be 4 files you can use:
    - devYYYY_netNNN_cert_yyyy-mm-dd_hh_ss_mm.crt - operational SC certificate
    - devYYYY_netNNN_pkey_yyyy-mm-dd_hh_ss_mm.key - corresponding private key
    - net1111_issuingcert_yyyy-mm-dd_hh_ss_mm.crt - issuing certificate
    - devYYYY_netNNN_cert_yyyy-mm-dd_hh_ss_mm.pfx - all three files above in one PFX container
28. Go to device configuration and upload files that device will expect and accept
----------------------------------------------------------------------------------------
