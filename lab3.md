# Lab 3 ISEA
## 3a-1 Domain, DNS, and TLS certificates
### Activity 1
### A record created + Domain name registered
<img width="853" height="685" alt="3a duck" src="https://github.com/user-attachments/assets/c0819604-b7aa-4805-aa84-e671b371185a" />

### Apache installed
```bash
sudo systemctl status apache2
sudo ss -tulnp | grep :80
```
<img width="892" height="75" alt="3a grep" src="https://github.com/user-attachments/assets/b54a0be6-2749-4101-99a4-45af4009ce6e" />
<img width="891" height="347" alt="3a apcherunning" src="https://github.com/user-attachments/assets/d17dfbcc-56c2-4a08-aee4-ba2c304fd34e" />

### Public IP to Domain mapping verified
```bash
nslookup zhengxuanweb.duckdns.org
dig zhengxuanweb.duckdns.org
```
<img width="1651" height="881" alt="3a-1 duckweb" src="https://github.com/user-attachments/assets/e01dbb3d-8678-4ae3-b9dc-9113e8ab9031" />

### Screenshot: DNS Test Output
```bash
nslookup zhengxuanweb.duckdns.org
dig zhengxuanweb.duckdns.org
```
<img width="888" height="549" alt="3a nslookup" src="https://github.com/user-attachments/assets/45dc0469-f8bd-4ada-9015-e553976eb1ab" />

## Activity 2
### Certbot installed
<img width="645" height="132" alt="3a certbot" src="https://github.com/user-attachments/assets/2ebe1640-96f8-49fd-90f2-ae5c9c33fc2a" />
<img width="1257" height="419" alt="3a valid cert" src="https://github.com/user-attachments/assets/e403d131-0fed-4224-9df8-47841d362238" />

### HTTPS Enabled on Domain 
<img width="952" height="940" alt="3a https enabled" src="https://github.com/user-attachments/assets/268bdec9-bf0a-4382-85cb-6d9e3c85b93d" />

### Valid TLS Certificate 
<img width="1854" height="882" alt="3a TLS" src="https://github.com/user-attachments/assets/3cc320c1-0d86-4f64-b0b5-75c1cd333f0f" />

### Screenshot: HTTPS with Lock Icon 
<img width="893" height="362" alt="3a lockicon" src="https://github.com/user-attachments/assets/c92a61dd-3026-4f3a-b221-c153c97ab7d3" />

### Screenshot: Certbot Success Message 
```bash
sudo certbot --apache
```
<img width="890" height="218" alt="3a certsuccess" src="https://github.com/user-attachments/assets/295a36a3-8c31-44e4-beea-11651e623a44" />

### Screenshot: Renewal Dry-Run Output 
```bash
sudo certbot renew --dry-run
```
<img width="883" height="168" alt="3a dryrun" src="https://github.com/user-attachments/assets/d5cf3d12-51dd-48ec-87ff-e6025cb23fed" />

### 3a-1 Reflection questions
What is the role of DNS in Internet presence? 
DNS maps human-readable domain names to server IP addresses, letting visitors actually reach their website.

Why does DNS propagation take time?
Changes must spread across cached records on servers worldwide, and caches only refresh after their TTL expires.

How does Let’s Encrypt validate domain ownership?
It asks their server to prove control, usually by serving a specific file or DNS record temporarily.

What are the risks if TLS is not configured on a public-facing site?
Data travels unencrypted, exposing passwords, sessions, and browsers may flag the site as untrusted or insecure.

What could happen if you leave your cloud VM running for months?
It accumulates ongoing charges, and the extended uptime increases exposure to unpatched vulnerabilities and attacks.

## 3ba-2 Enabling HTTPS with Let's Encrypt & Certbot
### Pre-Condition Verified: Domain Points to Server
<img width="1651" height="881" alt="3a-1 duckweb" src="https://github.com/user-attachments/assets/642e177d-6c20-4a36-9ac3-f59e7acf91e7" />
<img width="1249" height="769" alt="3a- duck ips" src="https://github.com/user-attachments/assets/a9b087c3-f56e-42c1-8d00-5798b75a2513" />

### Certbot Installed via Snap 
<img width="892" height="92" alt="3a snapbot" src="https://github.com/user-attachments/assets/4ca45ffd-2496-49a2-94cd-f2a31ccdc2b9" />

### HTTPS Enabled on Apache
<img width="1718" height="961" alt="3a-2 digital cert" src="https://github.com/user-attachments/assets/a2f5e063-e906-48e7-a2b8-09f83b2ecc46" />

### Browser Lock Icon (Secure Connection) 
<img width="893" height="362" alt="3a lockicon" src="https://github.com/user-attachments/assets/f917818f-7759-467e-8ba2-7c8f4e14a918" />

### View Certificate Issuer
<img width="1854" height="882" alt="3a TLS" src="https://github.com/user-attachments/assets/ed126469-1ba8-4f06-bb39-bbbaf0e638e3" />

### Certbot Auto-Renewal Dry Run Successful
<img width="883" height="168" alt="3b dryrun" src="https://github.com/user-attachments/assets/9be30033-47ba-4ee2-8dd1-adf4ad6ec385" />


### 3b-2 Reflection Questions
Why is HTTPS important for modern web applications? 
It encrypts data in transit, protecting logins and sensitive info from interception or tampering.

What entity issued your site’s TLS certificate? 
Let's Encrypt, a free, automated certificate authority, issued the certificate for your domain.

How long is your certificate valid for, and how can it be renewed? 
It's valid 90 days, and renews automatically via Certbot's scheduled background task.

What happens if a certificate expires and is not renewed? 
Browsers show security warnings, block access, and users lose trust in your site.

Why does Let’s Encrypt require port 80 or 443 to be open for verification? 
It confirms you actually control the domain by serving a challenge file publicly.

## 3b-1 Bash Backup Scripting, Cron Jobs & Cloud Export
### Practice Bash Commands Executed 
Output or screenshots showing: 
• echo, variables 
• Arithmetic with (( )) 
• Basic for loop summation 
Commands used
```bash
echo "Hello"

name="zhengxuan"
echo "My name is $name"
a=10
b=5
((sum=a+b))
((difference=a-b))
((product=a*b))
((division=a/b))
echo "a = $a"
echo "b = $b"
echo "Sum = $sum, Difference = $difference, Product = $product, Division = $division"

total=0
for i in 1 2 3 4 5
do
    echo "Adding $i"
    ((total=total+i))
done

echo "Final total is $total"
```
<img width="1851" height="563" alt="3b pracbash" src="https://github.com/user-attachments/assets/64b7a0d3-26d0-411e-9fb7-e6f00f1ad3fa" />

### Test Files & Directories Created 
Commands used
```bash
mkdir -p /home/ubuntu/Documents/folder1
mkdir -p /home/ubuntu/Documents/folder2
echo "This is file 1" > /home/ubuntu/Documents/file1.txt
echo "This is file 2 inside folder1" > /home/ubuntu/Documents/folder1/file2.txt
echo "This is file 3 inside folder 2" > /home/ubuntu/Documents/folder2/file3.txt
echo "This is another test file" > /home/ubuntu/Documents/folder2/file4.txt

ls -R /home/ubuntu/Documents
```
<img width="889" height="301" alt="3b dircreate" src="https://github.com/user-attachments/assets/791d8484-481a-4b87-9c88-be1ef44847fc" />

### Basic Script Working (testscript) 
File /home/ubuntu/testscript created and tested with: 
• Recursive copy from Documents to /home/ubuntu/backup/ 
• Script has execute permission (chmod 777) and produces expected output
Commands used
```bash
nano testscript
chmod 777 /home/ubuntu/testscript
/home/ubuntu/testscript
ls -l /home/ubuntu/testscript
ls -R /home/ubuntu/backup
```
<img width="890" height="360" alt="3b basicScript" src="https://github.com/user-attachments/assets/54d17d65-8ac6-4e29-9369-0eafcdd123fc" />
<img width="1852" height="451" alt="3b runbasicScript" src="https://github.com/user-attachments/assets/a93a38d0-2847-48d8-afc2-92ba428a12f2" />

### Script Moved to /usr/bin and Tested 
Output showing: 
• Script moved to /usr/bin/testscript 
• sudo chown applied 
• testscript works from any directory 
Commands used
```bash
sudo cp /home/ubuntu/testscript /usr/bin/testscript
sudo chown root:root /usr/bin/testscript
sudo chmod 777 /usr/bin/testscript

ls -l /usr/bin/testscript

cd /
testscript
pwd
ls -R /home/ubuntu/backup
```
<img width="1853" height="526" alt="3b scriptmove" src="https://github.com/user-attachments/assets/fe5feb15-fa43-43c4-902a-a4abc8ac6962" />

### ZIP Archive with Date Filename 
Script updated to: 
• Use zip -r to archive backup 
• Use now=$(date +"%d_%m_%y") to name the ZIP file 
• Screenshot of dated ZIP in /home/ubuntu/ 
Commands used
```bash
sudo apt update
sudo apt install zip -y
sudo nano /usr/bin/testscript
testscript

ls -lh /home/ubuntu/*.zip
```
<img width="1851" height="802" alt="3b zipdown" src="https://github.com/user-attachments/assets/10b06672-4bd6-4840-9e32-0c1dae24d51f" />
<img width="1849" height="569" alt="3b zipfile" src="https://github.com/user-attachments/assets/d3989bb7-1fb4-48b6-a11c-3f4847bd75dd" />
<img width="1852" height="368" alt="3b ziprun" src="https://github.com/user-attachments/assets/0f003b24-c7a9-4069-8ce9-e723dc9517d4" />
<img width="1412" height="419" alt="3b zipend" src="https://github.com/user-attachments/assets/dd6ef315-2e71-412c-b4da-a6c6b6cc79bf" />

### Cronjob Set Up for Hourly Backup 
Screenshot or output of /etc/crontab edited to include: 
9 * * * * ubuntu /usr/bin/testscript or similar hourly cron job 
Commands used
```bash
sudo nano /etc/crontab
sudo systemctl status cron
tail -n 10 /etc/crontab
```
<img width="1852" height="733" alt="3b statscron" src="https://github.com/user-attachments/assets/02162b4f-ef8b-426e-82bb-38deec83a28c" />
<img width="1853" height="607" alt="3b cronjob" src="https://github.com/user-attachments/assets/e99a64e0-2a61-4ed7-aeb7-49d5ad0433a0" />
<img width="918" height="215" alt="3b tailcron" src="https://github.com/user-attachments/assets/681bfa43-9928-4bf4-bc18-59e592ac6415" />

### Successful Cron Execution Verified 
Evidence that the script runs every hour: 
• ZIP file created hourly 
• Timestamps or ls -lh output confirming multiple backups created 
<img width="627" height="58" alt="3b evidence" src="https://github.com/user-attachments/assets/73bcded1-f021-405d-ab0f-6b5991ecb73a" />


### SCP to Cloud Working 
Script contains a line using: 
scp -i key.pem $now.zip ubuntu@<server>:~/ 
• Confirmed file reached cloud VM (ls ~/ on remote server) 
Commands used
```bash
cd C:\Users\User\Desktop
scp -i "C:\Users\User\Downloads\ubuntu.pem" ubuntu@13.239.143.151:/home/ubuntu/16_07_26.zip .
dir *.zip
scp -i "ubuntu.pem" "11_07_26.zip" ubuntu@13.239.143.151:/home/ubuntu/
ls -lh /home/ubuntu/*.zip
```
<img width="892" height="53" alt="3b scphere" src="https://github.com/user-attachments/assets/28784f9e-ac84-40b4-9dcb-8cec5bd9cc7f" />
<img width="925" height="215" alt="3b scptocloud" src="https://github.com/user-attachments/assets/8b4058ba-8f49-41c0-ac80-ece88ca96a24" />

### SSH Certificate Accepted by Root 
Output of sudo ssh -i key.pem ... showing manual acceptance of SSH key fingerprint 
Commands used
```bash
cd C:\Users\User\Downloads
scp -i "ubuntu.pem" "ubuntu.pem" ubuntu@13.239.143.151:/home/ubuntu/ubuntu.pem
chmod 400 /home/ubuntu/ubuntu.pem
ssh -i /home/ubuntu/ubuntu.pem ubuntu@13.239.143.151
``` 
<img width="1359" height="669" alt="3b manualaccept" src="https://github.com/user-attachments/assets/aed0b03b-8dce-47d2-a465-792cef9c3fef" />
<img width="936" height="140" alt="3b copypem" src="https://github.com/user-attachments/assets/bd249f6e-6a36-4e0f-9934-55b194cfcd52" />

### Final Script Submitted 
Full contents of script provided, with: 
• Dated ZIP backup 
• SCP transfer 
• Full paths used for cron 
```bash
cat /usr/bin/testscript
```
<img width="892" height="721" alt="3b script2run" src="https://github.com/user-attachments/assets/31e40d1e-33e6-4b71-8467-04293ec9649a" />
<img width="892" height="877" alt="3b script2" src="https://github.com/user-attachments/assets/94499106-5786-40d1-8005-77ec3ddff73d" />

### 3b-1 Reflection Questions
Why is using absolute paths important in scripts run by cron? 
Cron runs with minimal environment variables, so relative paths fail without the full context.

What are the benefits of cloud exporting for backups? 
Offsite copies survive local disasters, hardware failure, or if the original server gets destroyed.

How does cron differ from manual execution? 
Cron runs automatically on schedule without supervision, while manual execution requires them present, triggering it.

What happens if SSH keys are not accepted ahead of time? 
 Cron jobs hang or fail silently, since there's no interactive prompt to confirm host authenticity.

How can login messages help improve user/system engagement? 
They can display reminders, system status, or security notices right when a user connects.

## 3b-2 Additional Server Services
### System Preperation
I first updated the system and installed basic prerequisites if needed. There were some errors but I managed to fix them using sudo apt update --fix-missing
Commands used
```bash
sudo apt update
sudo apt update --fix-missing
sudo apt upgrade -y
sudo apt install -y curl wget gnupg lsb-release ca-certificates
```
<img width="1208" height="808" alt="3b update2" src="https://github.com/user-attachments/assets/5019317d-2d6f-4b8f-abbd-6182e0cefa89" />
<img width="1338" height="684" alt="3b update1" src="https://github.com/user-attachments/assets/adf9a9a6-9357-4f65-8b5b-8d745f7ff62f" />

### Installing MariaDB
First I install MariaDB, start and enable MariaDB, and perform a secure MariaDB installation, then verify MariaDB. When I used sudo mysql-secure-installation, it said command not found. Turns out, the command was sudo mariadb-secure-installation instead. 
```bash
sudo apt install -y mariadb-server mariadb-client
sudo systemctl start mariadb
sudo systemctl enable mariadb
sudo mariadb-secure-installation
sudo mysql -u root -p
SHOW DATABASES;
EXIT;
```
<img width="1584" height="799" alt="3b maria1" src="https://github.com/user-attachments/assets/95a8ec18-e151-432e-b20e-c03108e120b9" />
<img width="1852" height="837" alt="3b maria2" src="https://github.com/user-attachments/assets/9be4270d-f4fc-480e-a6d5-f48f8422a8b1" />


### Installing NTP Server
Here I install NTP Server for time synchronisation. No troubles encountered.
```bash
sudo apt update
sudo apt install -y chrony
sudo nano /etc/chrony/chrony.conf
sudo systemctl restart chrony
sudo systemctl enable chrony
chronyc sources
timedatectl
```
<img width="1572" height="637" alt="3b ntp2" src="https://github.com/user-attachments/assets/91d09443-e406-4319-bf80-d9ac238b1c20" />
<img width="1853" height="885" alt="3b ntp" src="https://github.com/user-attachments/assets/fea19047-34c0-44bc-8ffd-4be7e8669fe1" />


### DHCP Server
Here I will install DHCP Server and assign the ip
```bash
sudo apt install -y isc-dhcp-server
sudo nano /etc/default/isc-dhcp-server
sudo nano /etc/dhcp/dhcp.conf
sudo systemctl restart isc-dhcp-server
sudo systemctl enable isc-dhcp-server
systemctl status isc-dhcp-server
```
<img width="1329" height="650" alt="3b dhcp1" src="https://github.com/user-attachments/assets/9684fc08-0eaf-4a05-a7af-bfca6a41e384" />
<img width="1852" height="837" alt="3b dhcp2" src="https://github.com/user-attachments/assets/cee47358-becb-4d47-b9e2-87a89d409956" />
<img width="1852" height="829" alt="3b dhcp3" src="https://github.com/user-attachments/assets/f01ba75c-ede2-4328-be17-835e9c138c03" />
<img width="1328" height="815" alt="3b dhcp4" src="https://github.com/user-attachments/assets/37b5aaf1-8516-45a2-84dd-ff833ba12a73" />

### Installing NFS Server
Here I will install NFS Server, created shared directory, and configure NFS export
```bash
sudo apt install -y nfs-kernel-server
sudo mkdir -p /srv/nfs/share
sudo chown nobody:nogroup /srv/nfs/share
sudo chmod 777 /srv/nfs/share
sudo nano /etc/exports
sudo exportfs -a
sudo systemctl restart nfs-kernel-server
sudo systemctl enable nfs-kernel-server
showmount -e localhost
```
<img width="889" height="160" alt="3b installnfs" src="https://github.com/user-attachments/assets/710166ec-c35e-4acf-99ca-043ff7d07d2f" />
<img width="1851" height="828" alt="3b nfs1" src="https://github.com/user-attachments/assets/efdda1c5-e187-462f-ba62-5fa0b22b83ee" />
<img width="890" height="358" alt="3b nfs2" src="https://github.com/user-attachments/assets/605ffea7-f8fd-4295-a0c9-1de3f34d809f" />

### Installing Samba
Here I will install Samba, create shared folder, configure samba share, and verify. When I tried to run smbclient -L localhost -N, it said I had to install. So i ran sudo apt install smbclient command to install it, then I had no other errors.
```bash
sudo apt install -y samba
sudo mkdir -p /srv/samba/share
sudo chmod 777 /srv/samba/share
sudo nano /etc/samba/smb.conf
sudo systemctl restart smbd
sudo systemctl enable smbd
smbclient -L localhost -N
```
<img width="890" height="233" alt="3b installsamba" src="https://github.com/user-attachments/assets/727245b1-1d0a-4f4c-b31c-2b24044646da" />
<img width="1852" height="833" alt="3b sambaconf" src="https://github.com/user-attachments/assets/6e02cbfe-8205-4806-b561-8a4df3fcc178" />
<img width="914" height="58" alt="3b sambacon" src="https://github.com/user-attachments/assets/e4a8db4a-205e-415d-8c26-74834cc3182a" />
<img width="1171" height="237" alt="3b sambafinal" src="https://github.com/user-attachments/assets/7bea1567-8534-4ab0-8810-1183fe88e2e0" />

