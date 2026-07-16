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

### Terminal Commands<img width="886" height="489" alt="1a lookup" src="https://github.com/user-attachments/assets/fe58747a-9bd5-4449-9122-b64e69b1d40d" />


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
uname -a
lsb_relaese -a
hostnamectl
/proc/cpuinfo

<img width="691" height="877" alt="1a proc" src="https://github.com/user-attachments/assets/7d8f9509-7c9b-4728-a78c-6faffaa370e0" />
<img width="691" height="513" alt="1a uname" src="https://github.com/user-attachments/assets/76758c80-c0a4-48ab-b26d-a3ab5c435bdd" />

###User Privilege Experiment
whoami
sudo whoami
adduser test
sudo adduser test
<img width="691" height="372" alt="1a whoami" src="https://github.com/user-attachments/assets/9e7155ea-1db6-4101-92b5-fb6179c45715" />

### Networking Tests
```bash
ip a
ping 8.8.8.8
```
<img width="695" height="737" alt="1a ip a" src="https://github.com/user-attachments/assets/5eed2323-bef3-4a4c-9fd7-e68e2cb84a15" />

### Edit host file name and ping GoogleEpicDNS
```bash
sudo nano /etc/hosts editing
ping GoogleEpicDNS
```
<img width="893" height="875" alt="1a sudo nano" src="https://github.com/user-attachments/assets/466b91bf-b252-4e1b-bbc6-18a815b145da" />

### DNS Lookup
commands used:
```bash
nslookup google.com
sudo apt install whois
whois google.com
```
<img width="891" height="807" alt="1a whois" src="https://github.com/user-attachments/assets/77c3a47d-4927-4764-a348-f2099509b9c2" />
![Uploading 1a lookup.png…]()

### Hardware Info Commands
Here I will show the difference between the terminal hardware info and the GUI hardware info
The commands I used are
```bash
lsusb
lspci
less /proc/cpuinfo
```
<img width="890" height="740" alt="1a proccpu" src="https://github.com/user-attachments/assets/7bd3cc85-e2f1-4124-858e-0dcbdefc9599" />
<img width="892" height="694" alt="1a lsusb" src="https://github.com/user-attachments/assets/50d069ec-db44-422d-90e6-dbfbb46b3abd" />
<img width="892" height="851" alt="1a less bus" src="https://github.com/user-attachments/assets/e3ca85e1-d4b9-4857-a3e4-c1a836900b89" />
<img width="850" height="635" alt="1a command output" src="https://github.com/user-attachments/assets/07b9e1cd-e407-4210-9b88-d39a0229e75c" />

### Output Redirection
Here I will save a command line output into a file, view it and delete it all using just the terminal
The commands I used are
```bash
command lsusb > output_of_lsusb
ls -lah
less output_of_lsusb
rm output_of_lsusb
```
<img width="889" height="597" alt="1a lessoutput" src="https://github.com/user-attachments/assets/eca9eb28-0e71-4078-9f87-a44fad478278" />
<img width="891" height="552" alt="1a output redirec" src="https://github.com/user-attachments/assets/bcb09c39-1d99-4358-b46f-fda0f0863fee" />

### Software Installed
3 ways of using softwares in Ubuntu. Through the browser, through binary download, and through a repository install
The commands I used are
```bash
ls -lah
```
<img width="1712" height="950" alt="1a-libre" src="https://github.com/user-attachments/assets/7b25e947-33c8-4c72-b557-3be2e98aea18" />
<img width="361" height="65" alt="1a download" src="https://github.com/user-attachments/assets/c7eb263c-4ad5-4cb8-a95f-e9ae6fd43d30" />
<img width="953" height="884" alt="1a app" src="https://github.com/user-attachments/assets/b075c02a-41bd-47c8-a511-27f44b1a2055" />

### Command Line Install via Apt
The commands used:
```bash
sudo apt update
sudo apt upgrade
sudo apt install vlc
vlc --version
less /etc/apt/sources.list.d/ubuntu.sources
```
<img width="805" height="386" alt="1a vlcver" src="https://github.com/user-attachments/assets/a8474c40-a412-40ff-af10-91e2b45c8227" />
<img width="892" height="877" alt="1a ubuntusrc" src="https://github.com/user-attachments/assets/9d47e22c-9f9e-40d7-946a-223a9eb590f5" />
<img width="889" height="626" alt="1a update" src="https://github.com/user-attachments/assets/ebfaa7a7-93f6-46dd-8442-f3129254b650" />
<img width="890" height="751" alt="1a installup" src="https://github.com/user-attachments/assets/b8d81f41-ffc9-4152-88e1-0bda38b235c4" />

### Source Code Compilation
The commands used:
```bash
nano hello_world.c
sudo apt install gcc
gcc hello_world.c -o hello_world_executable
ls -lah
./hello_world_executable
```
<img width="820" height="691" alt="1a HelloCode" src="https://github.com/user-attachments/assets/ec589d55-5ed8-49e6-96e0-2194ef17783a" />
<img width="818" height="693" alt="1a Hello" src="https://github.com/user-attachments/assets/a887abbe-216d-4d1a-b707-beb2a00f96bf" />


### Reflection Summary 1a-2

Which file editors are best for remote access and why?
Nano file editor is better for remote access as it is a terminal editor.

Compare Software Installation Methods: Saas vs binaries vs repos vs source
Saas: does not need to be installed e.g Google Docs
Binaries: Pre-compiled files to download and run directly. Fast and simple, but need to manage updates and dependencies manually. 
Package Repositories: Software installed via a package manager that automatically handles dependencies and updates. e.g. apt install
Source Code: Raw code compiled manually and offers maximum control and customization, but is time-consuming, with dependencies, builds, and updates all needing manual handling.

what are the pros/cons of each method from user and developer perspectives
SaaS: The simplest option since no download is required, though functionality can sometimes be limited compared to other methods.
Binaries: A middle-ground option offering full functionality, but security can be a concern since not all downloads come from trustworthy sources.
Repositories: The easiest way to get full functionality, though updates may lag behind what's available directly from the source.
Source: The most demanding option, as it requires programming knowledge to build and install successfully.

How did using CLI improve your understanding of Linux
Using the CLI deepened my understanding by forcing me to know exactly what each command does, rather than relying on GUI shortcuts.

## 1b-1 Linux Services, SSH, Firewalls & Compression
### Apache Web Server Installed
The commands I used:
```bash
sudo apt install apache2
```
<img width="862" height="113" alt="1b apachedown" src="https://github.com/user-attachments/assets/6622c78d-4f59-4874-9dea-12fd75e5afb0" />


### Modified index.html page
Here I will modify Apache's default page to make it my own. I first tried nano /var/www/html/index.html since nano is to edit, but I could not save the file as i did not have permission. Hence, I had to use sudo nano to edit the file instead.
The commands I used are
```bash
sudo nano /var/www/html/index.html
```
<img width="891" height="842" alt="1b apacherewrite" src="https://github.com/user-attachments/assets/b950c800-940f-4a5f-81fb-8ebb69b4a392" />

### IP Address Identified and Shared
Here I will show my local IP and loopback IP and that I can access my partner's IP. For this excercise, I used my host OS to demonstrate.
<img width="895" height="647" alt="1b apacheweb" src="https://github.com/user-attachments/assets/28d99ff7-5c81-4854-9f38-2468c867238a" />
This shows my both my vm's loopback IP labelled lo and my local IP. 
<img width="821" height="454" alt="1b whatsmyip" src="https://github.com/user-attachments/assets/e62dd6f4-21a9-460b-9fbe-6b697051fbbd" />


### Nmap Port Scan Result
<img width="784" height="286" alt="1b zenmap" src="https://github.com/user-attachments/assets/c11bd749-6cc3-4f2b-b854-33a0d6645957" />


### Firewall (UFW) Status and Rules
Here I will show you the status before and after enabling firewall, and show youthat port 80 is allowed and verified. I also had to reinstall apache as the previous excercise asked us to remove apache.
The commands I used are
```bash
sudo ufw status verbose
sudo ufw allow "Apache"
sudo apt install apache2
```
<img width="639" height="294" alt="1b status" src="https://github.com/user-attachments/assets/4e7aa68e-ac7e-4b63-bc04-9e599e6e6a24" />

### New User Created and Verified
Here I will add a user and verify it with /etc/passwd
The commands I used are
```bash
sudo adduser testuser
cat /etc/passwd
```
<img width="682" height="198" alt="1b-f" src="https://github.com/user-attachments/assets/c123c959-3899-40da-bfc1-87e2622d8388" />

<img width="689" height="354" alt="1b-d" src="https://github.com/user-attachments/assets/9b4d30c3-e996-499f-8010-5075cbdfcdc3" />

### Compression and Decompression Tested
Here I will compress and decompress files using terminal codes and show the output using ls -la. when using bzip the system prompted me to install, so I used sudo apt install bzip2.
The commands I used are
```bash
ls -la
sudo apt install bzip2
bzip2 tar.bz2
bunzip2 tar.bz2
tar -xvf Gutenberg.tar
grep -n "best of times" twocities.txt
```
<img width="752" height="694" alt="1b-g" src="https://github.com/user-attachments/assets/221e77ee-bf61-4657-a74a-2aa7c85ce252" />

### SCP File Transfers Between Machines
Here I will copy a file from host machine to vmmachien through ssh
The commands I used are
```bash
echo "1b test" > test.txt
scp test.txt zxong@192.168.134.128:/home/zxong
ls -la
```
<img width="957" height="229" alt="1b scp" src="https://github.com/user-attachments/assets/1095b8e9-7bf0-4de9-a41c-7bdf506ca0c1" />

<img width="690" height="250" alt="1b testtxt" src="https://github.com/user-attachments/assets/8d986ef7-0287-4a9a-b0bb-26d7606125c5" />

### Extension Challenge 1 Completed
Here I will SSH into my vm and create a file on its desktop from my host machine
The commands I used are
```bash
ssh zxong@192.168.134.128
cd ~/Desktop
touch zxong
ls -la Desktop
```
<img width="972" height="504" alt="1b sshhosttovm" src="https://github.com/user-attachments/assets/c1a9dffd-cc3b-49a6-ac67-7117bcf716b5" />


### Extension Challenge 2 Completed
Here I will attempt to launch gedit over SSH. I am unable to launch gedit over SSH as is a GUI text editor and SSH only allows for command line access. 
The commands I used are
```bash
ssh zxong@192.168.134.128
gedit
```
<img width="820" height="691" alt="1b gedit" src="https://github.com/user-attachments/assets/f9ee8001-a4cd-4aa0-9047-c43d600de2f2" />

### Extension Challenge 3 Completed
Here i will create new files and attempt to transfer them from my host machine to my vm
The commands I used are
```bash
echo "test test" > test1
echo "test test" > test2
scp test.txt test1.txt test2.txt zxong@192.168.134.128
ls -la
```
<img width="690" height="250" alt="1b testtxt" src="https://github.com/user-attachments/assets/878c39cd-e506-4856-b046-a7a048a861ee" />
<img width="957" height="229" alt="1b scp" src="https://github.com/user-attachments/assets/8335ec19-8d2f-4c03-ab98-22f7c663298d" />

### Extension Challenge 4 Completed
Here I will download the top 10 books from Gutenberg, compress them using tar and bzip2, then transfer them to my host machine from vm via scp
The commands I used are
```bash
mkdir gutenberg_top10
cd gutenberg_top10
wget https://www.gutenberg.org/files/2701/2701-0.txt -O 01_moby_dick.txt
wget https://www.gutenberg.org/files/1342/1342-0.txt -O 02_pride_and_prejudice.txt
wget https://www.gutenberg.org/files/27509/27509-0.txt -O 03_2006_cia_world_factbook.txt
wget https://www.gutenberg.org/files/1513/1513-0.txt -O 04_romeo_and_juliet.txt
wget https://www.gutenberg.org/files/42486/42486-0.txt -O 05_two_magics.txt
wget https://www.gutenberg.org/files/2641/2641-0.txt -O 06_room_with_a_view.txt
wget https://www.gutenberg.org/files/27558/27558-0.txt -O 07_2003_cia_world_factbook.txt
wget https://www.gutenberg.org/files/2554/2554-0.txt -O 08_crime_and_punishment.txt
wget https://www.gutenberg.org/files/65662/65662-0.txt -O 09_der_zauberberg_zweiter_band.txt
wget https://www.gutenberg.org/files/67979/67979-0.txt -O 10_blue_castle.txt
ls -la
tar cf gutenbergtop10.tar gutenbergtop10
bzip2 gutenbergtop10.tar
scp zxong@192.168.134.128:/home/zxong/gutenbergtop10.tar.bz2 Desktop
```
<img width="575" height="59" alt="1b cd" src="https://github.com/user-attachments/assets/16e16c7f-a29a-477c-8ac0-5bf9c9b0382a" />
<img width="467" height="39" alt="1b bzipp" src="https://github.com/user-attachments/assets/e172308a-f861-4b06-aad3-a473e87d0606" />
<img width="930" height="292" alt="1b gutDownload" src="https://github.com/user-attachments/assets/e2693cdc-a856-4af7-92e9-dffc4fdf1412" />
<img width="814" height="500" alt="1b wget" src="https://github.com/user-attachments/assets/8c0208d2-756b-4670-9de5-0021799901c0" />

### Two VMs Networked
Here I will attempt to ping my host machine and my ubuntu to each other
The commands I used are 
```bash
ping 192.168.134.128
ipconfig
ping 192.168.18.67
```
<img width="694" height="180" alt="1b ubuping" src="https://github.com/user-attachments/assets/77d7dbbd-8fd2-4ef6-a68c-cb96e5e87b4c" />
<img width="1118" height="620" alt="1b pcping" src="https://github.com/user-attachments/assets/585d8735-dcdb-4c26-ae30-1171213e4e07" />

### Reflection Paragraph
Working with Linux networking gave me a much deeper, hands-on understanding of how machines actually communicate with each other, rather than just reading about it. Setting up SSH access let me control my VM remotely and made me realise how much server administration relies on the command line rather than a GUI. Using SCP to transfer files between my host machine and VM helped me understand how data moves securely between systems, and troubleshooting connection errors along the way taught me to think carefully about file paths, hostnames, and which machine I was actually issuing commands from.

### 1b-1 Reflection Questions

Whats the role of a firewall in managing services?
A firewall controls which ports/services are reachable from outside, blocking unwanted traffic while allowing legitimate access
How did SSH access deepen your understanding of Linux as a server?
SSH showed me that servers are managed entirely through commands, reinforcing that GUI tools aren't available or necessary for remote administration
Why is file compression important in server contexts?
Compression reduces storage space and transfer time, making backups, downloads, and file transfers between machines faster and more efficient.
How does user privilege management help secure system?
Limiting user privileges restricts what each account can access or modify, reducing damage potential if credentials are compromised or misused.

## 1b-2 Linux File Permissions & Gropu Access Control

### Three Users Created
Here i will create three new users using adduser
The commands I used are
```bash
sudo adduser alice
sudo adduser joe
sudo adduser dude
cat /etc/passwd
```
<img width="834" height="598" alt="1b adduser" src="https://github.com/user-attachments/assets/17198288-8727-444a-9af7-509aa1abf6cc" />
<img width="771" height="628" alt="1b passwd" src="https://github.com/user-attachments/assets/dda96afc-dace-4e7c-925d-c057d0ce262d" />

### Group Created and Configured
Here I will create a group with alice and joe via adduser [user][group]
The commands I used are
```bash
sudo groupadd sharedgroup
sudo adduser alice sharedgroup
sudo adduser joe sharedgroup
less /etc/group
```
<img width="668" height="94" alt="1b grp" src="https://github.com/user-attachments/assets/14a43721-e104-4a03-a6b8-ca2be0573321" />
<img width="468" height="300" alt="1b shrdgrp" src="https://github.com/user-attachments/assets/937bc1f2-b5fd-472a-8b3f-b677b04b2e08" />


### 'Shared' Directory Created in /home/
Here I will output mkdir /home/shared and update ownership and group via chown, chgrp
The commands I used are
```bash
sudo mkdir /home/shared
sudo chown alice /home/shared
sudo chgrp sharedgroup /home/shared
ls -ld /home/shared
```
<img width="817" height="111" alt="1b homeshd" src="https://github.com/user-attachments/assets/405012b1-ce2d-49dc-a265-448d6d5527d2" />

### Ten Files Created in 'shared' Folder
Here I will create 10 files inside the "shared" folder
The commands I used are
```bash
sudo touch /home/shared file1.txt
sudo touch /home/shared file2.txt
sudo touch /home/shared file3.txt
sudo touch /home/shared file4.txt
sudo touch /home/shared file5.txt
sudo touch /home/shared file6.txt
sudo touch /home/shared file7.txt
sudo touch /home/shared file8.txt
sudo touch /home/shared file9.txt
sudo touch /home/shared file10.txt
ls -l /home/shared
```
<img width="817" height="244" alt="1b files" src="https://github.com/user-attachments/assets/83f105ed-d8a0-43d6-bcc5-1a4c8771604c" />

### Permissions Assigned Properly
Here I will give permission to alice and joe in the shared group
The commands I used are
```bash
sudo touch /home/shared/file{1..10}.txt
sudo chown alice:sharedgroup /home/shared/file*.txt
sudo chmod 750 /home/shared/file*txt
ls -l /home/shared
```
<img width="819" height="546" alt="1b chown" src="https://github.com/user-attachments/assets/a018390d-637c-433d-8913-ced46ab68863" />

### Access Verified as Each User
Here I will check the permissions of the users
The commands I used are
```bash
su - alice
su - joe
su - dude
whoami
ls -l /home/shared
echo "test" >> /home/shared/file1.txt
echo "test" >> /home/shared/file2.txt
cat /home/shared/file1.txt
```
<img width="821" height="550" alt="1b access" src="https://github.com/user-attachments/assets/a526fa29-989c-474c-8b1a-1e88377c14c6" />

### Use of chmod/chown/chgrp -R
Here I will show the usage of recursive flags
The commands I used are
```bash
sudo chown -R alice /home/shared
sudo chgrp -R sharedgroup /home/shared
sudo chmod -R 750 /home/shaared
sudo ls -ld /home/shared
sudo ls -l /home/shared
```
<img width="649" height="367" alt="1b recursive" src="https://github.com/user-attachments/assets/ae841b39-5e61-45a1-8c89-b63b48ec170a" />

### Add Dude to Sudo
Here I will add dude to sudo group
The commands I used are
```bash
sudo addusers dude sudo
groups dude
```
<img width="422" height="79" alt="1b adddude" src="https://github.com/user-attachments/assets/dea16dc6-8992-4c85-8a91-7e214853c770" />

### Dude Sudo Access
Here I will use dude's new sudo permission to access protected files
The commands I used are
```bash
su - dude
ls -l /home/shared
sudo ls -l /home/shared
```
<img width="663" height="330" alt="1b dudesudo" src="https://github.com/user-attachments/assets/237a066e-faf7-49d7-bba4-042d414d4df9" />

### Clean Up Folder
Here I will delete the shared directory and its contents
The commands I used are
```bash
sudo rm -r /home/shared
sudo ls -ld /home/shared
```
<img width="693" height="58" alt="1b cleanup" src="https://github.com/user-attachments/assets/3db75eb2-702b-489d-bd79-24895eba7810" />

### 1b-2 Reflection Questions
How do Linux permissions differ from Windows ACL? 
Linux uses simple owner, group, and others permission bits, while Windows ACLs allow more granular, per user permission rules.

Whats the effect of chmod 770 vs 750?
Both give owners full access. 770 lets group members write and execute files, while 750 limits groups to read and execute only.

What is the risk of adding users to the sudo group?
Sudo access lets a user run any command as root, bypassing normal permissions, which is risky if misused or compromised.

Why is it important to verify with 'su' and 'whoami'?
They confirm which user is actually active, ensuring permissions are tested realistically instead of assumed to work correctly.

## 1b-3 File Search, Analysis & Archiving in Linux
### Archieve Extraction
Here I will extract the archieved guntenberg.tar.bz2. I had to transfer the file from my host machine to VM
The commands I used are
```bash
scp Gutenberg.tar zxong@192.168.134.128:/home/zxong/
ls -l Gutenberg.tar.bz2
bunzip2 Gutenberg.tar.bz2
tar -xvf Gutenberg.tar
ls -l
```
<img width="644" height="694" alt="1b Gutenberg" src="https://github.com/user-attachments/assets/3e77ff31-e61d-4f1c-9b26-e3dddc734df6" />
<img width="498" height="99" alt="1b extract" src="https://github.com/user-attachments/assets/58ae69a8-5070-475e-897d-646a7619c98a" />

### File Listing of Extracted Directory
Here I will show you the output of ls -l where Gutenberg was extracted to. 
The commands I used are
```bash
ls -l
```
<img width="785" height="472" alt="1b locateGuten" src="https://github.com/user-attachments/assets/a4f07348-a105-4e4f-878b-dce1701637af" />

### Filename Search
Here I will demonstrate filename search
The commands I used are
```bash
find . -name "*.txt"
```
<img width="833" height="194" alt="1b find" src="https://github.com/user-attachments/assets/0fcbbb2e-f882-4fff-9223-31eacf4a417a" />

### Text Seach via Grep
Here I will demonstrate a text search using grep
The commands I used are 
```bash
ls -l
grep -r "verdigris"
```
<img width="820" height="82" alt="1b textsearch" src="https://github.com/user-attachments/assets/32cdfdf8-d6b5-4e2d-923d-64ce4b646240" />

### Contextual Text Search
Here I will demonstrate a contextual text search using grep. There was no phrase matching "Next day there was a surprise for Jack". Thus, there was no output given
The commands I used are
```bash
grep -r -C 3 "Next day there was a surprise for Jack"
```
<img width="818" height="45" alt="1b nooutput" src="https://github.com/user-attachments/assets/5b5e56ac-1fed-4d50-a71b-234336f2d354" />

### Data Based File Search
Here I will demonstrate data based file search using find. find . -type f -printf '%T+ %p\n' lists the files, sort sorts the results with oldest being first and sed -n '3p' prints only the 3rd line 
The command I used are
```bash
find . -type f -printf '%T+ %p\n' | sort | sed -n '3p'
```
<img width="820" height="63" alt="1b databased" src="https://github.com/user-attachments/assets/adecbd00-12c5-4c93-8738-bfa8bc555a8e" />

### Size Based File Search
Here I will demonstrate a file search based on size. soze 255258c has no files, thus, there is no output
The commands I used are
```bash
find . -type f -size 255258c -exec ls -lh {} \;
find . -type f -size +512k -exec ls -lh {} \;
```
<img width="819" height="627" alt="1b sizeba" src="https://github.com/user-attachments/assets/06acb2f6-0524-4fba-9b9c-ce8b67fe37c7" />

### Find Largest File
Here I will demonstrate the Largest File found
The command line I used are 
```bash
du -a . | sort -nr | head
```
<img width="820" height="226" alt="1b largest" src="https://github.com/user-attachments/assets/45abec19-1380-46da-8765-61dc3ec18c11" />

### Text Frequency Analysis Performed
Here I will demonstrate text frequency analysis
The command i used are
```bash
sed -e 's/\s/\n/g' < test.txt | sort | uniq -c | sort -nr | head -200
```
<img width="821" height="100" alt="1b text frequency" src="https://github.com/user-attachments/assets/7cdec179-157a-4a56-84d8-c35425fbbb73" />

### Answers to Questions Provided
How many times does the string “verdigris” appear? (enter a number only) 
1
What is the surname of the author of the filename “1107.txt”? (case sensitive) 
NIL
What is the surname of the author of the file that is exactly 255258 bytes? (case sensitive) 
NIL
What is the filename of the file with the 3rd oldest creation date? 
frankenstein.txt
Find the word that follows the text: “Next day there was a surprise for Jack” (Case-sensitive, no spaces) 
NIL

### 1b-3 Reflection Questions
Which command-line tool was the most useful in solving the questions?  
find was most useful, since it let me search by name, date, and size, covering most of the question types directly.

How might these search tools help in cybersecurity investigations? 
They help investigators quickly locate suspicious files, timestamps, or specific text patterns across large systems without manually checking each file. 

How could scripting improve repetitive search tasks? 
Scripting automates repeated searches, saving time and reducing manual errors compared to retyping similar commands individually each time.

What limitations did you encounter using grep and find? 
Both tools returned no output when searches failed silently, making it hard to tell if a query worked correctly.
 
