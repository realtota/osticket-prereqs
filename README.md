<p align="center">
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

- Microsoft Web Platform Installer
- Microsoft Azure Subscription
- Enable Internet Information Services (IIS)
- MySQL
- C++ Redistributable
- PHP Manager
- Configure OS Ticket 

<p align="center">
   </p>

<h2>Installation Steps</h2>

   >**Note**: Make sure to have already created a Azure account as well as have a subscrition 
   
Start at the Azure services homepage, and click on the "Virtual machines" icon which is pointed out in the image below.

![lab1#1](https://user-images.githubusercontent.com/106701068/232634543-81a9c0f1-9dd5-49c0-b81d-7aadeb80cd8d.png)

Once you are on that page click create and select "Azure virtual machine" 
    
![lab1#2](https://user-images.githubusercontent.com/106701068/232634763-71e55c0e-dccc-455f-a623-6e0fc7277362.png)

 >**Note**: It might be beneficial to write down all the usernames and passwords we are going to use because they are very important to remember

Now that you have done that go ahead and fill out these details, make sure to click "Create new" to create a new resource group.
Make sure to select the region that best applies to you, to select "No infrastructure redundacy required", and Security type as standard.
For the Image make sure it is Windows 10 Pro and for size select 2-4 virtual CPUS to ensure you are not troubled with hiccups. Finally create
an Administrator account and make sure to remember your Username and Password, this is important. Now click review and create.

![lab1#3](https://user-images.githubusercontent.com/106701068/232634899-55f26492-2fbb-4364-a32b-54b2e8fe1f07.png)

<br />

It will take some time to create but once it does click on the Virtual Machine you just created and you will see a page like the one below. Now copy the Public IP address

![lab1#4](https://user-images.githubusercontent.com/106701068/233213220-4a147d42-fe7e-4649-a14e-ca3f4c194e4a.png)

Now click the search symbol on your taskbar and type in "Remote Desktop Connection" and click the application. Once it comes up paste the Public IP adress from the previous step into the "Computer" section and click Connect.

<p align="center">
   <img width="305" alt="lab1#5" src="https://user-images.githubusercontent.com/106701068/233213226-bb22408f-e155-486e-8081-68bb425968cd.png">
   </p>
   
 Once you have connected, select "Use a different account" and enter in the administrator account credentials from when you created the virtual machine. Once those are   in click OK and wait for the connection to the virtual machine to be complete. 
   
<p align="center">
   <img width="342" alt="lab1#6" src="https://user-images.githubusercontent.com/106701068/233213269-8778769b-0906-42a3-a1ad-8b1980576fdb.png">
   </p>
   
  As you enter the homescreen of your virtual machine go to the control pannel and select the "Uninstall a program" under the program section. Once you are there click the shield that says "Turn Windows features on or off".
  
![lab1#7](https://user-images.githubusercontent.com/106701068/233213276-56c8abd1-102d-40ef-8321-087a7c6b7e7a.png)

Clicking that will show a tab that looks like the image below, select "internet Information Services",then "World Wide Web Services", then application Development Features, and finally select CGI and hit OK.

<p align="center">
   <img width="349" alt="lab1#8" src="https://user-images.githubusercontent.com/106701068/233213283-12b53b59-3527-481d-a173-6a61a18907e6.png">
   </p>
   
 From here open this link https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 and download the packets that say "PHP Manager", "Rewrite Module", "PHP 7.3.8","VC_redlist"," MySQL". Open File Exploerer and go this This PC > Windows(C:) and create a folder called PHP. Now extract PHP 7.3.8 and put it into this folder. Now open all the other files we just downloaded and install all of them. 
   
 >**Note**: For the MySQL installation, for setup type select "Typical", "Standard Configuration", and keep everything else the same. Make sure you remember the password 
   
<p align="center">
   <img width="643" alt="lab1#9" src="https://user-images.githubusercontent.com/106701068/233213353-1f5ba2a9-0550-4153-a085-2652c79c6651.png">
   </p>
   
 Now click on the start and type in IIS for the Internet Information Services Manager app and run it as a administrator, from here you can see teh PHP manager and the URL Rewrite that we just installed. Click the PHP manager and click Register new PHP version.
   
![lab1#10](https://user-images.githubusercontent.com/106701068/233213360-1c5e0203-e826-455e-b620-c8798bde5620.png)


  Select the php-cgi file like the one below. It should be stored in This PC > Windows(C:) > PHP > php-cgi, select that file at click OK. Go back to the IIS homepage and click the green Restart button on the top right of the tab.

![lab1#11](https://user-images.githubusercontent.com/106701068/233213371-736222bf-58cf-4dfb-9095-57711634685c.png)

   Download OSTicket from here https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6, insdie that download there is a file called "upload" as  you see below, you want to drag that folder to the location to the right, whick is This PC > Windows(C:) > inetpub > wwwroot and wait for the file to copy. After it has successfully copied, rename that file as "osTicket"

<p align="center">
  <img width="1023" alt="lab1#12" src="https://user-images.githubusercontent.com/106701068/233213382-5249682b-e7f3-431e-b4cf-9374b95bb82b.png">
   </p>
   
 ![lab1#13](https://user-images.githubusercontent.com/106701068/233213402-855e3819-71d2-4b6a-bf72-516159804255.png)
 
<p align="center">
   <img width="615" alt="lab1#14" src="https://user-images.githubusercontent.com/106701068/233213414-88b5ee40-5fc6-4286-b758-6e11b2a3ac8f.png">
   </p>

![lab1#15](https://user-images.githubusercontent.com/106701068/233213424-7be7fb7a-3833-4d65-a663-bf0bd6106fb6.png)

![lab1#15](https://user-images.githubusercontent.com/106701068/233213424-7be7fb7a-3833-4d65-a663-bf0bd6106fb6.png)

<p align="center">
   <img width="542" alt="lab1#17" src="https://user-images.githubusercontent.com/106701068/233213459-11cace6f-42c4-4517-a54e-23518d5b03f6.png">
   </p>
   
![lab1#18](https://user-images.githubusercontent.com/106701068/233213470-af54f67a-b435-49cc-9607-149778d4cd5a.png)

![lab1#19](https://user-images.githubusercontent.com/106701068/233213480-76f4820d-00d5-420a-bc0f-67dcffaf7334.png)

<p align="center">
   <img width="616" alt="lab1#20" src="https://user-images.githubusercontent.com/106701068/233213490-27d5a04a-7f86-42b2-9cf6-1f8a3dadd0c9.png">
   </p>
   
![lab1#21](https://user-images.githubusercontent.com/106701068/233213498-99c62727-7bdd-494e-8500-46283d9f247c.png)  

![lab1#22](https://user-images.githubusercontent.com/106701068/233213528-8464a219-187a-4a6b-84b4-4599b4031f17.png)

<p align="center">
   <img width="238" alt="lab1#23" src="https://user-images.githubusercontent.com/106701068/233213553-4264613e-6283-4e84-b095-e9f33ddc7462.png">
   </p>
<p align="center">
   <img width="610" alt="lab1#24" src="https://user-images.githubusercontent.com/106701068/233213661-28f308cc-9786-4a37-b05a-22fbca232afb.png">
   </p>
   
![lab1#25](https://user-images.githubusercontent.com/106701068/233213701-39dbe33f-4d03-45fd-939e-6d1362931234.png)

![lab1#26](https://user-images.githubusercontent.com/106701068/233213714-aaf1fc6c-0971-4271-a6e9-8f760259802c.png)




