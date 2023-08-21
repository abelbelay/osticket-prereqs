# osticket-prereqs<p align="center">
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

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

  - Azure VM running Windows 10
  - <a href="https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view">PHP Manager for IIS v1.5.0</a>
  - <a href="https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view">Rewrite Module</a>
  - <a href="https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view">PHP v7.3.8 NTS</a>
  - <a href="https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view">Microsoft Visual C++ Redistributable</a>
  - <a href="https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view">MySQL v5.5.62</a>
  - <a href="https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe">HeidiSQL v12.3.0.6589</a>

<h2>Installation Steps</h2>

<h3>Create a Resource Group</h3>
<p>
  <img src="https://user-images.githubusercontent.com/142059616/261181101-9a5b961f-8570-4710-b81e-9a8004421b93.png" height="60%" width="60%" alt="Creating a Resource Group"/>
</p>
<p><img src="https://user-images.githubusercontent.com/142059616/261181468-b1cf6919-897a-48fc-964e-617b79480b31.png" height="60%" width="60%" alt="Creating a Resource Group"/>
</p>
<p>
 Name your rescourse Group and select "Create". 
</p>
<p>
  <img src="https://user-images.githubusercontent.com/142059616/261181696-654eee52-b743-4307-a214-81a8c808369b.png" height="60%" width="60%" alt="Creating a Resource Group"/>
</p>
  Your Resource group has been successfully created!
<p>
  <br>
  <hr>
<h3>Creating A virtual Machine</h3>
<img src="https://user-images.githubusercontent.com/142059616/261184714-7833ec95-4dc9-48fa-aa71-b7f4cb8e0e4c.png" height="60%" width="60%" alt="Creating a virtual machine"/>
</p>
<p>
  Next you must create a virtual machine that will host OSticket.A virtual machine in Azure is like a digital computer that lives in the cloud, allowing you to run programs and operate like you would on a physical computer
</p>
<img src="https://user-images.githubusercontent.com/142059616/261185136-38673ca8-758b-46e2-aa6c-84b84cc58980.png" height="60%" width="60%" alt="Creating a virtual machine"/>
<p>
We are going to name our VM "vm-osticket" for best organizational practices. The image we are going to use is Windows 10 pro, as that is the operating system that we will use. 
</p>
<img src="https://user-images.githubusercontent.com/142059616/261185442-e21916d8-03ed-41fb-b97e-50e5a31ad83e.png" height="60%" width="60%" alt="Creating a virtual machine"/>
<p>We will select the 4vcpu option for the size for optimal performance.Create any username and password of your choice. Click "Review + Create". You can skip all the tabs until you get to Review and create your VM. Hold on for a few seconds for your VM to deploy, and you have now created your virtual machine
</p>
<br />
<hr>

<h3>Connect Virtual Machine using RDP(Remote Desktop)</h3>
<p>
<img src="https://user-images.githubusercontent.com/142059616/261189115-201883b4-1284-4a97-b5d4-72a9067f8dd8.png" height ="50% "width="80%" alt="Remote Desktop"/>
</p>

<p>
Go to the virtual Machine that was just created and copy the Public IP address .
</p>
<img src="https://user-images.githubusercontent.com/142059616/261189891-ff074ff6-952e-4eb5-b53f-a45ba5e5172a.png" height ="20% "width="50%" alt="Remote Desktop"/>
<img src="https://user-images.githubusercontent.com/142059616/261190125-4e63b3f8-e606-4111-870b-ece0d3e4d559.png" height ="20% "width="50%" alt="Remote Desktop"/>
<img src="https://user-images.githubusercontent.com/142059616/261190888-a616603a-0773-41e6-b124-d0779e7120e8.png" height ="20% "width="50%" alt="Remote Desktop"/>

<p>Open the remote desktop application and paste the IP address. Click "connect". Then you enter your log in information from earlier. A prompt will appear about the identity cannot be verified; just press "YES".</p>
<img src="https://user-images.githubusercontent.com/142059616/261193321-14204893-87fb-4a16-b8a3-98555fe5c742.png" height="40%" width="50%"/>
<p>You have now successfully created a Virtual Machine!!</p>

<br />
<hr>
<h3>Enabling Windows Feature</h3>
<img src="https://user-images.githubusercontent.com/142059616/261201802-e22e7d88-ac34-4efc-947c-ade1847aa972.png" height="40%" width="50%"/>
<p>Using the virtual machine press the ⊞ Win key, search for "turn windows features on or off"</p>
<img src="https://user-images.githubusercontent.com/142059616/261413395-56d61bc3-097d-41ba-941c-173c648ba889.png" height="40%" width="50%"/>
<p>- Find "Internet Information Services", then click the checkbox ☐ to enable it 
  - Then, expand the folder by clicking the [+] button next to it.
- Expand "Application Development Features", then checkmark "CGI".
- Expand "Common HTTP Features", then checkmark ALL boxes.
- Click "OK" to apply changes.</p>
<hr>
<br />
<h3>Installing osTicket</h3>
<p>In order for osTicket to run properly, we are going to need to install the prequisite files onto the virtual machine <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">Here </p>
<img src="https://user-images.githubusercontent.com/142059616/261421222-6f55ac4b-399a-451b-9e26-1ae61b120b92.png" height="60%" width="80%"/>
<p>Select "download all"</p>
<p>First we will install <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> PHPmanagerForIIS</p>
<img src="https://user-images.githubusercontent.com/142059616/261431667-0600c144-fb02-4e74-8390-377985ef7595.png" height="20%" width="40%"/>
<img src="https://user-images.githubusercontent.com/142059616/261433135-4181c4ea-77ec-460c-9de7-6a967516f7c7.png" height="20%" width="40%"/>
<p>Next we will install <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">rewrite_amd64_en-US.msi</p>
<img src="https://user-images.githubusercontent.com/142059616/261435729-5cc88c16-b889-4671-b7ca-e97474835948.png" height="20%" width="40%/>
<img src="https://user-images.githubusercontent.com/142059616/261917312-e1f4e8e2-b50a-4a3a-96ad-2a5470922498.png" height="20%" width="40%"/>
<p>Next we are going to create a directory</p>
<ul><li>Open Windows C:\ on File Explorer</li>
  <li>Right click on the empty space</li>
<li>Select new --> Folder to create a blank new folder</li>
<li>Name the folder "PHP"</li></ul>
<img src="https://user-images.githubusercontent.com/142059616/261918932-5f51b4a8-9692-4044-9bef-fb2aaf91cb99.png" height="55%" width="60%"/>
<img src="https://user-images.githubusercontent.com/142059616/261919280-a67ad0ff-0a63-418f-a59e-ec903601bb02.png" height="55%" width="60%"/>
<p>Next, download <a href"https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">php-7.3.8-nts</p>
<p>Right click on the file, select "extract all"->"browse"->find the "PHP" folder-> select "Extract"</p>
<img src="https://user-images.githubusercontent.com/142059616/261921223-9ef54520-e3dd-4900-a872-6dc674af74b0.png" height="55%" width="60%"/>
<img src="https://user-images.githubusercontent.com/142059616/261921333-7c884ac2-f167-47e1-8a5b-d5f9d126ca01.png" height="55%" width="60%"/>
<p>Install <a href="https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">VC_redlist.x86.exe</p>
<img src="https://user-images.githubusercontent.com/142059616/261925385-293be6ee-bdb7-4468-914a-13efd10c1e0b.png" height="55%" width="60%"/> 

- Next, install <a href="https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view">mysql-5.5.62-win32.msi</a> (MySQL v5.5.62).
- Agree to the License Agreement, then click "Next".
- Click "Typical".
- Once that's complete, click "Finish".
<p align="center">
<img src="https://i.imgur.com/KE9Nf9j.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>

- Another window prompt will appear, just click "Next".
- Click "Standard Configuration", then "Next" twice (leaving everything by default).
- Create a password of your choice for the root login, then click "Next".
- Click "Execute" to start the configuration process.
- Once completed, click "Finish".
<p align="center">
<img src="https://i.imgur.com/J6sJ3D5.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/TYXyZre.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/NeKMEJo.jpg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h3>&#9315; Register PHP within IIS</h3>

- Press the Windows Key/Button and search for "Internet Information Services (IIS) Manager", then "Run as Administrator".
- Double-click "PHP Manager".
- Under PHP Setup, click on "Register new PHP version".
- Click on the 3-dots "..." to browse for `php-cgi.exe`, located inside the PHP folder on the C:\ drive.
- Once you find it, click "Open" (or double-click the file), then "OK".
<p align="center">
<img src="https://i.imgur.com/ZUbY9fi.jpg" height="20%" width="20%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/5vkhmRw.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/cvrfkk5.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h3>&#9316; Installing osTicket: Support Ticketing System</h3>

_Now we are ready to install osTicket!_
- Download <a href="https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">osTicket-v1.15.8.zip</a> (osTicket).
  - Open the .zip file (no need to extract all).
- Open another File Explorer window and navigate to **C:\inetpub\wwwroot**.
- Click and Drag the `upload` folder in the .zip file into wwwroot folder (this will automatically extract that specific folder).
- Rename `upload` to `osTicket`.
<p align="center">
<img src="https://i.imgur.com/caVUV5a.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>

- Return to IIS.
  - On the left sidebar, click "osTicket-VM".
  - Then, on the right sidebar, click "Restart".
<p align="center">
<img src="https://i.imgur.com/RjawCDK.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>

- On the left sidebar, click the dropdown arrow beside "Sites", same thing with "Default Web Site", then click "osTicket.
  - _The icons in the center window should change._
- On the right sidebar, click "Browse *:80 (http)".
  - This will open a new tab on Microsoft Edge to the osTicket Installer page.
<p align="center">
<img src="https://i.imgur.com/xnYfiBb.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Iyh6UO2.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>

_Note that some of the recommended extensions are not enabled, so this will need to be addressed:_
- Return to IIS, still under osTicket folder on the left sidebar, double-click "PHP Manager".
- Under PHP Extensions, click "Enable or disable an extension".
<p align="center">
<img src="https://i.imgur.com/rJNHqxf.jpg" height="30%" width="30%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/ao3rSMH.jpg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>

- Find the following below, then click "Enable" on the right sidebar:
  - php_imap.dll
  - php_intl.dll
  - php_opcache.dll
- Refresh the osTicket webpage to observe the changes.
  - _APCu Extension & Zend OPcache Extension should be the only two with a Red X._
<p align="center">
<img src="https://i.imgur.com/lJLsKOa.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>

- Return to the wwwroot folder in File Explorer.
  - Navagate to **...wwwroot\osTicket\include**.
  - Find `ost-sampleconfig.php`, and Rename it to `ost-config.php` (essentially removing the word sample).
<p align="center">
<img src="https://i.imgur.com/N3FLLaY.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>

_For demonstration purposes, we are going to temporarily give every user the permissions to access the `ost-config.php` file._
- Right-click the file and select "Properties".
- Click the "Security" tab at the top, then click "Advanced" at the bottom for special permissions.
<p align="center">
<img src="https://i.imgur.com/iPPcbIV.jpg" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/V1EmJ2w.jpg" height="30%" width="30%" alt="Disk Sanitization Steps"/>
</p>

- Next, click "Disable inheritance".
- When the prompt appears, click "Remove all inherited permissions from this object".
  - _The middle box should no longer have any principals, so we'll need to add one that includes everyone._
- Click "Add".
<p align="center">
<img src="https://i.imgur.com/8RaZ9Sn.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>

- At the top, click "Select a principal".
- In the object name box, type in "everyone", then click "Check Names" (it should automatically assign it to **Everyone**).
- Press "OK", then click the checkmark to enable "Full Control".
- Press "OK" until all properties windows are closed.
<p align="center">
<img src="https://i.imgur.com/8WWGxGN.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>

_Now we can continue setting up the osTicket installation._
- Install <a href="https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe">HeidiSQL v12.3.0.6589</a> (Heidi SQL).
  - Accept the agreement, then keep clicking "Next", then "Install".
  - Once done, click Finish to launch the program.
<p align="center">
<img src="https://i.imgur.com/8Ya2O7l.jpg" height="150%" width="150%" alt="Disk Sanitization Steps"/>
</p>

- In HeidiSQL, click "New" at the bottom left.
- Enter the username **"root"**, and the password you created when installing MySQL.
- Click "Open".
<p align="center">
<img src="https://i.imgur.com/MRTC33j.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>

- Right-click "Unnamed" on the left sidebar.
  - Select "Created new" > "Database".
- Type in the name "osTicket", then click "OK".
<p align="center">
<img src="https://i.imgur.com/ULeJErY.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>

- Return the osTicket Installation webpage, click "Continue".
- Under System Settings section:
  - Create a Helpdesk Name of your choice (this example uses **OST Help Desk**).
  - Create a Default Email of your choice (this example uses **ost@helper.com**).
- Under Admin User section, create the appropriate credentials of your choice (example below):
  - **First Name:** ost
  - **Last Name:** user
  - **Email Address:** ostuser@email.com
  - **Username:** ostuser
  - **Password:** Password1
- Under Database Settings section:
  - Enter MySQL Database name that was created in HeidiSLQ (**osTicket**).
  - Enter MySQL Username (default is **root**).
  - Enter MySQL Password (Password you created when installing MySQL).
- Once completed, click "Install Now".
  - _You should then be sent to a Congratulations! page, if no errors._
<p align="center">
<img src="https://i.imgur.com/1GQbv9n.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/sfmeeK5.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h3>&#9317; Clean Up</h3>

- Return to File Explorer and navigate to "C:\inetpub\wwwroot\osTicket\".
- Find and Delete the `setup` folder.
<p align="center">
<img src="https://i.imgur.com/6oY0tWK.jpg" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>

_Now we need to reset the permissions of the `ost-config.php` file to read-only to prevent any accidental edits._
- Navigate to "C:\inetpub\wwwroot\osTicket\include".
  - Right-click on `ost-config.php` file, then select "Properties".
  - Select "Security" tab, click "Advanced".
  - Select "Everyone" principal in the center box, then click "Edit".
  - Uncheck "Full Control", "Modify", and "Write".
  - Press "OK", "Apply", then "OK" to close the window.
<p align="center">
<img src="https://i.imgur.com/BIdXCox.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/bQsRfR0.jpg" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h3>&#9318; Testing The Login Services</h3>
Help Desk Login Page: <a href="http://localhost/osTicket/scp/login.php">http://localhost/osTicket/scp/login.php</a></br>
End User Ticket Page: <a href="http://localhost/osTicket/">http://localhost/osTicket/</a>

- Copy the URLs and open them in Microsoft Edge.
<p align="center">
<img src="https://i.imgur.com/mQYjqoF.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<hr>



