<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




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

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/81e09527-949d-4e1b-b7db-c6d7e0d54e1f)

Download and install PHPManagerForIIS_V1.5.0.msi and rewrite_amd64_en-US.msi from the install folders in the other web browser.

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/5a618b79-f590-4b15-98e2-1dd47165386f)

Next, create a new directory in your C drive called PHP or C:\PHP.

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/559345a0-df75-4861-b653-9aabfdaee1ff)

Now, download and install php-7.3.8-nts-Win32-VC15-x86.zip and then extract all the contents into C:\PHP.

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/cdc48559-e620-4cc6-987c-47f60a132437)

Download and install VC_redist.x86.exe.

Download and install mysql-5.5.62-win32.msi

Typical Setup > Launch Wizard > Standard Configuration > Next > Set the password to "Password1" > Execute

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/0dc28303-dce2-4828-8704-fe853a12c054)

Search for IIS in the search bar and open it as administrator.

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/8f36f8ba-8e94-4a50-88c9-24ace51a1b43)

After opening IIS Manager as admin, click on "PHP Manager" icon > click on "Register new PHP version" > Browse files > C:\PHP > open "php-cgi"

Restart the IIS server.

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/9c28342d-a8fa-4315-9673-11badb43fc88)

Now, download the file osTicket-v1.15.8 from the install files. After it finishes downloading, open two file explorer windows and navigate to the osTicket-v1.15.8.zip folder and "inetpup".

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/2066b6b2-aa99-4abd-8f35-bdef437209c5)

In the inetpup folder, go to "wwwroot" and transfer the "upload" folder in from the osTicket zip. After it finishes, rename the "upload" folder to "osTicket".

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/b4714d7b-1b46-46ee-9209-88b505b6f012)

Restart the IIS server.

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/4f25ba83-5ba5-4f21-b604-e33fe8110e9f)

Restart IIS as admin and expand VM1 on the left menus > Sites > Default Web Sites > Click osTicket. Click on "Browse *.80 which will open web browser that will open an osTicket installer.

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/9c04154e-131d-470e-9266-de1b62f42373)

Head back to IIS Manager and into osTicket again. Click on the "PHP Manager" icon and then at the bottom click "Enable or disable an extension".

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/cc4bbed3-b571-4a86-9f84-9ffd3c47bec5)

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/7d79e07c-105b-491b-870a-d650eb7eadad)

Refresh the web browser that has the osTicket installer and observe the changes. It should look like the screenshot above

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/ed3b95e7-8821-4869-846b-cb8beb3a5bdf)

Open up File Explorer and navigate back to osTicket inside of inetpub. Click on Include and locate "ost-sampleconfig.php" at the bottom of the list.

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/24d394d2-31dd-4a63-bde4-b560da2cd012)

Then rename the file from "ost-sampleconfig.php" to "ost-config.php"

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/dbfe0219-3703-4f6d-b347-0a7716d2a79f)

Now, click on that files Properties > Security > Advanced > Disable Inheritance > Remove all

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/9ba37e59-421b-4718-9c9f-6d7ba9aead71)

Check the box for "full control" > press OK > Apply and then OK until the properties window closes.

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/037b5b95-9e91-4ffe-9bac-0befb1c02622)

Head back to the osTicket installer and press "Continue".

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/8c9242b5-30eb-4cfa-9f20-f22d0fd28bf1)

Name your Helpdesk to your liking and a random email. This tutorial will be using the name "Helpdesk" and the email "john@helpdesk.com". You will continue the form by making your own Admin user credentials. I used a random email and created a password; be sure to jot these down if you are forgetful for this tutorial only.

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/aaaa0e57-0afb-43a6-9f71-41b120ecd556)

Next, download HeidiSQL from the drive folder, which contains a word doc with a link to the downloader. Open the installer and click continue all the way through. Once it has been installed, you will click the "New" button at the bottom of the window > the username should already be set to "root" and type the password that we created "Password1" > press open.

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/ddd55429-c60e-4946-ba97-5b851a7fd857)

nside of HeidiSQL, right click "Unnamed" > Create new > Database > Name it "osTicket"> Click OK.

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/ae3b8690-29e1-4823-baf4-c463e8ce957b)

Head back to the osTicket installer and enter the username and password. This should be "root" and "Password1". The hostname should also be "osTicket".

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/2909bdd0-055c-48cd-aa1d-80e6324ef875)

To clean up some of the extra stuff in the tutorial, we'll browse back into C:\inetpub > wwwroot > osTicket > delete the "setup" folder.

![image](https://github.com/Timothyjdm44/osticket-prereqs/assets/142111972/97f85ba6-91f9-4026-8fc2-eae4f8be81b5)
