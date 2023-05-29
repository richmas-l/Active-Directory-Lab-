<img src="https://imgur.com/Q7fBbju.png"
     alt="BugBountyToolkit"
     style="float: left; margin-right: 10px;" />

# INTRODUCTION
This project is dedicated to constructing a robust Active Directory (AD) lab environment, meticulously designed to simulate real-world scenarios and facilitate comprehensive testing. The focus is on creating an environment that mirrors a production AD setup while allowing for controlled experimentation. By meticulously building this lab, we can thoroughly assess potential vulnerabilities, misconfigurations, and security gaps that may exist within an AD infrastructure.<br/>

Through this AD lab build, we aim to create a safe yet realistic environment for conducting rigorous testing, analysis, and implementation of security measures. It serves as an essential tool for enhancing our understanding of AD security, enabling us to proactively address any vulnerabilities before they become exploitable risks.
<br />

## ENVIRONMENTS USED
- Kali linux</b> 
- Windows Server 2019</b>
- Windows 10 Enterprise</b> 
- Oracle VirtualBox</b>

## Instructions
Update, upgrade & reboot linux machine

```
sudo apt upgrade && update -y
```
- [Download & install Oracle Virtualbox](https://www.geeksforgeeks.org/how-to-install-virtual-box-in-kali-linux/)
- [Download Windows Server 2019 ISO Image](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019)</b>
- [Download Windows 10 Enterprise](https://www.microsoft.com/en-us/evalcenter/download-windows-10-enterprise)</b>

## AD Build Instructions
### Windows Server 2019 Installation

Lets start with installing the Windows Server 2019. 

If you encounter error "**Windows cannot find microsoft Software license Terms** ..."  remove the virtual floppy drive and restart the process. 

<img src="https://imgur.com/bRChFmg.png"
     style="float: left; margin-right: 10px;" />

After the installation is complete, go to pc name and change it to an easy to recognise name for a domain controller. 

<img src="https://imgur.com/vo0A2sw.png"
     style="float: left; margin-right: 10px;" />


### Domain Controller Installation
This will acts as a central authority that ensures security, manages access, and keeps things organized within a network of computers in an organization. 
Restart your server, upon restart you should have a windows server manager dashboard. 
- You will click Manage on the top right of your screen.
- **Add roles & features**.
- Click next on default selections until you reach server roles. 
- Check **Active Directory Domain Services** in server roles

<img src="https://imgur.com/CsIJ3In.png"
     style="float: left; margin-right: 10px;" />
     
Click next until you finally get to install. 

<img src="https://imgur.com/C6KMbCQ.png"
     style="float: left;margin-right: 10px;" />


Once complete with installation you will see a notification pop up on the top right. <br />
click it **promote this server to a domain controller.**

<img src="https://imgur.com/7Ww45EH.png"
     style="float: left;margin-right: 10px;" />

### Domain Controller Configuration
Once you promote the server to domain controller, you will have a configuration pop up

-**Deployment configuration**: Add a new forest: Name your domain and give it a .local (company.local)<br />
-**Domain Controll Options**: Create a password<br />
-**Click next for rest of steps until installation and auto reboot**

<img src="https://imgur.com/xhxf7q3.png"
     style="float: left; margin-right: 10px;" />
     
### Domain Controller Complete
You have finally completed the creation of the domain controller.<br />
As you can see your next login will show the domain controller name/administrator

<img src="https://imgur.com/6thQNjT.png"
     style="float: left; margin-right: 10px;" />


### Add 2 Users
- Start the installation process again like you did the server above<br />
- Rename the pc name<br />
- Repeat once more. <br />
- You should have 2 Users now<br />

<img src="https://imgur.com/6thQNjT.png"
     style="float: left; margin-right: 10px;" />




[![asciicast](https://asciinema.org/a/sMorBlA5yzTIwfdiWzdRR3yEh.svg)](https://asciinema.org/a/sMorBlA5yzTIwfdiWzdRR3yEh)

## Docker Build Instructions
```
docker build . -t hackersploit/bugbountytoolkit
```

## Installation Instructions - Ubuntu/Debian
```
git clone https://github.com/AlexisAhmed/BugBountyToolkit.git
cd BugBountyToolkit
chmod +x install.sh
./install.sh
```
## Installing New Tools
You can install new tools from the Kali Linux repositories by utilizing the Katoolin script.
```
cd ~/toolkit
cd katoolin
./katoolin.py
```
# Installed Tools
- [x] altdns
- [x] amass
- [x] awscli
- [x] bucket_finder
- [x] CloudFlair
- [x] commix
- [x] dirb
- [x] dirsearch
- [x] dnsenum
- [x] dnsrecon
- [x] dotdotpwn
- [x] droopescan
- [x] fierce
- [x] ffuf
- [x] gobuster
- [x] gitGraber
- [x] httprobe
- [x] joomscan
- [x] Knockpy
- [x] masscan
- [x] massdns
- [x] Nikto
- [x] Nmap
- [x] Recon-ng
- [x] s3recon
- [x] S3Scanner
- [x] sqlmap
- [x] subfinder
- [x] Sublist3r
- [x] subjack
- [x] SubOver
- [x] teh_s3_bucketeers
- [x] thc-hydra
- [x] theHarvester
- [x] tmux
- [x] virtual-host-discovery
- [x] wafw00f
- [x] waybackurls
- [x] wfuzz
- [x] whatweb
- [x] wpscan
- [x] XSStrike
- [x] zsh

## Wordlists
- SecLists 

# Tools being added
- [ ] Sn1per Framework

# Contributors
- https://github.com/rishabhdeepsingh
- https://github.com/brutalgg 
- https://github.com/vimicasa
- https://github.com/muokicaleb
- https://github.com/mcnamee
