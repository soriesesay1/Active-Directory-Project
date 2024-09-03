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

We create new index because we did not see our scripted index
![image](https://github.com/user-attachments/assets/f1e31c35-62f4-4eac-be12-a6fcba5f0f48)

We enable our Splunk Server to receive data by clicking on Settings and Forwarding and receiving
![image](https://github.com/user-attachments/assets/176f58f0-7083-47f5-acae-b83e5207a6a6)

Click configure under Receive Data and click on New receiving Port at the top right
![image](https://github.com/user-attachments/assets/e24b239a-e6d3-4b35-ba02-6305703a3afd)
![image](https://github.com/user-attachments/assets/d29d4381-0442-4eeb-b681-0663ea1dcdaf)

Default = 9997 and Save
![image](https://github.com/user-attachments/assets/402b9bd4-f2bb-4820-93d0-093cfd064a03)
![image](https://github.com/user-attachments/assets/d86fd9d7-5e14-4bf4-9a9a-b3e0d0f15861)

To see if data coming in from our target machine, click on Apps, and select Search & Reporting
![image](https://github.com/user-attachments/assets/9aff9040-331b-4a81-bdf0-a05fb3e40c8f)

Type in ‘index=endpoint’ and click on search
![image](https://github.com/user-attachments/assets/aad4cbc6-4965-4fc4-bd88-a3fe2f08e1c1)

We see some events and 1 host machine which is our machine (target-PC)
![image](https://github.com/user-attachments/assets/aa948a52-cfa3-4abe-bf37-c21d027031f1)

Our input.conf files
![image](https://github.com/user-attachments/assets/069e2f38-b1fb-4b4f-a5f1-4bd2b95bc2dc)
We successfully install & configure Sysmon and Splunk. Success!

# Part 4:
Is to install and configure Active Directory on our Windows 22 Server and move it to a domain controller and configure the target machine to join our new domain.
![image](https://github.com/user-attachments/assets/2bfea06b-01a0-4992-a593-b6889ca924a1)

We give our windows server 22 a static IP and press okay to save it
![image](https://github.com/user-attachments/assets/c449479f-75b5-49ec-8f3a-bbdabb8dc135)

Open the command prompt to verify the IP address has been change and ping google.com to verify we have a connection. We also ping our splunk server to know if we have a connection.
![image](https://github.com/user-attachments/assets/613dc76c-b5d6-4095-a2f8-2e29031d27df)

Now we add our roles by clicking on Manage at the top. Follow the steps below.
![image](https://github.com/user-attachments/assets/fc6f01fd-9696-4748-94cd-a191a65ab486)
![image](https://github.com/user-attachments/assets/e0b23319-eb9f-4a73-b360-7ce5781ae5cf)
![image](https://github.com/user-attachments/assets/89cf04ba-0ace-4989-809f-9c574d7042c2)

Select Active Directory Domain Services and click on Add Features
![image](https://github.com/user-attachments/assets/70789f9f-578c-4960-a376-9eb63845368d)
![image](https://github.com/user-attachments/assets/41bacd13-3ac3-4308-8ae0-2f2fbd484818)

Click next until install and close when the installation is complete.
![image](https://github.com/user-attachments/assets/d63b0cbb-2702-451a-b9d9-69e41e93594e)

Click on the flag at the top and select ‘Promote this server to a domain controller.’ In the deployment configuration, select ‘Add a new forest’ because we are creating a new domain
![image](https://github.com/user-attachments/assets/44033c76-b531-49ff-9b59-034eded70a3f)
![image](https://github.com/user-attachments/assets/ccd1573d-fc69-4ba5-86ad-5f493b963047)

Leave everything on default except for password creation and click next.
![image](https://github.com/user-attachments/assets/cd596c45-582d-4de5-9db5-d74a07a83fb9)
![image](https://github.com/user-attachments/assets/d2ea3fb1-2ae4-4002-a165-a995793a36ad)
![image](https://github.com/user-attachments/assets/904a8464-d70a-4d72-a380-dfd7dfee9779)

After Prerequisite Check, click Install. And the server will automatically restart. 
![image](https://github.com/user-attachments/assets/24040a42-762d-4c95-9ff1-a81b3608fc58)

Login to the server we just created, and it may look like this below. This shows our server was a success!
![image](https://github.com/user-attachments/assets/c5b08b74-7cde-4a54-91dc-66e956830a27)

# Create Users on our Domain:
On Tools, select Active Directory Users and Computers
![image](https://github.com/user-attachments/assets/fc7a87e2-73e8-4897-879c-38072da528a0)
![image](https://github.com/user-attachments/assets/ad573925-2c04-474d-a1bb-8b9cb125549b)

In our local domain, we created an ‘Organizational Unit’ for IT & HR and added Users in both. To do this, you have to right click on your local domain.
![image](https://github.com/user-attachments/assets/2d75e696-804b-4ecb-8823-66e4d9f637ca)
![image](https://github.com/user-attachments/assets/9cb47470-9cd9-46d3-b42c-a623069e3cc7)

After setting up our Active Directory and the server is now a domain controller, we must now join our windows target machine into our new domain called dcyber.local and authenticate using one the Users.

On our target machine ‘windows 10’ search for This PC and click on Properties. In properties, scroll down to Related Settings and click on Advanced System Settings. Inside system, click on Computer Name and select change. Inside Computer Name/Domain Changes, select Domain and type in our domain (dcyber.local)

![image](https://github.com/user-attachments/assets/f561eb0a-7d1d-436b-9db1-f3b579f49af0)
![image](https://github.com/user-attachments/assets/71767002-7d91-4b26-b313-e7026086f315)

We have an error and to fix this, we go to our network settings
![image](https://github.com/user-attachments/assets/c52a667b-357f-4579-8d9e-b09368399467)

In the network settings, select Change adapter options, right click on the Ethernet, select properties and double click on Internet Protocol Version 4 (TCP/IPv4)
![image](https://github.com/user-attachments/assets/f28a97a5-10b8-42fa-9531-631026e15890)

Our DNS was set to google and that’s the reason for the error. We change it to our domain DNS and click
![image](https://github.com/user-attachments/assets/7bfc658c-ab8b-4089-a989-4bc2182a3554)

Verify everything went well by typing cmd (command prompt) and inside type ipconfig space /all and hit enter. This shows our DNS is on our domain.
![image](https://github.com/user-attachments/assets/103679d5-6ad4-4374-bd98-b07a9a026121)
Success! We are able to join our domain. Username type administrator and the password you used. You will be prompted to restart the computer

![image](https://github.com/user-attachments/assets/4ae6f29a-3919-49f1-a38e-4c4f52af39ff)
![image](https://github.com/user-attachments/assets/988dcc79-8738-4464-8fa4-229b824d9a21)

To make sure everything is correct, we have to sign in with our User (jsmith) that we created in the .local domain. Verify you are signing in to your domain (dcyber)
![image](https://github.com/user-attachments/assets/959f885b-b3c8-49b6-bb84-b3985f7bc3d2)
Success! We created 2 Users and configure Active Directory.

# Part 5 Final:
We learn how to use Kali Linux to perform a brute force attack on our users in Active Directory and use splunk to query the activities. We also learn how to install Atomic Red Team to run a test and generate telemetry to detect similar attacks in the future

# Power Up Kali:
![image](https://github.com/user-attachments/assets/3dd07288-09a1-429a-accd-8c6d7f1f18af)

We learn how to setup a static IP address in Kali Linux to 192.168.1.2 just like in the diagram. To do that, we right click the ethernet connection at the top and click ‘Edit Connections’
![image](https://github.com/user-attachments/assets/6df6a55a-f206-4bbb-b6fa-2fb54adfeb3d)

Select the Wired connection 1 and click settings below. Select IPv4 Settings and below where it says Automatic (DHCP) change it to Manual and click Add to enter the IP address and save.
![image](https://github.com/user-attachments/assets/020482e5-345b-4824-b35e-73455a253651)

Right click on the desktop and select Open Terminal Here, type in ip a and enter to verify the static IP 
![image](https://github.com/user-attachments/assets/5acb79b3-7703-475a-8a22-b83444bb20ab)

If the IP didn’t change, disconnect the internet and reconnect it again. We ping google for connections.
![image](https://github.com/user-attachments/assets/55f33e3f-e761-4f07-8464-8e21137e1409)

Ping our splunk server for connection:
![image](https://github.com/user-attachments/assets/1f52ef62-43cd-47bb-940d-c655d41bca4a)

Update our kali:
![image](https://github.com/user-attachments/assets/4e8d65e5-793c-43ed-a9f5-9b32be86c8a1)

We are creating a directory on our desktop for all our files 
![image](https://github.com/user-attachments/assets/b18cee0d-879a-4ded-8de8-b2d280e35487)

We install crowbar to perform brute force attacks
![image](https://github.com/user-attachments/assets/889a2d92-4184-4cb8-b833-bc34a18861a6)
![image](https://github.com/user-attachments/assets/540d2785-7779-4409-8bfe-637613a100a4)

We unzip rockyou file and copy it to our desktop 
![image](https://github.com/user-attachments/assets/51ed5708-8302-4dc8-adef-21fc2af1745d)
![image](https://github.com/user-attachments/assets/c6ee56dc-855f-4a75-ac57-e1db30e25023)
![image](https://github.com/user-attachments/assets/3d39732f-4692-4f32-a891-97bd86319e49)

To enable remote desktop in our target machine and make sure the ADministrator is type like this. After that, go to the Remote tab and select ‘Allow remote connections to this computer’ and click Select Users. Click Add in the Remote Desktop Users and type in the Users we created before, just like this
![image](https://github.com/user-attachments/assets/37d5f57c-ce60-4695-92b8-bb74ac0341f0)

After that, click on okay, Okay, and Apply and Okay.
![image](https://github.com/user-attachments/assets/65ce31e7-2cd6-49d6-a4e8-b1b731a0379e)

Here we are testing our Remote Desktop Access to one of our User with a specific IP target.
![image](https://github.com/user-attachments/assets/d205557f-c5a7-47d1-98eb-b7c30a9b1923)

# For some reason, mine didn’t get the password from the User. We are going to splunk to see if we generate any telemetry.

In splunk, select Search & Reporting and type in index=endpoint tsmith and select last 15 minutes
![image](https://github.com/user-attachments/assets/b7cd8cdc-65cc-414a-90df-ffa58992d827)

After the search, we notice that we have 21 events generate.
![image](https://github.com/user-attachments/assets/8ef51e46-68c6-445a-8ff3-ec3fe0eb4e85)

We have 1 EventCode during our attempted rdp (Remote Desktop Attempt) and the value is 4625 and count is 21. 
![image](https://github.com/user-attachments/assets/78997240-0349-4c81-b6aa-57adae36d0fc)

4625 means a failed log on ID when we google it. 21 means 21 attempt to log on.
![image](https://github.com/user-attachments/assets/ebfc4cc2-29ac-40fd-8f22-edfac6901e12)
![image](https://github.com/user-attachments/assets/1cb0b77c-94ff-47ce-9eb6-8cdc46a3ef70)

For some reason we didn’t have any Events for the last 15 minutes and we try the 60 minutes and we do have query.
![image](https://github.com/user-attachments/assets/21d0de2a-3a2a-4f54-879e-692f5523207a)

We try EventCode 4624 and we have no query meaning there was no successful log on.
![image](https://github.com/user-attachments/assets/71294a48-f9b1-4876-936f-dff56eb89230)

Inside our query, we check to see who and where was the log on attempts coming from and their IP
![image](https://github.com/user-attachments/assets/781524a3-6a35-4301-9dfd-861036436418)

Now we install Atomic Red Team on our Attack machine using PowerShell. To do that we type PowerShell on the search bar and run as an administrator to open. 
![image](https://github.com/user-attachments/assets/3825c564-d807-4d97-a2a9-0a68472325ac)

You will be asked for the Administrator account and password.
![image](https://github.com/user-attachments/assets/558e7726-b193-4e3a-8aaf-0bec998c2827)

Before we install the atomic framework, we need to exclude the entire C drive because Microsoft Defender might stop us and not let the complete package to install. To do that, we go Windows Security and click on Virus & threat Protection, inside click on Virus & threat Protection manage settings
![image](https://github.com/user-attachments/assets/187add8b-3b82-4e22-8610-dd54d73bd0f0)

Scroll down and under Exclusions, click on ‘Add or remove exclusion’ and for some reason, I was asked to sign in with my administrator privileges. 
![image](https://github.com/user-attachments/assets/e40c2c79-5ca6-495f-b0fe-e3c790852ffc)

Inside Exclusions, click on Add an exclusion and select folder. Inside, click on This PC and select Local Disk (C)
![image](https://github.com/user-attachments/assets/2e06c924-6347-4648-bd43-f9b9bd46a508)
![image](https://github.com/user-attachments/assets/c383a709-3e64-4c02-9b40-115a21243082)

It will look like this below.
![image](https://github.com/user-attachments/assets/2c5ca3b9-30ef-4eb0-a1fc-351c967f0ebc)

Now we go back to PowerShell to install Atomic Red Team. There were some roadblocks, but we fix it
![image](https://github.com/user-attachments/assets/c788b2c9-184a-4aa0-b127-d45b4771bb87)
![image](https://github.com/user-attachments/assets/1848a723-22d7-4c67-8ecc-41e0df8230a5)

# All these codes are in the MITRE Attack frame to give us a clear understanding of what we are doing, just hover above them. 
For Example: T1136.001, T1136.002, T1136.003 in Atomic Red Team
In MITRE Attack: T1136.001 is a Local Account, T1136.002 is a Domain Account, and T1136.003 is a Cloud account. 
![image](https://github.com/user-attachments/assets/544e5a31-ed6c-4786-b011-9cec53288687)
![image](https://github.com/user-attachments/assets/454f4e8e-155f-4d0e-9084-797f2918a577)

We Invoke T1136.001 and the result is below. This also will generate telemetry because of the local account created.
![image](https://github.com/user-attachments/assets/fd17cb9d-e629-4175-aad1-89954dc40b46)

In splunk, we have a telemetry that generate event codes from our atomic red team created using PowerShell. This shows we can see any local account created in our system/computer.
![image](https://github.com/user-attachments/assets/158a26fe-fce7-465a-a0d4-9da007cd31fd)

Another Example: - T1059 which is Command and Scripting Interpreter
![image](https://github.com/user-attachments/assets/2d91139e-7971-4478-805d-9707c363ba7c)

From the look of things, it looks like Windows Defender is picking up the T1059.001 PowerShell. We did see 209 events of PowerShell in our splunk for the last 15 minutes
![image](https://github.com/user-attachments/assets/6ba3ad69-aab0-49b4-a649-69ba25f5152f)
![image](https://github.com/user-attachments/assets/e97b364e-7d3b-47da-a57d-d9fc86a655d4)

Congratulations dcyber! You have successfully completed the Active Directory Project!

A Big Thank You to MyDFIR on YouTube for this project. I appreciate you alot!  


