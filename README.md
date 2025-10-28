<h1> - Windows User & Group Management </h1>

<h2>Description</h2>
This project shows various system administrator concepts like creating and managing Users and NTFS permissions. I also wanted to try and create a user with PowerShell. 
<br />


<h2>Programs, Tools and Utilities Used</h2>

- <b>Local Users and Groups</b> 
- <b>PowerShell</b>
- <b>File Explorer </b>
- <b>Local Security Policy </b>



<h2>Program walk-through:</h2>

<p align="center">
Launch the Local Users & Groups. You can find this under Control Panel or you can launch Run and utilise "lusrmgr.msc" : <br/>
<img src="https://i.postimg.cc/6QHjSLSx/1-run-lusrmgr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Here I am creating an example set of three users.
  1. An Administrator (Will)
  2. A Standard User (Clive)
  3. Limited Access user (Intern Joe).
  
  I'm using the GUI to create users and change what group they are a part of in Properties:  <br/>
<img src="https://i.postimg.cc/FKPWqgqs/2-create-user-accounts.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
For the 3rd user Jeremy, I decided to add them using PowerShell as a mini-exercise. Making sure to run as administrator and I just set the password as my initials of 'wfjc' just for this occasion.
 The PowerShell Script I used is "New-LocalUser -Name "Intern_Jeremy" -Fullname "Jeremy Intern" -Description "Limited User" -Password (Read-Host -AsSecureString "wfjc")" : <br/>
<img src="https://i.postimg.cc/BvhYycy4/3-Powershell-creation-account.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Here I am just confirming to see whether Jeremy the intern was added by using 'Get-LocalUser' in PowerShell. I then refresh Users and Groups and crosscheck to make sure:  <br/>
<img src="https://i.postimg.cc/CKvPtHtY/4-Get-Local-User-Powershell-works.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Here we are adding different created users to various groups. I am adding Will to the administrator group as an example here:  <br/>
<img src="https://i.postimg.cc/nLdR5Y5L/5-Adding-users-to-groups.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Here I wanted to create a custom security group in the way of a 'Finance department' that could be commonly found in many organisations domain. Clive is part of the 'FinanceTeam' and I only want him and others in the finance department to have access to the Finance departments folders and group documents obviously, therefore I only add Clive, not Jeremy, for example, to the FinanceTeam group.:  <br/>
<img src="https://i.postimg.cc/hjfyqQWW/6-Custom-Security-Group.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
To illustrate my last point, I created a folder known as FinanceData meant as a folder used explicitly by the Finance group. To set the permissions locally, I use NTFS permissions (Security tab). If I wanted to set permissions over the network, I would use 'Sharing' permissions tab, this would be useful if the organisations domain is large and perhaps employees are using Roaming Profiles if they don't always use the same computer when starting their shift.
I also made sure to break inheritance so that the created folder didnt automatically provide permissions to the parent folder!:  <br/>
<img src="https://i.postimg.cc/ydkQz34B/7-NTFS-permission-change.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Finally I sought to set a password policy for the users in the network. I opened 'Run' and initialised 'secpol.msc' which brought me to Local Security Policy console. Under Account Policies you can set password policies for users.
I chose to enforce Password Complexity, max password age of 90 days and a minimum password length of 8+ characters. This is great for security and enables you to have some additional hardening of your network:  <br/>
<img src="https://i.postimg.cc/mDtXG1fB/8-Password-Policy-enforcing.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
These are a few ways you can work some SysAdmin concepts. Local Users and Groups is particularly useful for creating a lot of users/groups in an organisation, using PowerShell if you are comfortable with it.
