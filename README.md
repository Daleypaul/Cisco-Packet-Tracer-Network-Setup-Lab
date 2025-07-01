# Cisco-Packet-Tracer-Network-Setup-Lab

# SCCM Lab: Targeted Software Deployment Using Device Collections


<h2>Description</h2>
Project consists of a simple PowerShell script that walks the user through "zeroing out" (wiping) any drives that are connected to the system. The utility allows you to select the target disk and choose the number of passes that are performed. The PowerShell script will configure a diskpart script file based on the user's selections and then launch Diskpart to perform the disk sanitization.
<br />


<h2>Languages and Utilities Used</h2>

- <b>SCCM</b> 


<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Identify the Target Device by Asset Tag: <br/>
<img src="IMG_3495.jpg" height="80%" width="80%" alt="Identifying Target Device "/>
<br />
<br />
  <b>Start by launching the Microsoft Endpoint Configuration Manager (SCCM) console and navigating to the Devices node:

Go to the Assets and Compliance section on the left panel.

Click on Devices.

In the search bar at the top, input the asset tag or partial computer name of the user’s device.

Once the machine appears, note the asset tag (example: CMRI-LT70776618) for reference and to ensure you’re targeting the correct device.</b> 
Add Device to an Existing Device Collectionk:  <br/>
<img src="IMG_3496.jpg" height="80%" width="80%" alt="Adding devices"/>
<br />
<br />
<b>After confirming the correct device:

Right-click on the device name.

Hover over “Add Selected Items” in the context menu.

Click “Add Selected Items to Existing Device Collection.”



This action allows you to group the device with others targeted for the same software deployment policy./b> 
Choose the Target Collection (New York Desktop Collection): <br/>
<img src="IMG_3497.jpg" height="80%" width="80%" alt="NY Desk Collection"/>
<br />
<br />
 <b>Next, the system will prompt you to choose from a list of existing collections:

Scroll through the list and select “New York Desktop Collection” (or whichever location-based group is appropriate).

Click OK or Next to finalize adding the machine.



Once the machine is in the collection, any deployment policies tied to that collection — such as software pushes — will apply to this device.

</b>
 Wait for the Software Deployment on the Device :  <br/>
<img src="IMG_3498.jpg" height="80%" width="80%" alt="Software Deployment"/>
<br />
<br />
 <b>Now that the machine is part of the target collection:

The device will receive the updated policy from SCCM.

On the user’s machine, open Software Center (type “Software Center” in the Start menu).

Go to the Applications tab and wait for the newly pushed application to appear.

Once visible, the app can be installed either automatically or manually, depending on the deployment settings.</b> 


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
