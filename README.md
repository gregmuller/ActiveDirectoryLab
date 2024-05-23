<h1>Active Directory Home Lab</h1>

In this lab we're going to walk through how to create a 1000+ user Active Directory home lab environment using Oracle VirtualBox. 

<h2>Languages/Utilities/Evironments Used</h2>

- <b>Windows 10 Pro</b> 
- <b>Windows Server 2019</b>
- <b>Oracle VirtualBox</b>
- <b>Active Directory</b>
- <b>Powershell</b>

<h2>Program walk-through:</h2>

<p align="center">
<img src="https://i.imgur.com/gpohvC1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Download Oracle VirtualBox: <br/>
<img src="https://i.imgur.com/rWXYC4p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Download Windows 10 ISO:  <br/>
<img src="https://i.imgur.com/bOYGhPH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Label Your Machine "DC": <br/>
<img src="https://i.imgur.com/eLACBX6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Change "Clipboard" and "Drag'n'Drop" to "Bidirectional":  <br/>
<img src="https://i.imgur.com/TdP8dLB.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a NAT in adapter 1:  <br/>
<img src="https://i.imgur.com/yN3dHFY.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create an internal network in adapter 2 labeled "intnet":  <br/>
<img src="https://i.imgur.com/GHfSQly.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Verify you Ethernet settings (which ones the internal network and which is the NAT):  <br/>
<img src="https://i.imgur.com/IRIasTs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Input IP address and Subnet mask:  <br/>
<img src="https://i.imgur.com/SwsJTlx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Go to Add Roles in the Server Manager and choose the server:  <br/>
<img src="https://i.imgur.com/dG5fn9Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Create a Root domain name:  <br/>
<img src="https://i.imgur.com/UuAKNHf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Login to the new domain:  <br/>
<img src="https://i.imgur.com/BQK1twi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Go into Active Directory in the virtual Windows server:  <br/>
<img src="https://i.imgur.com/vi4vYzC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a new user:  <br/>
<img src="https://i.imgur.com/IiAe6JJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Setup Routing and Remote Access:  <br/>
<img src="https://i.imgur.com/TTrCp5J.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/yc2bQ44.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Set the DHCP Scope:  <br/>
<img src="https://i.imgur.com/ARngqLk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Use this list of names and run Powershell ISE. Use the script provided and generate users:  <br/>
<img src="https://i.imgur.com/lBQmyqY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/ywHUu9k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/dBYM3xl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 br />
<img src="https://i.imgur.com/DN7LhI6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Use Windows 10 ISO and create "CLIENT 1":  <br/>
<img src="https://i.imgur.com/gR8n9cr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Check the status using "ipconfig and ping. Set router properties". Address lease set to eight days:  <br/>
<img src="https://i.imgur.com/NTRtgFH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/YnbN5lR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Boot CLIENT 1 and verify gmuller. SUCCESS:  <br/>
<img src="https://i.imgur.com/SeMFjBN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/r9V0vGA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
