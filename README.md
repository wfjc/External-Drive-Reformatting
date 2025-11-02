<h1>How to reformat an external storage drive</h1>

<h2>Description</h2>
Project consists of reformatting a USB drive from FAT32 to exFAT using the command prompt. I check the work with the Disk Defragmentation Tool and also show how the drive can be encrypted for further security.
<br />


<h2>Utilities Used</h2>

- <b>Command Prompt</b> 
- <b>Format command</b>
- <b>Optimise Drives (Disk Defragmentation Tool)</b>
- <b>Bitlocker</b>

<h2>Environments Used </h2>

- <b>Windows 11</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Open command prompt, select your drive. I changed mine and set it as B:. It is an external USB stick with a default name of 'Store N Go'.
The USB stick is FAT32, which is an older format style, we will be formatting to the more up to date exFAT as I want a storage device that is suitable for cross-platform OS.
You can use the GUI of the Disk Management tool in Control Panel, or you can reformat the drive directly in the command prompt using the format command in the way of 'format b: /fs:exFAT' : <br/>
<img src="https://i.postimg.cc/Dz5yjhDD/reformat-drive-1.png" height="80%" width="80%" alt="Open command ready drive"/>
<br />
<br />
Run the command and then command prompt will ask if you want to rename. I renamed to W Choblet Storage, although it decided that was too long of a name, so I settled with W Choblet (my name). Now external drive B is reformatted to exFAT!:  <br/>
<img src="https://i.postimg.cc/jdcLLzq6/Reformatting-external-drive-2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


Using the Disk Management Console, we can see that drive B has been reformatted. If we wanted, we could partition that drive further and create a separate area, perhaps for Mac only as APFS instead of exFAT. Though the drive is only 28 odd GB. If this was a large 2TB drive for example, you might want to create multiple partitions. Perhaps you want to boot using Linux off your external drive, you would format an ext4 partition:  <br/>
<img src="https://i.postimg.cc/7Z43Z5dc/Reformat-drive-2025-10-28-at-09-23-43.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Additionally, if the drive needed to be defragmented or decluttered, we could use 'Defragment and Optimise Drives' found in Windows Tools in Windows 11. But because we just reformatted the drive from FAT32 into exFAT, this feature is not available. If we wanted to do this, we would need to reformat to NTFS, a modern Windows only format type that supports the optimise drive feature and other things like journaling etc; however I chose exFAT as it's best for cross-platform storage purposes:  <br/>
<img src="https://i.postimg.cc/cLMbxg1K/Screenshot-2025-10-28-at-10-01-29.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Finally, if we wanted to secure the drive using Windows, there is the option to use Bitlocker. Because we are using removable storage, we use 'Bitlocker-To-Go', this is found in Bitlocker Drive Encryption under Control Panel.
  This action encrypts the device with a password or even a smart card. It just adds another layer of security to removable drives:  <br/>
<img src="https://i.postimg.cc/2yDWS6SZ/bit-locker-option-reformat-28-10-25.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
