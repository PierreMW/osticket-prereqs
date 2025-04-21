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

![image](https://github.com/user-attachments/assets/ee8d2866-239d-4f55-8528-9322e4b2e1d5)

Within the same file that we downloaded PHP. It is also mandatory that you install the rewrite module. 

![image](https://github.com/user-attachments/assets/060b94c9-0f5b-4db9-9ae8-214044bf5c43)

Then you will go to your library and create a new folder under your C drive and title it 'PHP'. This new folder will be for the documents for the osTicket files.

![image](https://github.com/user-attachments/assets/abdaeeb8-a786-44cc-a750-2d42dbd51e79)

![image](https://github.com/user-attachments/assets/c4b23947-deee-4f17-94e2-a62b1be42f66)

![image](https://github.com/user-attachments/assets/ea9dae0e-b40d-4dbc-86bf-3da1d3a03e8d)

![image](https://github.com/user-attachments/assets/0534cb7f-7bbb-4305-b89b-927e8cf92914)

Next you are going to right click the file php-7.3.8-nts.Win32-VC15-x86 and choose the option to extract all. Browse for where the files will go which is labeled PHP. Once done the files from php-7.3.8-nts.Win32-VC15-x86 should now be in PHP.

![image](https://github.com/user-attachments/assets/c97c7c8a-0e2f-47b6-bdb5-dd7e272862c4)

Following that, install VC_redist.x86.exe from the osTicket installation folder to ensure the  Visual C++ Redistributable components are in order.

![image](https://github.com/user-attachments/assets/9aa412e8-3274-488f-9a54-d945675ef58e)

Next step is to install the file mysql-5.5.62-win32 from the installation folder. Sequel will help maintain and store all data. For instance user accounts, ticketing information to make sure osTicket runs proficiently. 

![image](https://github.com/user-attachments/assets/56b838d3-3573-44a0-802a-b8260e0b1d70)
![image](https://github.com/user-attachments/assets/67b1065d-16a3-4ee7-af2f-4e4766b3f9cd)
![image](https://github.com/user-attachments/assets/cf017b29-a78d-4ac8-8ab1-99f1c50a2196)

Then you are going to open IIS as an administrator through the remote desktop. Next look for the option of PHP Manager. Continue to register new PHP version and connect php-cgi to the php manager. Once finished stop and start the system to test.

![image](https://github.com/user-attachments/assets/aec7a3de-3b4d-4cf2-a890-97f4199feda5)
![image](https://github.com/user-attachments/assets/1c02fd7a-f310-49c9-8a5d-6832061d9cca)

From the osTicket-installation-files folder. Take osTicket-v1.15.8.zip and copy the upload folder to C:\inetpub\wwwroot. Then, within C:\inetpub\wwwroot, rename the upload folder to osTicket.

![image](https://github.com/user-attachments/assets/0b781aec-2c5e-40fe-b094-5f3a30071a62)

You are going to then sign back into IIS Manager to enable the specific PHP extensions. To get there you will go to IIS through remote desktop > osticket-vm > sites > default web site > osTicket > enable or disable an extension.

![image](https://github.com/user-attachments/assets/eb65b86e-b5e3-4406-8e4b-6963175dd3a0)

Once you are here you will enable php_imap.dll, php_intl.dll, and php_opache_dll. Soon after that refresh osTicket server. It should show that the Intl extension is enabled.

![image](https://github.com/user-attachments/assets/2790ac8a-8597-4cf2-be98-4e0c4a990d56)
The next step is to change the title ost-samepleconfig.php and rename the it to ost-config.php in the same directory as wwwroot. Do this by right clicking on the name and choosing rename. 

![image](https://github.com/user-attachments/assets/e011f944-57b6-4b53-8a01-ecac37000203)
Right-click on the ost-config.php file and choose Properties. Go to the Security tab, disable all inheritance, then remove all current permissions, and assign full control to everyone.

![image](https://github.com/user-attachments/assets/076baf32-26f8-429e-92f1-86cd0c7df54c)
Lastly to complete osTicket setup, open your browser and click continue to begin continue. Choose a name for your helpdesk and set a default email address to receive notifications for customer tickets. 









