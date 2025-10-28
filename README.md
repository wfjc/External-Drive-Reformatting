<h1>How to reformat an external storage drive</h1>

<h2>Description</h2>
Project consists of reformatting a USB drive B:/ from FAT32 to exFAT
<br />


<h2>Languages and Utilities Used</h2>

- <b>Command Prompt</b> 
- <b>Format command</b>

<h2>Environments Used </h2>

- <b>Windows 11</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Open command prompt, select your drive, mine is 'Store N Go' and reformat using the line 'format b: /fs:exFAT'.
  I want to convert the file from FAT32 to exFAT....: <br/>
<img src="https://i.postimg.cc/Dz5yjhDD/reformat-drive-1.png" height="80%" width="80%" alt="Open command ready drive"/>
<br />
<br />
Run the command and then command prompt will ask if you want to rename. I renamed to W Choblet. Now external drive B is reformatted to exFAT!:  <br/>
<img src="https://i.postimg.cc/jdcLLzq6/Reformatting-external-drive-2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Using the Disk Management Console, we can see that drive B has been reformatted. If we wanted, we could partition that drive further and create a separate area, perhaps for Mac only as APFS instead of exFAT:  <br/>
<img src="https://i.postimg.cc/7Z43Z5dc/Reformat-drive-2025-10-28-at-09-23-43.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
