1. Installing a Linux Environment on Your PC
(Based on: Obtaining a Linux Environment Lab)
Session 1a: Setting up linux
Managed to create a new repository but was having some issues with cloning the repository to my local machine using Git, googled it and found "sudo apt update && sudo apt install git -".
However met some error when using that line, stated "error: The repository file :/cdrom resolute release" no longer has a release file"
Went back on google and found "sudo nano /etc/apt/sources.list" There was 0 files

<img width="872" height="646" alt="image" src="https://github.com/user-attachments/assets/c215a1d5-b945-4ed4-a033-a5d2940373e5" />

I realized that this error happens because the OS installer leaves the virtual CD-ROM drive mapped as an active package repository source file. So when I try to update using apt update, the system prevents the update.
Had to look inside the extra sources directory with "ls /etc/apt/sources.list.d/" , proceeded to show me a file named cdrom.sources
I then deleted the cdrom file with "sudo rm -f /etc/apt/sources.list.d/cdrom" and follow up with sudo apt update. After doing that my sudo apt install git -y worked.

<img width="873" height="697" alt="image" src="https://github.com/user-attachments/assets/71e3d382-3918-42e6-8271-1c7f5f34553a" />





Lab: Obtaining Linux on your PC - Install Ubuntu using Virtualbox/VMware Workstation
→ I used VMware workstation to create a new virtual machine and have configured the following

<img width="791" height="520" alt="image" src="https://github.com/user-attachments/assets/26cd7622-2445-403b-993d-bd3abd2e7806" />

→ Living system proof on running ubuntu
 
<img width="794" height="530" alt="image" src="https://github.com/user-attachments/assets/febcbe98-e611-47d3-a441-8bd9f3a40402" />
