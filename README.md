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


















