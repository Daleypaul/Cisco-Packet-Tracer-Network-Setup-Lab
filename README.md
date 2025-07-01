# Cisco-Packet-Tracer-Network-Setup-Lab

# SCCM Lab: Targeted Software Deployment Using Device Collections


<h2>Description</h2>
In this lab, I created a functional network topology using Cisco Packet Tracer. The design included a mix of static and dynamically assigned IP addresses, DHCP and DNS services, web servers, and routing/switching infrastructure. This hands-on activity helped demonstrate my understanding of basic network design, device configuration, and end-to-end connectivity testing.


<h2>Languages and Utilities Used</h2>

- <b>2 Dynamic PCs</b>
- <b>1 Static PC</b>
- <b>1 DHCP Server</b>
- <b>1 DNS Server</b>
- <b>2 Web Servers</b>
- <b>1 Switch (Cisco 2960)</b>
- <b>1 Router (Cisco 2811)</b> 


<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>


<img src="IIMG_2560.png" height="80%" width="80%" alt="Finished project  "/>
<br />
<br />
  <b>I opened Cisco Packet Tracer and selected the Logical Workspace to begin designing the network.

Step 1: Launching Cisco Packet Tracer: <br/>
I opened Cisco Packet Tracer and selected the Logical Workspace to begin designing the network.
<br />
<br />
Step 2: Launching Cisco Packet Tracer
I opened Cisco Packet Tracer and selected the Logical Workspace to begin designing the network.
<br />

<br />
Step 3: Adding Devices
Using the bottom device menu:

PCs: I dragged three PC-PT devices into the workspace and labeled them Dynamic1, Dynamic2, and Static.

Servers: I added four Server-PT devices and renamed them:

DHCP Server

DNS Server

Web Server (www.etsmail.com)

Web Server (www.test.edu)

Switch: I added a 2960 switch.

Router: I added a 2811 router.
<br />
<br />

Step 4: Connecting Devices with Cables
Using the Connections (lightning bolt icon) tool:

PCs to Switch: I used Copper Straight-Through Cables to connect each PC’s FastEthernet0 to the switch (ports Fa0/1, Fa0/2, etc.).

Switch to Router: I connected the switch to the router’s FastEthernet0/0 using another straight-through cable.

Router to Servers: I connected each server to the router using appropriate ports and cables based on my design.
<br />
<br />

Step 5: Configuring the PCs
Dynamic PCs (Dynamic1 & Dynamic2):

Accessed Desktop > IP Configuration

Selected DHCP so they could automatically receive an IP address from the DHCP Server.

Static PC:

Accessed Desktop > IP Configuration

Manually entered:

IP Address: 192.168.1.10

Subnet Mask: 255.255.255.0

Default Gateway: Router interface IP (e.g., 192.168.1.1)

<br />
<br />

Step 6: Configuring the DHCP Server
On the DHCP Server:

Navigated to Config > DHCP

Created a pool:

Pool Name: Pool1

Default Gateway: Router IP (e.g., 192.168.1.1)

DNS Server: DNS Server IP (e.g., 192.168.1.2)

Start IP Address: 192.168.1.100

Subnet Mask: 255.255.255.0

Clicked Add to enable the pool.

<br />
<br />

Step 7: Configuring the DNS Server
On the DNS Server:

Navigated to Config > DNS

Added entries:

www.etsmail.com → IP address of Web Server 1

www.test.edu → IP address of Web Server 2

<br />
<br />

Step 8: Configuring the Web Servers
For both web servers:

Navigated to Config > Services > HTTP and ensured HTTP was ON

Set their IP addresses in Config > FastEthernet according to the network plan

<br />
<br />
Step 9: Configuring the Router Interfaces
On the Router:

Navigated to Config > FastEthernet0/0 and any other necessary interfaces

Assigned IP addresses matching the network plan

Enabled each interface by turning Port Status to ON

<br />
<br />

Step 10: Testing Connectivity
I used the Command Prompt on each PC to run various tests:

Ping the DHCP Server to confirm dynamic IP assignment was successful

Ping the DNS Server to verify DNS resolution

Ping both Web Servers by name (e.g., ping www.etsmail.com) to confirm that DNS and routing were properly configured
<br />
<br />

Conclusion:
This lab demonstrated the end-to-end setup of a small network environment including client devices, essential servers, and networking infrastructure. I successfully configured DHCP and DNS services, tested dynamic and static IP addressing, and confirmed connectivity through ping and domain resolution. This experience reinforced my practical skills in network planning, device configuration, and troubleshooting using Cisco Packet Tracer.



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
