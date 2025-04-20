# osTicket Prerequisite and Installation
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

- osTicket Installation files 
- Heidi SQL
- Azure Virtual Machine

<h2>Installation Steps</h2>

![image](https://github.com/user-attachments/assets/f148c728-8f42-4470-b2e5-cf92e358f4b8)
<p>
Create a resource group in Microsoft Azure called osTicket. Then, make a virtual machine inside that group. Use a Windows 10 Pro image for the virtual machine, and make sure it has at least 2 vCPUs. This VM will be used for practice.
</p>
<br />

![image](https://github.com/user-attachments/assets/6a368591-f067-4720-b8ee-42772970dc16)

Next, connect to the VM using **Remote Desktop Protocol (RDP)**. To do this, go to the **Azure portal**, find the **Public IPv4 address** of the VM, and copy it. Then, use that IP address to start the RDP connection.

![image](https://github.com/user-attachments/assets/f3cbb380-d11b-437f-8f49-5a920c3114df)

Next, you will want to download https://drive.usercontent.google.com/open?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD. This will ensure you have the file on your remote desktop. This will help you stay organized as well as make the process easier when looking for and creating new files. Once you have the file downloaded in your library. Continue to place the file on your desktop.

![image](https://github.com/user-attachments/assets/eef23dcd-ec7d-48bd-bd90-707b48184e72)

Following, you will want to open your settings on your remote desktop and go to the control panel. Go to uninstall a program. You will be using this to install certain programs needed. Add internet information services (IIS). Followed by worldwide services, then expand application development features and make sure CGI is included. 

![image](https://github.com/user-attachments/assets/21c5c7f5-dce0-46c0-81ec-8ec4d9740063)

Prior to making sure CGI is included. The next step will be to install PHP Manager using the osTicket file we have on our remote desktop. 


