# Manual Setup - Linux VM

If you do not want to go the route of using the provided Virtual Machine Download, you can setup your own box. Below is the list of steps you need to run to get your own environment up and running. This will definitely take long and will be more frustrating to figure out if you go this route, but it will certainly help you in the future as you work on other VMs.


## Virtual Machines with VirtualBox

VirtualBox is a tool called a Hypervisor. This piece of software allows you to run a different operating system on your host machine (regardless if you have a Windows, MAC, or a Linux OS). There are other HyperVisors like VMware that you are welcome to use but we suggest VirtualBox if you are new to this. VirtualBox software runs on almost all operating systems.

VirtualBox Installation: [https://www.virtualbox.org/wiki/Downloads]

Once VirtualBox is installed, you need to download the Ubuntu Linux OS that you wish to install. For this course we will install a Long Term Support Release for Ubuntu (e.g. 16.04 LTS,17.04 LTS). You may create your own VM and manually download and install all necessary tools as described in the the section Creating Your Own Virtual Machine (below). This is good practice if you have never done this before or are not familiar with Linux.


## Creating Your Own Virtual Machine

If you already have a Linux machine and are familiar with Linux, use whatever distribution you are comfortable with. The course will formally support the latest Ubuntu release.

Download the Ubuntu 17.04 LTS release here (an .iso file):

* [http://releases.ubuntu.com/17.04/]
* [http://virtualboxes.org/images/ubuntu]

Open up VirtualBox and now you will need to create a virtual machine. There are many online resources that show this process (and YouTube Videos), but here are some links with how to do this.

* [https://www.youtube.com/watch?v=jy3ExRlQAys]
* [https://www.youtube.com/watch?v=GGorVpzZQwA]

I also highly suggest that you install VirtualBox Guest Additions as it adds useful features like folder shares between your host and virtual machine as well as resolution/screen scaling.

    [https://www.virtualbox.org/manual/ch04.html]

## Linux Configuration

Once you have installed a Linux VM, you will create a login with a password. Do not forget this password, we will use it regularly. Login into your VM and you need to do a quick package update and install a couple of packages. Open up a terminal and start with the following commands. A terminal usually starts with a prompt, on the default ubuntu installation, that is a dollar sign “$”. All examples provide that symbol at the beginning of a terminal command. You do not need to manually type that in.

To perform the update run the following command:

```
  sudo apt-get update
```

To search for packages you can install you can search the linked repositories. if you are interested to see what is out there type this, but enter in a correct package name.

$ sudo apt-cache search <package-name>

```
sudo apt-cache search arm-none-eabi 
```

There are a couple of compilers we are going to use. Here is a list of them with a description.

* gcc – Host machines cross Compiler. Used for testing architecture independent code. This should already be installed on your machine.

* arm-none-eabi-gcc – Compiler we will use for the Cortex-M4 

These are the packages that need to be installed with apt-get install.

* git
* gitk
* gcc-arm-none-eabi
* vim (or another text editor of your choice)

Here is an example of how you would install some of these packages.

```
sudo apt-get install git gitk
sudo apt-get install gcc-arm-none-eabi vim
```


