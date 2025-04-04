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
<p>
<h3 align="center">Create a Resource Group inside Azure. Now, create a Windows 10 Virtual Machine (VM),When creating the Virtual Machine, make sure your VM and resource group have the same region. It is advisable to remember the Username and password you chose and allow Azure to create a new Virtual Network (Vnet).
After clicking on the 'Review and create" button,it might take a while to complete deployment.</h3>
</p>
<p>
	<img src="https://i.imgur.com/8N7SyL4.png" height="75%" width="100%" />
          <br />
	<br />
        <img src="https://i.imgur.com/7QIUuxj.png" height="35%" width="50%" />
</p>
<br />
<br />
<h3 align="center">Open Windows Remote Desktop on your computer and paste the public IP address of the virtual machine that was created, then click on the "connect" button. You will then be asked for the Username and Password of the VM, do that to access the VM. </h3>
        <p>
	<img src="https://i.imgur.com/mS1sFhC.png" height="50%" width="70%" />
	</p>
<h3>Within the Virtual machine, download the osTicket-Installation-Files.zip.
	<p>
	<img src="https://i.imgur.com/IcgeaNv.png" height="50%" width="70%" />
	</p>
	<br />
	 <p> Unzip it onto your desktop by right clicking it and click on "Extrack all". </h3>
         </p>
	 <p>
	<img src="https://i.imgur.com/ZoHkqYg.png" height="20%" width="30%" />
         </p>
	 <br />
  <h3 align="center">Now we have to enable IIS in Windows (It's a web server that will help run ostickets). 
Go to your Search Bar > Type "Control Panel" > Click "Programs" > "Turn Windows features on or off" > Look for "Internet Information Services".</h3>
<br />
<p>
	<img src="https://i.imgur.com/DNeIRoM.png" height="20%" width="50%" />
</p>
<br />
<br />
<h3 align="center"> Expand IIS > Expand the "World Wide Web" > Expand "Application Developer" > Check the "CGI" button & press "Ok". You will need CGI to download the PHP Manager which is a back-end web programming language that allows osTicket to run off a web browser.</h3>
<br />
<p>
  <img src="https://i.imgur.com/nAczn0a.png" height="20%" width="50%" />
</p>
<br />
<h3 align="center">Installing PHP Manager</h3>
<p>
<h3 align="center">Now we need to download PHP which is a backend web server language that is needed to run osTicket. 
	<br />
	Go to osticket installation folder > Double click "PHPManagerforIIS" > Agree with all the terms and we've now downloaded the PHP manager.</h3>
<p>
  <img src="https://i.imgur.com/55s3HDP.png" height="20%" width="50%" />
	<br/>
	<br/>
   <img src="https://i.imgur.com/oHkGLSs.png" height="20%" width="50%" />
</p>
<br/>
<h3 align="center">Installing Rewrite Module</h3>
<p>
<h3 align="center"> Go to osticket installation folder > Double click "rewrite_amd64" > Agree with all the terms and it should now be installed onto the Computer.</h3>
<p>
  <img src="https://i.imgur.com/fDXjTge.png" height="20%" width="50%" />
</p>
<br/>
<h3 align="center">CREATE DIRECTORY C:\PHP</h3>
<p>
<h3 align="center"> Go to File Explorer > Click on "This PC" > Click on "Windows C(drive)" and create a new folder named "PHP".
	            Now go to the OSticketinstallation-folder > Right click on "php-7.3.8-nts-Win32-VC15-x86" to extract all > click "Browse" and go to the C drive and 
                    direct the extraction to the PHP folder.
</h3>
<p>
  <img src="https://i.imgur.com/NFPuc5D.png" height="20%" width="70%" />
</p>
<br/>
<h3 align="center">DOWNLOADING VC_REDIST</h3>
<h3 align="center"> Double click on "VC_redist.x86, Agree with it's terms and agreements and finish installing.
</h3>
<p>
  <img src="https://i.imgur.com/4vaUR52.png" height="20%" width="70%" />
</p>
<br/>
<h3 align="center">DOWNLOAD MySQL </h3>
<h3 align="center"> Go to “osTicket-Installation-Files” folder > Doubleclick "mysql-5.5.62-win32" to begin installation, Make sure to choose "Typical setup".
	             Lauch it after install and insert the username and password of your choice then make sure to tick all the box.
	           <br />
	             <p> <img src="https://i.imgur.com/VkUa41f.png" height="20%" width="50%" />
			     <br />
			     <br />
			 <img src="https://i.imgur.com/iK7iHP1.png" height="20%" width="50%" />
		     </p>
	           <br />
	            Next, search for IIS in the searchbar and open it as an admin > Double click "PHP Manager" > Click "Register new PHP version" 
	            > Browse to the PHP floder and choose "php-cgi" > Now reload IIS by clicking Stop(wait) and start. 
</h3>
<p>
  <img src="https://i.imgur.com/CSxUqjC.png" height="20%" width="50%" />
<br />
	<br />
  <img src="https://i.imgur.com/lxw6vwb.png" height="20%" width="50%" />
</p>
<br />
<br />
<h3 align="center">Installing osTicket v1.15.8</h3>
<p>
	Extract and copy the “upload” folder into the C drive "wwwroot" (“c:\inetpub\wwwroot”). Then change the file named from "upload" to "osTicket"
</p>
	<img src="https://i.imgur.com/c6gwg4e.png" height="20%" width="50%" />
<p>
	<img src="https://i.imgur.com/yfwtbkQ.png" height="20%" width="50%" />
</p>
<br />
<br />
<h3 align="center">Enable some Extensions in IIS</h3>
<p>
    Under IIS manager, go to sites--> defualt-->ostickets in the top left hand corner > Click osticket > Click "browse 80" under manage folder to 
    open the osticket web page. Now back to IIS, Double-click PHP Manager > Click “Enable or disable an extension” > Click enable "php_imap.dll"
    "php_intl.dll" and "php_opcache.dll".
    	<br />
	 <p> 
	<img src="https://i.imgur.com/vF3kZDd.png" height="20%" width="50%" />
	<img src="https://i.imgur.com/LzkzPns.png" height="20%" width="50%" />
         </p>
	<br />
      Now refresh the osTicket site in your browser to observe the changes. 
      <p>
	    <br />  
	<img src="https://i.imgur.com/6UcBVnL.png" height="20%" width="50%" />
</p>
<br />
<br />
<h3 align="center">Rename</h3>
<p>
   Go to Windows C drive > Click "inetpub" >  Click "wwwroot" >  Click "osticket" >  Click "include" and then you change the name of the php 
   from "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php" to "C:\inetpub\wwwroot\osTicket\include\ost-config.php"
</p>
<br />
<h3 align="center">Assign Permissions (ost-config.php)</h3>
<p>
     To assign Permissions, Right click "ost-config.php" > Click "Properties" > Click "Advanced" > Disable inheritance
     >Click "remove all inherited permissions from the object" > Add everyone to the permissions.
</p>
 <p>
	    <br />  
	<img src="https://i.imgur.com/SV6D0uI.png" height="20%" width="50%" />
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket </h3>
<p>
     Open osTicket in the browser or refresh the webpage and input all the information required. Make sure the email 
     you choose is your work email which you will use to receive email from customers.
</p>
  <br />  
 <p>
	<img src="https://i.imgur.com/PNztWP5.png" height="20%" width="50%" />
</p>
<br />
<br />
<h3 align="center">Downloading and Installing HeidiSQL</h3>
<p>
	Go back to the “osTicket-Installation-Files” folder and Double click on "HeidiSQL" to install.
	Then create a new session and input a username and password that you'd remember or simply write it down as
	it is very important to not forget them. Create and connect.
	<br />
	<p>
	<img src="https://i.imgur.com/YiJMWhq.png" height="20%" width="50%" />
        </p>
	<br />
	Create a database called “osTicket (Click on "Create New")
        <p>
	<img src="https://i.imgur.com/IJIqulX.png" height="20%" width="50%" />
        </p>
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser</h3>
<p>Go back to the webpage > Go to the database setting > Input all the MySQL information > Click "Install Now" button</p>
<p>Congratulations, hopefully there was no error!!</p>
<p>
	<img src="https://i.imgur.com/rSmf2m5.png" height="50%" width="80%" />
</p>
<br />
<br />
<h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</h3>
<br />
<p>
	<img src="https://i.imgur.com/xddlBLV.png" height="50%" width="90%" />
</p>
<br />
<br />
<h3 align="center"> Congrats, You've Finished Installing osTicket.</h3>
