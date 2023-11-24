<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket
- HeidSQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Remote Desktop Connection to your Windows 10 Virtual Machine
- Install / Enable Internet Information Services in Windows With CGI
- Download and install PHP Manager for internet information Services
- Download and install the Rewrite Module
- Create the directory C:\PHP
- Download PHP 7.3.8 and unzip the contents into C:\PHP
- Download and install VC_redist.x86.exe
- download and install MySQL 5.5.62
- Open IIS as an Admin and register PHP from within IIS
- Install osTicket v1.15.8
- Download and install HeidiSQL
- Continue setting up osTicket in the browser

<h2>Installation Steps</h2>

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/cd39dd59-e91a-41ea-90e4-371405dc315e)


</p>
<p>
First, we will be connecting to our VM through a Remote Desktop connection. Go to the VM on the Azure Portal > Copy Public IP Address > Connect with RDC to do this.


</p>
<br />

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/ba16a325-342d-4214-a00d-04a548090dd7)

Paste the link into the browser inside of your VM.

https://drive.google.com/drive/folders/1DABjdlQAXxIvWIURTiBelD0rw6IzLNru
</p>
<br />

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/84e27fc0-cbca-46e1-a048-d323e2af6527)

</p>
Go to the Programs section in the Control Panel and click on "Turn Windows features on or off."


![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/6fc52af2-3a7f-4ded-81f9-4ca75cf3757d)

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/54c1b438-4d72-4df7-805b-35fe7851f2e2)

After you install IIS, open a new browser and type into the search bar "127.0.0.1". The IIS page should pop up, but if you do not see it, you must go back to the control panel to ensure CGI is checked.
