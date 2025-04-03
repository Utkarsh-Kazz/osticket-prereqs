# osticket-prereqs

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png"/>
</p>

<h1> How to Install osTicket </h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br/>

<h2> Files to Download </h2>

- ### [Download Files](https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) 📁

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Windows 10 (21H2)
- Windows Remote Desktop 
- Internet Information Services (IIS)

  <h2> List of Prerequisites </h2>

- Creating a Virtual Machine in Azure
- Installing osTicket v1.15.8
- Installing HeidiSQL
- Installing MySQL then and set up user and pass
- Installing PHP
- Installing Microsoft Visual C++ Redistributable
  <h2>Steps</h2>
<h3 align="center">Creating Virtual Machine in Azure</h3>
<br />
<p>
<h3 align="center">Create a Resource Group inside Azure.</h3>
<br />
</p>
<p>
<img src="https://i.imgur.com/eBi5k2l.png" height="75%" width="100%" />
</p>
<p>
<h3 align="center">Now, create a Windows 10 Virtual Machine (VM),When creating the Virtual Machine, make sure your VM and resource group have the same region. It is advisable to remember the Username and password you chose and allow Azure to create a new Virtual Network (Vnet).
After clicking on the 'Review and create" button,it might take a while to complete deployment.</h3>
<br />
</p>
<p>
	<img src="https://i.imgur.com/dEF1c7h.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Open Windows Remote Desktop on your computer and paste the public IP address of the virtual machine that was created, then click on the "connect" button. You will then be asked for the Username and Password of the VM, do that to access the VM. </h3>
<br />
        <p>
	<img src="https://github.com/Joeljjoseph1998/osticket-prereqs/assets/50834280/2e71fd86-4198-47aa-aa1a-d0aed1b8e0eb"/>
	</p>
<br />
<h3 align="center">Within the Virtual machine, download the osTicket-Installation-Files.zip.
	 <p> <br /><br />
	Unzip it onto your desktop by right clicking it and click on "Extrack all". </h3>
         </p>
<h3 align="center">Now we have to enable IIS in Windows (It's a web server that will help run ostickets). 
	<br />
Go to your Search Bar > Type "Control Panel" > Click "Programs" > "Turn Windows features on or off" > Scroll down to "Internet Information Services (IIS).</h3>
<br />
<p>
	<img src="https://i.imgur.com/iB0DDRd.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Once clicked, find the "Internet Information Services" expand it and then expand the "World Wide Web" tab. Afterward, expand the application Developer tab. Finally check the "CGI" button & press Ok. You will need CGI to download the PHP Manager. The PHP manager is a back-end web programming language that allows osTicket to run off a web browser.</h3>
<br />
<p>
  <img src="https://github.com/Joeljjoseph1998/osticket-prereqs/assets/50834280/a6af9c35-e10c-4d7e-b2c8-30ffbe128f08" height="75%" width="100%"/>
</p>
<br />
<h3 align="center">Installing PHP Manager</h3>
<br />
<p>
<h3 align="center">Now we need to download PHP which is a backend web server language that is needed to run osTicket. 
	<br />
	Go to osticket installation folder > Double click "PHPManagerforIIS" > Agree with all the terms and we've now downloaded the PHP manager.</h3>
<p>
  <img src="https://i.imgur.com/pmwpPEu.png"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">Installing Rewrite Module</h3>
<br />
<p>
<h3 align="center"> Go to osticket installation folder > Double click "rewrite_amd64" > Agree with all the terms and it should now be installed onto the Computer.</h3>
<p>
  <img src="https://github.com/Joeljjoseph1998/osticket-prereqs/assets/50834280/28cf2dd0-d39e-45f8-a01b-61aec6657228"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">CREATE DIRECTORY C:\PHP</h3>
<br />
<p>
<h3 align="center"> Go to File Explorer > Click on "This PC" > Click on "Windows C(drive)" and create a new folder named "PHP".
	            Now go to the OSticketinstallation-folder > Right click on "php-7.3.8-nts-Win32-VC15-x86" to extract all > click "Browse" and go to the C drive and direct the extraction to the PHP folder.
</h3>
<p>
  <img src="https://github.com/Joeljjoseph1998/osticket-prereqs/assets/50834280/18746085-a3cf-4f1f-b0d5-5cd73f969319"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">DOWNLOADING VC_REDIST</h3>
<br/>
<h3 align="center"> Double click on "VC_redist.x86, Agree with it's terms and agreements and finish installing.
</h3>
<p>
  <img src="https://i.imgur.com/Gx8ryBV.png"75%" width="100%"/>
</p>
<br/>
<h3 align="center">DOWNLOAD MySQL </h3>
<h3 align="center"> Go to “osTicket-Installation-Files” folder > Doubleclick "mysql-5.5.62-win32" to begin installation, Make sure to choose "Typical setup".
	             Lauch it after install and insert the username and password of your choice then make sure to tick all the box.
	           <br />
	           <br />
	            Next, search for IIS in the searchbar and open it as an admin > Double click "PHP Manager" > Click "Register new PHP version" 
	            > Browse to the PHP floder and choose "php-cgi" > Now reload IIS by clicking Stop(wait) and start. 
</h3>
<p>
  <img src="https://i.imgur.com/IVpLg40.png"75%" width="100%"/>
<br />
  <img src="https://i.imgur.com/zdhWXNx.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Installing osTicket v1.15.8</h3>
<br />
<p>
	Extract and copy the “upload” folder into the C drive "wwwroot" (“c:\inetpub\wwwroot”). Then change the file named from "upload" to "osTicket"
</p>
	<img src="https://i.imgur.com/0MUJLMU.png" height="75%" width="100%" />
	<img src="https://i.imgur.com/1h9goM8.png" height="75%" width="100%" />
<p>
	<img src="https://i.imgur.com/pDikkgq.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Enable some Extensions in IIS</h3>
<br />
<p>
    Under IIS manager, go to sites--> defualt-->ostickets in the top left hand corner > Click osticket > Click "browse 80" under manage folder to 
    open the osticket web page. Now back to IIS, Double-click PHP Manager > Click “Enable or disable an extension” > Click enable "php_imap.dll"
    "php_intl.dll" and "php_opcache.dll".
    	<br />
	<br />
      Now refresh the osTicket site in your browser to observe the changes. 
      <p>
	    <br />  
	<img src="https://imgur.com/a/nrQo0kz" height="75%" width="100%"/>
</p>
<br />
<br />
<h3 align="center">Rename</h3>
<br />
<p>
   Go to Windows C drive > Click "inetpub" >  Click "wwwroot" >  Click "osticket" >  Click "include" and then you change the name of the php 
   from "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php" to "C:\inetpub\wwwroot\osTicket\include\ost-config.php"
</p>
<p>
	<img src="https://i.imgur.com/TEw71SD.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Assign Permissions (ost-config.php)</h3>
<br />
<p>
     To assign Permissions, Right click "ost-config.php" > Click "Properties" > Click "Advanced" > Disable inheritance
     >Click "remove all inherited permissions from the object" > Add everyone to the permissions.
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket </h3>
<br />
<p>
     Open osTicket in the browser or refresh the webpage and input all the information required. Make sure the email 
     you choose is your work email which you will use to receive email from customers.
</p>
<br />
<br />
<h3 align="center">Downloading and Installing HeidiSQL</h3>
<br />
<p>
	<img src="https://i.imgur.com/AEg0b2P.png" height="75%" width="100%" />
</p>
<p>
	Go back to the “osTicket-Installation-Files” folder and Double click on "HeidiSQL" to install.
	Then create a new session and input a username and password that you'd remember or simply write it down as
	it is very important to not forget them. Create and connect.
	<br />
	<br />
	Create a database called “osTicket (Click on "Create New")
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser</h3>
<br />
<p>Go back to the webpage > Go to the database setting > Input all the MySQL information > Click "Install Now" button</p>
<p>
	<img src="https://i.imgur.com/akDyber.png" height="75%" width="100%" />
</p>
<p>Congratulations, there was no error!!</hp>
<p>
	<img src="https://i.imgur.com/J5omRoE.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</h3>
<br />
<p>
	<img src="https://i.imgur.com/8wvWH0H.jpg" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center"> Congrats, You've Finished Installing osTicket.</h3>
