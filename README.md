
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
<img src="https://i.imgur.com/9r7ka40.png"/>
</p>
<p>
Next, we are going to download and install some prerequisite files needed to setup and run OS Ticket. We will need to download the following files: PHPManagerForIIS_V1.5.0.msi, rewrite_amd64_en-US.msi, php-7.3.8-nts-Win32-VC15-×86.zip,VC_redist.×86.exe, and mysql-5.5.62-win32.msi.
</p>
<br />

<p>
<img src="https://i.imgur.com/9r7ka40.png"/>
</p>
<p>
After downloading and setting up the necessary files, we will have to 
</p>
<br />

