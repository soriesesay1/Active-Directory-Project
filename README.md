# Active-Directory-Project
My-Active-Directory-Home-Lab-Project-With-MyDFIR-YouTube

What is Active Directory? This link will explain better https://www.quest.com/solutions/active-directory/what-is-active-directory.aspx

In this lab, we will learn how to set up Splunk, Kali Linux, and Atomic Red Team as part of this Active Directory project (home lab). We will also look at how a domain environment works and how to send events logs to our Splunk (SIEM) and make data about attacks seen in the wild to help you find them. This home lab has 5 parts.

# Part 1:
We learn how to draw the diagram for our lab (project) using a site name draw.io and below is the outcome.

Diagram:
![image](https://github.com/user-attachments/assets/490b2a59-f539-4648-a02e-5e9c258e66f9)

# Part 2:
We spend time on how to download and install our virtual machines in VirtualBox. Machines included: -Windows Server 2022, -Windows 10, -Kali Linux, -Ubuntu Server (Splunk)

VirtualBox Settings
![image](https://github.com/user-attachments/assets/22a544a9-b829-4a9e-979f-ea8b43b7077b)

For the Hardware, it depends to how many gigs you have in your laptop and as for me I have 32. 
![image](https://github.com/user-attachments/assets/c5fe655d-a84a-41ba-b05c-6fb2942a7f83)

For the virtual hard disk, 50.00GB should be fine.
![image](https://github.com/user-attachments/assets/4989d7cc-c2b1-429e-8917-4fa3940fa1be)

Click finish!
![image](https://github.com/user-attachments/assets/bc0b2c37-9797-4df9-8f36-f5c3eb8799f0)

# After setting our windows in virtual box, you will click start on the top right and wait for the windows to finish powering up. You will see a window like this below, click Next, and click Install. In the activate windows click on “I don’t have a product key” In the       windows setup, select “Windows 10 Pro” and click Next. Select ‘Custom: Install Windows on (advanced)’ and Next and wait for the installation to complete. 

![image](https://github.com/user-attachments/assets/eb1e4c1a-8042-4c86-97de-aaf83ec25c91)
![image](https://github.com/user-attachments/assets/0ff3e1ef-6f32-4ff0-98fd-974f76a1afc5)
![image](https://github.com/user-attachments/assets/4347dc42-76eb-4449-b6fa-f641f90b7e2a)
![image](https://github.com/user-attachments/assets/2f706af0-07be-4cc5-a482-453ea274ff42)
![image](https://github.com/user-attachments/assets/1556afc6-00dc-449f-a0a9-3b9f68d0ae71)
![image](https://github.com/user-attachments/assets/e538f372-da3c-4b80-bc41-4b88f204c4ae)

Setup windows for personal use and click Next. Windows will ask you for your email before you login and suggestion is for you to click ‘create account’ which will let you just create your name for the machine and a password. 

![image](https://github.com/user-attachments/assets/be2ca5fc-a947-4e3e-9909-da1962a18b79)
![image](https://github.com/user-attachments/assets/22fa002a-b675-4cdd-a82b-e4d245e228c1)
![image](https://github.com/user-attachments/assets/efdb4085-3d10-4b19-b037-899b07abdf35)
![image](https://github.com/user-attachments/assets/7fc90a1f-4f07-4988-98da-238283ddd887)
![image](https://github.com/user-attachments/assets/be2c12ac-e7d2-4be4-ae7d-97f2a20418cf)

# Install Kali:
We go to kali.org, click on virtual machines, 
![image](https://github.com/user-attachments/assets/bd39bff7-703a-4233-8714-d14431454138)

On the Pre-built Virtual Machines, select anyone and for this lab I select VirtualBox because my computer is 64 bits.
![image](https://github.com/user-attachments/assets/bad8f006-3fcf-49b2-ab72-b19ea72135c8)

After the download, you will have a ‘zip file’ like this below and ‘right-click’ to extract all.
![image](https://github.com/user-attachments/assets/1dc99593-98e6-45a9-a0cd-2cb1428c4897)

You will have a file that looks like this below, open it and ‘double-click’ on the ‘blue’ kali which will take you directly to virtualbox and click start with no settings require because it’s per-built.
![image](https://github.com/user-attachments/assets/b59fbfe3-63b1-46cb-bb2b-e051d15cf90a)

Both login and password is kali/kali as default. 
![image](https://github.com/user-attachments/assets/068c7750-4643-4136-aa89-2919632aabc7)

We are in Kali, Success!
![image](https://github.com/user-attachments/assets/f4fd5890-18cc-48e4-ab61-bfd54a727ee0)

# Let’s download and install Windows Server 22:
  Go to google.com and type in windows server 22. It will take you to this Microsoft page
![image](https://github.com/user-attachments/assets/42b54d9c-6532-481c-90b3-c38f49fe04de)
Make your way down and click on ‘Download the ISO’ and you will see a registration form to fill out and go ahead and fill it out your credential. I have already downloaded windows server 22.
![image](https://github.com/user-attachments/assets/76a6aa5b-965d-4505-903c-8fc009334523)
After the download, let’s install it in virtualbox. Since we are following MyDFIR, we want to leave everything as default
![image](https://github.com/user-attachments/assets/519d356a-3c2f-4848-8de3-21ba32f93dec)
![image](https://github.com/user-attachments/assets/0c8b1fb2-92cd-48b7-9e8d-48cd810084ae)
![image](https://github.com/user-attachments/assets/50f1ad60-82de-459e-956d-929933604c3d)

We have a windows like this, click Next and Install. 
![image](https://github.com/user-attachments/assets/e402b624-13d1-481b-8c23-4f595408502c)
![image](https://github.com/user-attachments/assets/65e84250-f6a1-4c6c-aca6-9c8e59bf68cc)
For the operating system, select the ‘Standard Evaluation Desktop Experience’ for a better window and click Next.
![image](https://github.com/user-attachments/assets/2c8530ac-3b6e-4188-ada5-204edf340dd9)
Installation type, we select ‘Custom’ and click next.
![image](https://github.com/user-attachments/assets/654a1aaf-4b13-417e-bffc-6583fa183677)
Wait for the installation to complete
![image](https://github.com/user-attachments/assets/6323bcf5-afc8-4b45-b54c-cb771a2690e2)
Enter your password as admin and click finish
![image](https://github.com/user-attachments/assets/f7b4c517-4a5a-4de0-99d2-33551d5bf152)
You will have a window with no way to open it. On the top, click on Input, Keyboard, and select ‘Insert Ctrl+Alt+Delete’ which will let you put in your password. 
![image](https://github.com/user-attachments/assets/e158b79c-e70e-4b89-a405-ed94a52d3ad3)
![image](https://github.com/user-attachments/assets/3982da3c-c64a-42fb-ad58-b6dcb1ec9f0c)

# Install Ubuntu Server (Splunk):
  To download Ubuntu Server, go to ubuntu.com, hover your cursor over ‘products’ and select Ubuntu Server. Once you are in, click ‘Download Ubuntu Server.’ I have already downloaded it. 
![image](https://github.com/user-attachments/assets/f71ce22e-a141-41e3-b718-074b4cf31cf3)
![image](https://github.com/user-attachments/assets/d81ea93e-cf9a-4a4a-992c-e69b573e3cc8)

Your screen will look like this once you click on download
![image](https://github.com/user-attachments/assets/6a883b62-61be-4a03-bbc7-6fa95f730ade)
After the download is completed, we go to virtualbox for installation
![image](https://github.com/user-attachments/assets/7960c037-225f-4f08-952d-6daea4e2f0e7)
![image](https://github.com/user-attachments/assets/6bc1c5a6-07da-409f-8391-fcd1aeffe9ba)
You can increase this depending your space/gigs on your computer
![image](https://github.com/user-attachments/assets/a702b9d7-769e-4e8e-8d79-d10db32be40d)
![image](https://github.com/user-attachments/assets/7aa9cdfd-9631-420e-a06e-a48246bd5cf0)

After the download and installation, now let’s configure our server. Follow the default instructions/green line
![image](https://github.com/user-attachments/assets/76373ee3-088f-41ba-b9f5-40468dc297c0)
![image](https://github.com/user-attachments/assets/6303c8a5-fc52-425d-9aba-1e0064cf4ba0)
![image](https://github.com/user-attachments/assets/c6ef0fcc-bfeb-48c2-8fc6-9ed82694942e)
![image](https://github.com/user-attachments/assets/58668297-8324-454e-acc3-b8f9ede81a3d)
![image](https://github.com/user-attachments/assets/6d6fbb6c-61c9-45a6-9f6a-9da2198d6f07)
![image](https://github.com/user-attachments/assets/ea5cbda7-4635-46ca-8e20-0e2079d57fbb)
![image](https://github.com/user-attachments/assets/087202f9-cb9d-44f0-aacf-83ff4c92e1cf)

Use the down arrow and hit enter
![image](https://github.com/user-attachments/assets/5b066102-9da4-4a3e-9aaf-fa629eca4c6b)
Your storage configuration will look like this below and click done.
![image](https://github.com/user-attachments/assets/e4738388-e190-428b-9e2e-e597eaf7ec6a)
Use the down arrow to click on continue below.
![image](https://github.com/user-attachments/assets/6014340f-c6ad-454b-906a-eddf1cfbe210)

Profile setup
![image](https://github.com/user-attachments/assets/fe776e8c-bab7-478b-aef2-0b6f37281d1e)
OpenSSH Server is OPTIONAL if you want.
![image](https://github.com/user-attachments/assets/27357e8b-b99b-4193-ac18-6d88da611daf)
Same for these below, OPTIONAL if you want to install any.
![image](https://github.com/user-attachments/assets/26fe675d-1d4c-40e6-a757-ad3a4c757e74)
Give the installation time to complete. Reboot when you see ‘Reboot Now’
![image](https://github.com/user-attachments/assets/c3802d56-00a4-4c5c-afb1-7f80f1645f2c)
![image](https://github.com/user-attachments/assets/760a0f44-c5f5-43ff-b61c-b2c5881aa1ed)

Once login using your password, update the server with ‘sudo apt-get update && sudo apt-get upgrade -y’ and click enter for the update to proceed. Type your password
![image](https://github.com/user-attachments/assets/d2f11864-ae3d-400d-a0fb-dec3489e83ae)

![image](https://github.com/user-attachments/assets/f1610546-9fe1-442c-b138-eb2adbde9a41)

# Part 3:
  We install and configure our softwares: Sysmon(Use for login purpose), Splunk(For alerts and telementry) as the most important of them all. 
![image](https://github.com/user-attachments/assets/031f6220-2150-4356-b0ba-2d3bcfe7bd9b)

We put our network on the same network, select tools on the top and click on the 3 dots top right, and select network. In the ‘network’ select ‘NAT Networks’ and click on create and change the IP address.
![image](https://github.com/user-attachments/assets/d19a7774-cc22-43d5-b30f-77951e2f6314)
In virtualbox, we change the network from NAT to NAT Networks for Splunk and the rest of the machines.
![image](https://github.com/user-attachments/assets/d89ef5c6-0689-4483-a824-77f5f57248d4)

My advice for this Lab is for you to download the Ubuntu Server 22 instead of 24 because when changing the network to static it would not WORK for some reason, I had to uninstall the 24 and install the 22 version before it worked.

Firstly, to know your IP address type IP space a and click enter. You will see MyDFIR dashboard because I completed this part quickly because I thought it is not going to work again. 
![image](https://github.com/user-attachments/assets/f7d549c7-bacc-4f67-ab56-4f25dbb10be8)

To enter the NANO gnu network type in ‘sudo nano /etc/netplan/00-installer-config.yaml’ and hit enter.
![image](https://github.com/user-attachments/assets/ead14ed3-9d7c-4bab-bd6a-b9f14dbcd716)

In the NANO system, your network settings should look like this below. And to save the settings, press Ctrl+X, and then Y and hit enter to save the network settings. And type ‘sudo netplan apply’ to apply the settings
![image](https://github.com/user-attachments/assets/0702b568-5cd9-4d9b-b76a-9ee98a0cc2ea)

You will have a screen like this when applying the network settings
![image](https://github.com/user-attachments/assets/f33f171b-fbff-47f6-9faf-606026855f3d)

Verify if the static IP was successful by typing ip space a and hit enter.
![image](https://github.com/user-attachments/assets/9f60adbb-a864-4443-b8e9-78bd2a57f838)

Splunk:

If you already have a splunk account fine and just sign in and if not sign up and login. Inside splunk, hover on ‘Products’ and scroll down and click ‘Free Trials & Downloads’
![image](https://github.com/user-attachments/assets/19922e69-3398-4d38-935d-e8c739435f7c)

Select ‘Get My Free Trial’ under Splunk Enterprise
![image](https://github.com/user-attachments/assets/e34449b9-9dc2-405d-9eb1-608a268e6984)

Select the Linux Package and download the ‘.deb’ file.
![image](https://github.com/user-attachments/assets/17992aba-f6fc-4be9-8a28-dec9ab6e9898)

Install virtualbox guest
![image](https://github.com/user-attachments/assets/f5d239aa-f5bc-438c-8f1a-0e1894657068)

# Shared Folder:
To access the shared folder, we go to device at the top and scroll down to ‘Shared Folder’ and select ‘Shared Folder Settings’
![image](https://github.com/user-attachments/assets/ec88c04b-ed4c-41cb-8cd7-787bf35824b1)

Once inside, do the following below. For the Path, select where you save your splunk download file.
![image](https://github.com/user-attachments/assets/b7c5dab6-0477-4554-b2ea-c22238a61d84)

Directory Created
![image](https://github.com/user-attachments/assets/967674ca-e02e-44b8-8916-6e2cad8046a9)
![image](https://github.com/user-attachments/assets/59536573-072a-408d-b452-fafd5df68c84)
![image](https://github.com/user-attachments/assets/e32348ad-7e3b-49d1-9dd3-379a06154525)
![image](https://github.com/user-attachments/assets/142f0a3c-dea8-4367-a0ff-42d0f08272c6)


# Windows 10:
On windows, we rename the name to target-PC and set a static IP address.
![image](https://github.com/user-attachments/assets/8a1cec4b-6224-4551-bc9b-85d11d0f8e77)

Right-click on the networking tab and select ‘Open Network & Internet Settings’ for Network Connections to open
![image](https://github.com/user-attachments/assets/6cd17418-0dd0-4881-a58b-c75882a00efb)

On the network status, select ‘Change Adapter options’
![image](https://github.com/user-attachments/assets/00616806-2ac3-4df2-9165-eb06deb5914d)

Right-click on Ethernet and select properties. After that, double click on ‘Internet Protocol Version 4 (TCP/IPv4)’
![image](https://github.com/user-attachments/assets/7a58a00b-dbe0-40c5-886c-20a0e8dbb6bd)

# Static IP:
![image](https://github.com/user-attachments/assets/fc204ce4-f934-4308-9b33-6779c0eecb64)

Splunk:
Access the splunk server on windows using the IP address from the splunk server. IP address: 192.168.10.10:8000
![image](https://github.com/user-attachments/assets/1792bfe8-de5e-4d7a-8a6e-90a362d710a9)

Install splunk universal forwarder:
Go to Product again and click on Free Trials & Downloads. Scroll down to Universal Forwarder and click on download.
![image](https://github.com/user-attachments/assets/e1fd38be-31c3-4d07-8dc0-6d2bc3fa406d)

Once inside, click on the windows download to download.
![image](https://github.com/user-attachments/assets/d85580ff-c5dd-4afe-96a8-3449edf99947)

After downloading Splunk Universal Forwarder, go to downloads on your PC and double click on it.
![image](https://github.com/user-attachments/assets/6b3e9cf2-c0eb-4609-a0fc-71ec83178e7a)

Username: admin and click next
![image](https://github.com/user-attachments/assets/d389c9f6-8ffc-4fe3-a807-044df72c75df)
![image](https://github.com/user-attachments/assets/3a3946b7-f840-4256-bbb1-d5eb54c7f365)
Click Install

# Sysmon Installation:
  Go to google.com and type Sysmon. Click on Sysmon-Sysinternals and click Download Sysmon
![image](https://github.com/user-attachments/assets/f0cf5869-cfd2-434a-b3a6-4bb94ffc2e78)
![image](https://github.com/user-attachments/assets/b4ecca1b-9e7a-4638-ac08-10315fdb5c69)
![image](https://github.com/user-attachments/assets/4ce5e009-bf3a-4172-b68d-e065cf73c948)

We download the RAW page from github.com and save it to our downloads
![image](https://github.com/user-attachments/assets/79a90f84-cf12-4f4f-a25a-d472d305c584)

We open PowerShell with administrative rights to run and install Sysmon 
![image](https://github.com/user-attachments/assets/84b849b7-4bf5-47a0-8a82-996f48526b2c)

We cannot rename the default file ‘input.conf’ in the system of splunk universal forwarder, so we wrote a script in ‘Notepad with admin rights’ and save the file in the local instead of default.
![image](https://github.com/user-attachments/assets/06cca9f2-6936-412a-bcff-b2d8395d801d)

We Restart and Start the Splunk Forwarder in Services for the script to work, and change the account to local 
![image](https://github.com/user-attachments/assets/f34a8290-6d23-40e8-b301-c815204c2503)
![image](https://github.com/user-attachments/assets/d8a018c0-d7f4-469a-8505-b4281047c568)

# Our Splunk Portal:
![image](https://github.com/user-attachments/assets/4dcd93ec-88f4-48aa-a299-d710426d54a6)

We go to Settings at the top and click Indexes for the input.conf ‘EventsLog’ called endpoint we created.
![image](https://github.com/user-attachments/assets/75a57a45-587b-4499-ab88-36c24f927f6d)























































































