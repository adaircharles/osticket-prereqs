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

<h2>Installation Steps</h2>


<p>
I created a Windows 10 VM on Azure which we will use to install and set-up osTicket. The next step, in order to reach the web server was to install IIS with CGI enabled. Next, I installed PHP Manager for IIS, the Rewrite Module, VC_redist, and MySQL (And subsequently set it up, using the credentials root/root. I created the directory C:\PHP and extracted the php folder from our osTicket installation files into the newly created directory.
</p>

![creating vm](https://github.com/user-attachments/assets/4b25e497-8ce1-48a7-b0ae-56c1c3453bf9)
![enabling IIS with CGI](https://github.com/user-attachments/assets/96234643-2680-487b-8f96-006edbfc6a51)
![installing sql and creating php folder](https://github.com/user-attachments/assets/c4f35aad-af90-4069-a6b8-83d2e5396ca4)

<br />

<p>
My next step was to register PHP within IIS ran as an administrator before reloading IIS and installing osTicket. I unzipped the osTicket zip file and copied the "upload" folder into the file path c:\inetpub\wwwroot and renamed "upload" to "osTicket". After reloading IIS once more, in the osTicket PHP Manager, I enabled a few extensions that were disabled by default.
</p>

![Annotation 2025-03-20 153943](https://github.com/user-attachments/assets/d61418e3-402f-4bfb-a118-bea39ecc985e)
![Annotation 2025-03-20 154350](https://github.com/user-attachments/assets/8a8982f8-74d2-485b-b569-c11d1242cfa8)


<br />


<p>
The final step was to install Heidi SQL, create and connect to a new session root/root and create a database "osTicket", then after configuring our osTicket installation making sure to name the MySQL database the new "osTicket" and our other credentials, I finished the install and confirmed that it was working correctly.
</p>

![Annotation 2025-03-20 155128](https://github.com/user-attachments/assets/5dac6bc4-ea15-4963-af55-86b56a70d15b)
![Annotation 2025-03-20 155150](https://github.com/user-attachments/assets/01bc0052-2ab4-43b6-9112-cfa46ccbb507)
![Annotation 2025-03-20 155251](https://github.com/user-attachments/assets/179c44ee-e41e-49f7-be3c-538ccdc9a8fa)


<br />
