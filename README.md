
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Setting up a virtual machine
- Installing/enabling IIS (Internet Information Services)
- Downloading prerequisite installation files (PHP Manager for IIS, Rewrite module, PHP 7.3.8, etc) 
- Registering PHP from within IIS
- Downloading OSTicket (v1.15.8)

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/YuKomFr.png"/>
</p>
<p>
To start off, we set up an Azure virtual machine with 4vCPUS. The operating system we will use will be Windows 10. This is where we will install all the prerequisite files and setup OSTicket.
</p>
<br />

<p>
<img src="https://i.imgur.com/srPfsX2.png"/>
</p>
<p>
Next, we log into the newly created virtual machine with remote desktop using its public IP address. This address can be found in the "Overview" tab for the virtual machine we just created. We will use the credentials we made when we created the virtual machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/PMcagG9.png"/>
</p>
<p>
After logging into the virtual machine, navigate to the control panel, and head to "Programs and Features", then hit "Turn windows Features on or off."
</p>
<br />

<p>
<img src="https://i.imgur.com/PMcagG9.png"/>
</p>
<p>
After logging into the virtual machine, navigate to the control panel, and head to "Programs and Features", then hit "Turn windows Features on or off."
</p>
<br />

<p>
<img src="https://i.imgur.com/9RPQdV0.png"/>
</p>
<p>
Head to the "Internet Information Services" section and click on the drop down list. Navigate to "Web Management Tools." After doing so, check all the boxes in the drop down list.
</p>
<br />

<p>
<img src="https://i.imgur.com/p2qGYwq.png"/>
</p>
<p>
After turning on all web management tools, head back to "World Wide Web Services," then head to "Application Development Features," and check the box next to "CGI."
</p>
<br />

<p>
<img src="https://i.imgur.com/9r7ka4O.png"/>
</p>
<p>
Next, we are going to download and install some prerequisite files needed to setup and run OS Ticket. We will need to download the following files: PHPManagerForIIS_V1.5.0.msi, rewrite_amd64_en-US.msi, php-7.3.8-nts-Win32-VC15-x86.zip, VC_redist.x86.exe, and mysql-5.5.62-win32.msi.
</p>
<br />

<p>
<img src="https://i.imgur.com/9r7ka4O.png"/>
</p>
<p>
After downloading all the prerequisite fiiles, make sure to unzip the contents of "PHP 7.3.8" into a newly made directory named "C:\PHP." Then, open IIS (Internet Information Services) as an administrator.
</p>
<br />

<p>
<img src="https://i.imgur.com/9r7ka4O.png"/>
</p>
<p>
After opening IIS as an admin, register PHP from within IIS. Then, refresh the page.
</p>
<br />

<p>
<img src="https://i.imgur.com/9r7ka4O.png"/>
</p>
<p>
Next, download install osTicket v1.15.8 and its accompanying files. Then, copy the "upload" folder to "c:\inetpub\wwwroot." Lastly, make sure to refresh IIS.
</p>
<br />

<p>
<img src="https://i.imgur.com/9r7ka4O.png"/>
</p>
<p>
Next, open IIS, head to "sites", then head to "default," and select "osTicket." Then, click on "Browse *:80."
</p>
<br />

<p>
<img src="https://i.imgur.com/9r7ka4O.png"/>
</p>
<p>
From within IIS, navigate to PHP Manager, and toggle on the following extensions: "php_imap.dll," "php_intl.dll," and "php_opcache.dll."
</p>
<br />

<p>
<img src="https://i.imgur.com/9r7ka4O.png"/>
</p>
<p>
When done enabling the above extensions, rename "ost-sampleconfig.php" to "ost-config.php" (under the "C:\inetpub\wwwroot\osTicket\include\" directory).
</p>

<p>
<img src="https://i.imgur.com/9r7ka4O.png"/>
</p>
<p>
Next, assign permissions to "Everyone" for the "ost-config.php" file.
</p>
<br />

<p>
<img src="https://i.imgur.com/9r7ka4O.png"/>
</p>
<p>
From within the browser, setup osTicket (name the helpdesk, provide a default email address for incoming tickets, etc).
</p>
<br />

<p>
<img src="https://i.imgur.com/9r7ka4O.png"/>
</p>
<p>
After setting up osTicket from within your browser, download and install HeidiSQL and use the installed files to finish setting up osTicket.
</p>
<br />

<p>
<img src="https://i.imgur.com/9r7ka4O.png"/>
</p>
<p>
Lastly, delete the "C:\inetpub\wwwroot\osTicket\setup" file and set permissions to "Read" only for "C:\inetpub\wwwroot\osTicket\include\ost-config.php".
</p>
<br />

<p>
<img src="https://i.imgur.com/9r7ka4O.png"/>
</p>
<p>
When done, you should be able to browse to your login page using the following url: "http://localhost/osTicket/scp/login.php."
</p>
<br />
