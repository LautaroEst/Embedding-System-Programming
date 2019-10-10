# Quick Setup - Virtual Machine Download

The virtual machine for this class can be created manually for students (difficult) or downloaded from the following instructions (easy). First you need to install VirtualBox on your machine. The latest release is fine to go with.

## Virtual Machines with VirtualBox

VirtualBox is a tool called a Hypervisor. This piece of software allows you to run a different operating system on your host machine (regardless if you have a Windows, MAC, or a Linux OS). There are other HyperVisors like VMware that you are welcome to use but we suggest VirtualBox if you are new to this. VirtualBox software runs on almost all operating systems.

VirtualBox Installation: [https://www.virtualbox.org/wiki/Downloads]

Once VirtualBox is installed, you need to download the Ubuntu Linux OS that you wish to install. For this course we will install a Long Term Support Release for Ubuntu (e.g. 16.04 LTS,17.04 LTS). You may create your own VM and manually download and install all necessary tools as described in the supplementary materials section on Manual Virtual Machine setup. This is good practice if you have never done this before or are not familiar with Linux.

[https://www.virtualbox.org/]

## Download the Virtual Machine

Go to the following google drive link:

[https://drive.google.com/drive/folders/0BzO-JQgfBgLHVDB4LW9ER0N3MGM?usp=sharing]

In this location, there are a few files within a top level folder called Embedded Software. Open this folder and download all of the files to your machine into a folder called Embedded Software.

Once downloaded you should see 5 Files/folders:

* Logs (Folder)
* Snapshots (Folder)
* Embedded Software.vbox
* Embedded Software.vbox-prev
* Embedded Software.vdi

Your files must be named as they are show above. There needs to be a space in between the Embedded and Software words. Your virtual box installation has a specific location it installs its Virtual Machines. You will need to download all of the files below to your local machine's VirtualBox VMs Folder. You can find your VM Folder by clicking "File->Preferences" and select the General Tab. Here there will be a Default Machine Folder. Copy your new folder "Embedded Software" to this path. It is extremely important that this folder and the VM files have Read-Write permissions and not Read-Only permissions. Check this by selecting your VMs Default Machine Folder and going through the properties menu and make it is not read-only.

For example, on my Windows machine, the path to this folder is: c:\users\alex\VirtualBox VMs. I created a folder in here called EmbeddedSW (c:\users\alex\VirtualBox VMs\Embedded Software) and copied all of these files into that location.

Once you have copied these files down to your local machine, you need to add a new virtual machine to VirtualBox. Click "Machine->Add" and select the path to your Embedded Software folder where you copied these VM files to. Now select the "Embedded Software.vbox" file. This will now add your Embedded VM to your VirtualBox VM list!

This VM has a default username "ecee" and an admin password "ecee"
