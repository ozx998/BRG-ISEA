# Lab 1a Setting up Ubuntu, VMware and Command Line Familiarisation
## Installing a Virtual Machine


## 1a-1 Virtualisation and Linux setup
### This is the VMware version used.
<img width="487" height="385" alt="vmware installation" src="https://github.com/user-attachments/assets/e29753c8-f3ec-4b26-9332-51e0ae680802" />

<img width="729" height="597" alt="vmworkstation" src="https://github.com/user-attachments/assets/57bf0301-7fbb-428e-b2c4-b0ca29a6581a" />

### ubuntu version used, successfully installed, nat mode is configured
<img width="950" height="905" alt="ubuntu" src="https://github.com/user-attachments/assets/611f6288-f12c-4e16-811f-1fd630ce945b" />
<img width="950" height="905" alt="ubuntu" src="https://github.com/user-attachments/assets/fef2d556-693f-43de-9fca-63f65048e869" />
<img width="1720" height="980" alt="ubuntu-nat" src="https://github.com/user-attachments/assets/2683bbfe-a537-4253-9058-b3fc28b3daec" />
<img width="1720" height="975" alt="ubuntu-installed" src="https://github.com/user-attachments/assets/a929322c-a2cb-492b-b089-c4eafbc1a49a" />


<img width="691" height="844" alt="ubuntu update" src="https://github.com/user-attachments/assets/417ebf36-700b-4691-86e7-3bad65584b2c" />
Once installed, I updated the system by using commands:
sudo apt update (This is to tell the system to search for the latest updates)
sudo apt upgrade -y (This is to tell the system to proceed with the update)

Package manager is an Advanced Package Tool that helps you install, update, remove, and manage software using the terminal. For example, "sudo apt update" checks for the latest updates.

Repository concept is a online storage where software packages are kept which you can download and install from.

The difference between update and upgrade is that update refreshes the list of available package versions from repositories. While upgrade installs the newer versions of packages already installed in the system.

### ubuntu running successfully
<img width="685" height="195" alt="ubuntu-run" src="https://github.com/user-attachments/assets/e49165f0-588d-4c29-9a3e-b2de6860ee38" />

### 1a Reflection Questions
What challenges did you encounter during the virtual machine setup?
I didn't run into any major issues during the setup. The installation process went smoothly from start to finish, following the standard steps without needing to troubleshoot anything.

What did you learn about virtualisation tools and their differences?
I learned that virtualisation tools vary quite a bit depending on their intended use case. Local VMs, like the one I set up, are convenient for testing and experimentation since they can be reset or cloned easily and don't require ongoing costs. Cloud-based virtualisation platforms, by comparison, offer scalability and remote access but typically come with subscription costs and more complex management.

How confident do you feel using Ubuntu after completing this lab?
I feel quite confident using Ubuntu now. Since the setup went smoothly, I was able to focus on getting comfortable with the interface and basic commands rather than spending time fixing errors.

In what ways can a virtualised Linux environment help in industry scenarios?
A virtualised Linux environment allows developers and IT teams to safely test configurations, software, or updates in an isolated space before deploying them to production systems, reducing the risk of disruptions to live services.

What would you do differently if setting up another VM?
Since this setup went well, I wouldn't change much about my approach. If anything, I'd explore some of the more advanced configuration options now that I'm comfortable with the basics.


# Lab 1a Ubuntu GUI & CLI Familiarisation + Software Installation Methods

## 1a-2 Ubuntu Linux Familiarisation
### GUI Familiarisation
Ubuntu desktop applications such as firefox, File manager, terminal and appstore were explored
<img width="1712" height="950" alt="1a-libre" src="https://github.com/user-attachments/assets/4d76e9ef-dc81-4088-8be3-043468231127" />
<img width="753" height="938" alt="1a-2 gui fam" src="https://github.com/user-attachments/assets/5d21ed12-b05b-46a8-b95c-38326828cd73" />

### Terminal Commands
These are the commands that I used to explore the Linux environment

```bash
ps -e
top
ls
ls -la
ls -alt
touch
nano
gedit
cat
less
```
<img width="1653" height="735" alt="1a gedit" src="https://github.com/user-attachments/assets/255cb408-1522-4227-a531-ab2f1d423c63" />
<img width="677" height="58" alt="1a testcommand" src="https://github.com/user-attachments/assets/9eebdc3a-64b7-4235-b14c-5c83bf6e35d9" />
<img width="685" height="581" alt="1a notes" src="https://github.com/user-attachments/assets/dad0d641-1278-400e-abc0-81148941b846" />
<img width="689" height="350" alt="1a test1a" src="https://github.com/user-attachments/assets/e77242f0-06f8-457a-8084-d87d3db34876" />
<img width="694" height="532" alt="1a lsalt" src="https://github.com/user-attachments/assets/db0a2e70-d7fd-4ef1-959e-72a52f298cc1" />
<img width="690" height="600" alt="1a ls" src="https://github.com/user-attachments/assets/31e02057-04ec-4ed5-b8de-e54b70b674ef" />
<img width="693" height="614" alt="1a top" src="https://github.com/user-attachments/assets/503dac7c-5036-4ffc-b093-d75e4b4c91c7" />
<img width="695" height="879" alt="1a less" src="https://github.com/user-attachments/assets/5898af59-5023-4d2e-9258-ab54a6da0fce" />
<img width="693" height="164" alt="1a cat" src="https://github.com/user-attachments/assets/9d61e181-6a2a-4cb5-8e86-60755c6e9a68" />


### System information Commands

I explored system information using the terminal commands:
uname -a
lsb_relaese -a
hostnamectl
/proc/cpuinfo

<img width="691" height="877" alt="1a proc" src="https://github.com/user-attachments/assets/7d8f9509-7c9b-4728-a78c-6faffaa370e0" />
<img width="691" height="513" alt="1a uname" src="https://github.com/user-attachments/assets/76758c80-c0a4-48ab-b26d-a3ab5c435bdd" />

###User Privilege Experiment
commands used:
whoami
sudo whoami
adduser test
sudo adduser test
<img width="691" height="372" alt="1a whoami" src="https://github.com/user-attachments/assets/9e7155ea-1db6-4101-92b5-fb6179c45715" />

### Networking Tests
Here I will try to ip an output and ping to ip 8.8.8.8
commands used:
```bash
ip a
ping 8.8.8.8
```

### Edit host file name and ping GoogleEpicDNS
Here I will edit the hosts file and create a custom name, and also try and ping GoogleEpic DNS
The commands I used are 
```bash
sudo nano /etc/hosts editing
ping GoogleEpicDNS
```

### DNS Lookup
commands used:
```bash
nslookup google.com
sudo apt install whois
whois google.com
```

### Public vs Private IP Reflection
Here I find my ip using https://whatismyipaddress.com and I noticed that it is different.
The IP address shown by ip a is the private IP address assigned to Ubuntu inside the network. While the IP address shown by whatismyipaddress.com is the public IP address which is seen by the websites and is provided by the router.
The commands I used are 
```bash
ip a
```

### Hardware Info Commands
Here I will show the difference between the terminal hardware info and the GUI hardware info
The commands I used are
```bash
lsusb
lspci
less /proc/cpuinfo
```

### Software Installed
Here I will demonstrate the 3 ways of using softwares in Ubuntu. Through the browser, through binary download, and through a repository install
The commands I used are
```bash
ls -lah
```
### Command Line Install via Apt
Here I will use APT to update package lists. When I tried to run less /etc/apt/sources.list, the system prompted me that since my Ubuntu is a newer version, it has been moved to /etc/apt/sources.list.d/ubuntu.sources
The commands I used are
```bash
sudo apt update
sudo apt upgrade
sudo apt install vlc
vlc --version
less /etc/apt/sources.list.d/ubuntu.sources
```
### Source Code Compilation
Here I will file hello_world.c with source code, compile it using gcc, and execute it. 
When I tried to compile it using gcc, the system prompted me that I do not have gcc installed. Thus, i used sudo apt install gcc
The commands I used are
```bash
nano hello_world.c
sudo apt install gcc
gcc hello_world.c -o hello_world_executable
ls -lah
./hello_world_executable
```

### Reflection Summary

### 1a-2 Reflection Questions
Which file editors are best for remote access and why?

Compare Software Installation Methods: Saas vs binaries vs repos vs source

what are the pros/cons of each method from user and developer perspectives

How did using CLI improve your understanding of Linux
