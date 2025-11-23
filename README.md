BRG-27-labs

Day 1 updated GitHub
Learned new Linux commands
===
Reflective Learning Journal Template – BRG28-ISEA
Student Name: Tan Jie Ying
Student ID: 35891972
GitHub Repository Link:
1.	Installing a Linux Environment on Your PC
As a class we were represented with the following options:
•	VMWare(https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion)
•	VirtualBox(https://www.virtualbox.org/)
However as we could not register for VMWare we proceeded to install Virtualbox instead.
 
I had faced several issues with VirtualBox that took some time to work around, initially following the default settings, I had been stuck with a black screen upon powering on the system, in order to resolve this I increased the video memory distributed to 256 MB and successfully got to the Ubuntu desktop, however quickly I was presented with another issue, when it was supposed to update and initialize, it froze and hung, and in order to resolve this I increased the distributed RAM to 4GM.

This allowed the system to initialize and update accordingly smoothly, and had faced no issues with stuttering, or hanging, or black screens throughout the remainder of the following activities.

Upon reflection the benefits of utilising a virtual machine are:
•	Efficient resource utilisation, a single computer can run multiple virtual machines, each with it’s own OS and applications.
•	Cost Savings, you don’t need multiple computers to run multiple workloads
•	Isolated environments where you can test new software or OS without risking the main system, if something goes wrong you can delete or reset the VM without affecting the host computer.
•	Virtual machines can be backed up and cloned, and moved between physical systems quickly, making disaster recovery faster and more reliable.
2. Exploring Ubuntu Desktop and CLI Tools
	 
 
To begin, I tested if the internet is working by accessing Firefox on the right dashboard. In order to practice installing via a GUI, I enter the Applications and downloaded LibreOffice and explored the File manager as well. This allowed me to get a better understanding of navigating the GUI of the Ubuntu OS.
Utilising the GUI offers a visual or intuitive way to interact with the system and allows for easy customization for the desktop to suits the needs of the user.
Following that I tried to get a better understanding of the command terminal by practicing basic commands.
Below are the list of commands I had practiced, alongside with a short description and a use case example that I had reflected upon
No	Commands	Description	Use Case
1	ls	List files	Check what files are in your current folder after downloading something
2	ls - la	Show all files	Check if a .config file exists
3	cd fold	Change directory	Go into documents to work on files there
4	pwd	Show current path	Make sure you’re inside the right location in the system
5	ps -e	List processes	Check if there are any background processes that are undesirable
6	top	Live process monitor	See which process is using the most CPU or memory

  
 
 

Below are a list of commands I had practiced for file operations, alongside with a short description and use case example that I had reflected upon
No.	Commands	Description	Use case 
1	touch 	Creates empty file	Setting up a project, and need a placeholder file called README.md before writing content
2	gedit	Edit in GUI editor	Drafting a report with formatting in a GUI editor for easier text styling.
3	nano	Edit in terminal	Logged into a remote server via SSH and need to quickly edit config.cfg without a GUI
4	cat	Show contents	Just downloaded a file and want to see the content inside
5	less	Scroll contents	Trouble shooting and need to scroll through error log without flooding the terminal
6	cp	Copy file	Backing up files
7	mv	Move file	Moving files between folders
8	rm	Delete file	Deleting clutter
 
Checking User Info
 
 





Checking Ip addressing using ip a
 
3. Managing and Controlling Linux Services
Install Apache
  
Check ssh.service whether is enabled
 
Enable and then start ssh.service and check again
 
Enable firewall and allow HTTP
 
Testing SSH to another user with the same VM
 
Download with wget
 
Tar archive (Compress, decompress, and extract)
Tar Archive  bundles multiple files and directories into a single file, preserving the original file structure and metadata. It is commonly used on Linux and Unix-like systems for data backup and software distribution but is not a compressed format by itself.
  
Compressing TAR files using bzip2
 
Decompressing with bunzip2 


Extracting with tar -xvf
 

4. Understanding and Applying Linux Permissions
Linux Permissions
Permission types:
Symbol	Meaning	Action Allowed
r	Read	View file contents / list directory
w	Write	Modify file / add or remove files in directory
x	Execute	Run file as program / enter directory

User categories:
User Type	Symbol	Description
Owner	u	The user who owns the file
Group	g	Users in the file’s group
Others	o	Everyone else


Permission Digits:
Digit	Binary	Symbolic	Meaning
0	000	---	No access
1	001	--x	Execute only
2	010	-w-	Write Only
3	011	-wx	Write + Execute
4	100	r--	Read only
5	101	r-x	Read + execute
6	110	rw-	Read + write
7	111	rwx	Full access
Structure of Permission numbers:
Position	Refers To
1st Digit	Owner (u)
2nd Digit	Group (g)
3rd Digit	Others (o)
Commonly used examples:
Command	Owner	Group	Others
chmod 755 script.sh	rwx	r-x	r-x
chmod 777 file	rwx	rwx	rwx
chmod 700 file	rwx	---	---
chmod 600 file	rw-	---	---

5. Searching and Navigating the Linux File System
6. Total Cost of Ownership (TCO) in Cloud Infrastructure
7. Provisioning and Securing a Cloud VM (AWS EC2)  
 
 
 
 
 

Using SSH to connect to EC2 Instance 
Installing Apache on instance
 
Testing Apache
 
Editing Apache2 default page using nano
 

Hello World
 
Hyperlink to download file
 

Succesful download
 
Editing website by using CLI
 
Ending instance
 
8. Writing Bash Scripts and Using Regular Expressions

9. Configuring DNS and Testing Domain Resolution

10. Obtaining and Managing Digital Certificates with Let’s Encrypt
Certbot
Ensure that HTTPS is enabled in inbound rules
 
Ensure apache is installed and enabled and running
 
install and run certbot
 
 
 


Automatic renewal
 
sudo certbot revoke --cert-path /etc/letsencrypt/live/your-domain.com/fullchain.pem
Domain name: https://nathantanjieyingisea1.duckdns.org/
 
11. Scripting Linux Server Functions for Automation
Crontab is a utility that allows the user to schedule automated and recurring tasks also known as cronjobs.
 
Automating crontab to check login history for past 24 hours for a user to identify any unauthorized access. 
 
 
	


