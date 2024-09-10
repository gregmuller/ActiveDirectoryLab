<h1>Active Directory Home Lab</h1>

In this lab we're going to walk through how to create a 1000+ user Active Directory home lab environment using Oracle VirtualBox. 

<h2>Languages/Utilities/Environments Used</h2>

- <b>Windows 10 Pro</b> 
- <b>Windows Server 2019</b>
- <b>Oracle VirtualBox</b>
- <b>Active Directory</b>
- <b>Powershell</b>

<h2>Program walk-through:</h2>

<p align="center">
<img src="https://i.imgur.com/gpohvC1.png" height="80%" width="80%"/>
<br />
<br />
Download Oracle VirtualBox: <br/>
<img src="https://i.imgur.com/rWXYC4p.png" height="80%" width="80%"/>
<br />
<br />
Download Windows 10 ISO:  <br/>
<img src="https://i.imgur.com/bOYGhPH.png" height="80%" width="80%"/>
<br />
<br />
Label Your Machine "DC" for "Domain Controller": <br/>
<img src="https://i.imgur.com/eLACBX6.png" height="80%" width="80%"/>
<br />
<br />
Change "Clipboard" and "Drag'n'Drop" to "Bidirectional" This will allow you to drag and drop files from your computer into the virtual machine:  <br/>
<img src="https://i.imgur.com/TdP8dLB.jpeg" height="80%" width="80%"/>
<br />
<br />
Create a NAT (Network Address Translation) in adapter 1. This will connect to your home internet:  <br/>
<img src="https://i.imgur.com/yN3dHFY.jpeg" height="80%" width="80%"/>
<br />
<br />
Create an internal network in adapter 2 labeled "intnet":  <br/>
<img src="https://i.imgur.com/GHfSQly.jpeg" height="80%" width="80%"/>
<br />
<br />
Verify your Ethernet settings (which ones the internal network and which is the NAT) The internal network would be the 172.16.0.1, while the NAT would be the 169.254.209.133 from the home network:  <br/>
<img src="https://i.imgur.com/IRIasTs.png" height="80%" width="80%"/>
<br />
<br />
Input IP address and Subnet mask. Use loopback address 127.0.0.1 in the DNS Server or 169.254.209.133 to loop to the computer to itself:  <br/>
<img src="https://i.imgur.com/SwsJTlx.png" height="80%" width="80%"/>
<br />
<br />
Go to Add Roles in the Server Manager and choose the server. Make sure to check mark "active domain services" after. Hit next until install appears:  <br/>
<img src="https://i.imgur.com/dG5fn9Q.png" height="80%" width="80%"/>
<br />
<br />
Click the Flag with the yellow triangle to create the domain. Select "Add new forest" and create a Root domain name. Type in Password1 for the password, hit next and install:  <br/>
<img src="https://i.imgur.com/UuAKNHf.png" height="80%" width="80%"/>
<br />
<br />
Login to the new domain:  <br/>
<img src="https://i.imgur.com/BQK1twi.png" height="80%" width="80%"/>
<br />
<br />
Go to start into Active Directory Users and Computers in the virtual Windows server:  <br/>
<img src="https://i.imgur.com/vi4vYzC.png" height="80%" width="80%"/>
<br />
<br />
Go into "mydomain.com". Select "New" and "Organizational Unit". Label the folder _ADMINS and uncheck "Protect container from accidental deletion" and create a new user. User Login name should be a-gmuller. Click a-gmuller, select properties, member of, add. Type "domain admins" and click check names. Log out and log into other user with a-gmuller and Password1:  <br/>
<img src="https://i.imgur.com/IiAe6JJ.png" height="80%" width="80%"/>
<br />
<br />
Select Add Roles and Features. Hit "Next" until you see a list with "Remote Access" as a checkbox and the "Routing" checkbox. Setup Routing and Remote Access:  <br/>
<img src="https://i.imgur.com/TTrCp5J.png" height="80%" width="80%"/>
<br />
<br />
 Select "DC Local" and "Configure and Enable Routing and Remote Access". Click "NAT" and select "INTERNET" as the interface: <br/>
<img src="https://i.imgur.com/yc2bQ44.png" height="80%" width="80%"/>
<br />
<br />
(Setting Up DHCP Server) Click "Add Roles and Features" Select "DHCP" checkbox and install. Set the DHCP Scope by selecting "Tools" and "DHCP". Click on the server and select "New Scope". Name it 172.16.0.100-200 as this is the range. 24 for the length. 255.255.255.0 for the subnet mask. 172.16.0.1 for the IP address and click "Add":  <br/>
<img src="https://i.imgur.com/ARngqLk.png" height="80%" width="80%"/>
<br />
<br />
Use this list of names and run Powershell ISE. Use the script provided and generate users:  <br/>
<img src="https://i.imgur.com/lBQmyqY.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://i.imgur.com/ywHUu9k.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://i.imgur.com/dBYM3xl.png" height="80%" width="80%"/>
<br />
 br />
<img src="https://i.imgur.com/DN7LhI6.png" height="80%" width="80%"/>
<br />
<br />
Use Windows 10 ISO and create "CLIENT 1":  <br/>
<img src="https://i.imgur.com/gR8n9cr.png" height="80%" width="80%"/>
<br />
<br />
Check the status using "ipconfig and ping. Set router properties".:  <br/>
<img src="https://i.imgur.com/NTRtgFH.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://i.imgur.com/YnbN5lR.png" height="80%" width="80%"/>
<br />
<br />
Boot CLIENT 1 and verify gmuller. SUCCESS:  <br/>
<img src="https://i.imgur.com/SeMFjBN.png" height="80%" width="80%"/>
<br />
<br />
<img src="https://i.imgur.com/r9V0vGA.png" height="80%" width="80%"/>
<br />

 
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
