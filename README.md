<h1>Active Directory Home Lab</h1>

In this lab we're going to walk through how to create an Active Directory home lab environment using Oracle Virtual Box. 

<h2>Languages and Utilities Used</h2>

- <b>Oracle</b>

<h2>Environments Used </h2>

- <b>Windows 10 Pro</b> 
- <b>Windows Server 2019</b> 

<h2>Program walk-through:</h2>

<p align="center">
Download Oracle Virtualbox: <br/>
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
Go into Active Directory in the virtual Windows server:  <br/>
<img src="https://i.imgur.com/vi4vYzC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a new user:  <br/>
<img src="https://i.imgur.com/IiAe6JJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
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
