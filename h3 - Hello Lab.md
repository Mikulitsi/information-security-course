# h3 - Hello Lab

## Karvinen 2021: Install Debian on Virtualbox - Updated 2024
- You will start with installing VirtualBox and choosing the create new virtual machine option.
- Then you will choose "Expert Mode" for installation but skip on "Unattended Install."
- I also created the VM with plenty of memory and sufficient virtual disk.
- Add the ISO as a virtual CD and boot the VM.
- After you run the installer, you will be prompted to select an English and Finnish configuration as well as fill out user info.
- After the install is complete, log into the system and open a terminal and update everything.
- After the updating process is complete install a firewall and reboot your system.
- In order to fix the small screen and enable copy and paste, you can install Virtual Box Guest Additions.


Thoughts:
  - I assigned 4GB of RAM to the VM and 60 GB disk space as my laptop's RAM is only 8GB. While it's not the fastest, it seemed to run well enough.
  - I did not run into the black screen bug but good to know about the xforcevesa trick if I do at some point or have friends that have that problem.
  
  
## Karvinen 2020: Command Line Basics Revisited
- pwd, ls, and cd to move around folders.
- nano filename lets you edit files in the terminal.
- mkdir, mv, cp, and rm are for making, moving, copying, and deleting stuff.
- rm -r deletes everything and it can't be undone.
- ssh lets you connect to other computers remotely.
- scp is for copying files between computers.
- Use --help to learn what a command does.
- history shows your past commands, and ctrl + R helps you search them.
- Important folders: /home/, /etc/, /media/, /var/log/.
- sudo gives you superuser/admin powers.
- Install software with sudo apt-get install command.
- Remove stuff with sudo apt-get purge command.

Thoughts:
  - We did a bit of Linux command line basics stuff during one lesson in Intro to Infra & Cloud course during last spring but it's good to get repetition as without it, I forget these commands quickly.

## Can't Fish
- Executed a ping command and added -c 10 to the command as without it Linux will continue to ping endlessly. Now it stops pinging after 10 attempts.

<img width="665" height="332" alt="image" src="https://github.com/user-attachments/assets/c3c4aff3-20dd-4f35-967f-7b0c57df714c" />

- Executed the same command after disabling network:

<img width="657" height="110" alt="image" src="https://github.com/user-attachments/assets/e8cccc61-99f6-432c-90ea-bb1c716bd3a5" />


## Local only
- First I start with installing the NMap:
<img width="430" height="31" alt="image" src="https://github.com/user-attachments/assets/693cdfc0-3e79-406f-b0be-99c6c6f1b2a4" />

- Then with the network being disabled, I ran the portscan.

<img width="808" height="422" alt="image" src="https://github.com/user-attachments/assets/0f857e04-dd1b-4c4c-ad10-b9dc5c873b87" />


## Daemon scan
<img width="462" height="21" alt="image" src="https://github.com/user-attachments/assets/24d64c29-fa47-4f61-a161-1131b8a6355d" />
<img width="1001" height="477" alt="image" src="https://github.com/user-attachments/assets/d15b375f-3261-4521-9711-ce0ec2787b08" />


## Bandit oh-five
### Level 0
<img width="680" height="577" alt="image" src="https://github.com/user-attachments/assets/b31b9c71-2e03-4a97-b174-145253fdf763" />

### Level 0 → Level 1
<img width="845" height="211" alt="image" src="https://github.com/user-attachments/assets/8e8d7430-70c2-478a-bfe2-0f36e016f4d1" />

### Level 1 → Level 2
<img width="642" height="95" alt="image" src="https://github.com/user-attachments/assets/706bdd16-b664-40e1-b496-a1e74c65a3f9" />
<img width="342" height="198" alt="image" src="https://github.com/user-attachments/assets/896dd217-498f-422b-acec-1327a7423457" />

### Level 2 → Level 3
<img width="586" height="267" alt="image" src="https://github.com/user-attachments/assets/f645bdd6-830a-41ba-809e-c4aa184237e7" />

### Level 3 → Level 4
<img width="662" height="522" alt="image" src="https://github.com/user-attachments/assets/6d342043-12cf-4c34-8953-72ebb0a304d7" />


## Sources
- https://terokarvinen.com/2021/install-debian-on-virtualbox/
- https://terokarvinen.com/2020/command-line-basics-revisited/
- https://terokarvinen.com/information-security/
- https://www.scaler.com/topics/port-scanner-linux/
- https://www.hivelocity.net/kb/scanning-ports-in-your-linux-system/
- https://labex.io/tutorials/nmap-how-to-scan-localhost-ports-418379
- https://overthewire.org/wargames/bandit/
- https://www.wikihow.com/Use-SSH
- https://www.manageengine.com/products/eventlog/kb/linux/how-to-show-hidden-files-in-linux.html
