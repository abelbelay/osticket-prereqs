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

<h4>Create a Resource Group</h4>
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
<h4>Creating A virtual Machine</h4>
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

<h4>Connect Virtual Machine using RDP(Remote Desktop)</h4>
<p>
<img src="https://user-images.githubusercontent.com/142059616/261189115-201883b4-1284-4a97-b5d4-72a9067f8dd8.png" height ="50% "width="80%" alt="Remote Desktop"/>
</p>

<p>
Go to the virtual Machine that was just created and copy the Public IP address .
</p>
<img src="https://user-images.githubusercontent.com/142059616/261189891-ff074ff6-952e-4eb5-b53f-a45ba5e5172a.png" height ="20% "width="80%" alt="Remote Desktop"/>
<img src="https://user-images.githubusercontent.com/142059616/261190125-4e63b3f8-e606-4111-870b-ece0d3e4d559.png" height ="50% "width="80%" alt="Remote Desktop"/>




<p>Open the remote desktop application</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
