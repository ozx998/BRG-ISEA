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

### Public IP to Domain mapping verified

```bash
nslookup zhengxuanweb.duckdns.org
dig zhengxuanweb.duckdns.org
```

### Screenshot: Apache Welcome Page via Domain
Apache Welcome Page via Domain name

### Screenshot: DNS Test Output
```bash
nslookup jadenwebapp.duckdns.org
dig jadenwebapp.duckdns.org
```

## Activity 2
### Certbot installed


### HTTPS Enabled on Domain 


### Valid TLS Certificate 


### Screenshot: HTTPS with Lock Icon 


### Screenshot: Certbot Success Message 
```bash
sudo certbot --apache
```

### Screenshot: Renewal Dry-Run Output 
```bash
sudo certbot renew --dry-run
```

### 3a-1 Reflection questions
What is the role of DNS in Internet presence? 

Why does DNS propagation take time?

How does Let’s Encrypt validate domain ownership?

What are the risks if TLS is not configured on a public-facing site?

What could happen if you leave your cloud VM running for months?

## 3ba-2 Enabling HTTPS with Let's Encrypt & Certbot
### Pre-Condition Verified: Domain Points to Server

### Certbot Installed via Snap 

### HTTPS Enabled on Apache

### Browser Lock Icon (Secure Connection) 

### View Certificate Issuer

### Certbot Auto-Renewal Dry Run Successful

### 3b-2 Reflection Questions
Why is HTTPS important for modern web applications? 

What entity issued your site’s TLS certificate? 


How long is your certificate valid for, and how can it be renewed? 


What happens if a certificate expires and is not renewed? 


Why does Let’s Encrypt require port 80 or 443 to be open for verification? 

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

cd / testscript
pwd
ls -R /home/ubuntu/backup
```

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

### Cronjob Set Up for Hourly Backup 
Screenshot or output of /etc/crontab edited to include: 
9 * * * * ubuntu /usr/bin/testscript or similar hourly cron job 
Commands used
```bash
sudo nano /etc/crontab
sudo systemctl status cron
tail -n 10 /etc/crontab
```

### Successful Cron Execution Verified 
Evidence that the script runs every hour: 
• ZIP file created hourly 
• Timestamps or ls -lh output confirming multiple backups created 


### SCP to Cloud Working 
Script contains a line using: 
scp -i key.pem $now.zip ubuntu@<server>:~/ 
• Confirmed file reached cloud VM (ls ~/ on remote server) 
Commands used
```bash
cd C:\Users\User\Desktop
scp -i "ubuntu.pem" ubuntu@13.239.143.151:/home/ubuntu/*.zip .
dir *.zip
scp -i "ubuntu.pem" "11_07_26.zip" ubuntu@13.239.143.151:/home/ubuntu/
ls -lh /home/ubuntu/*.zip
```

### SSH Certificate Accepted by Root 
Output of sudo ssh -i key.pem ... showing manual acceptance of SSH key fingerprint 
Commands used
```bash
scp -i "ubuntu.pem" "ubuntu.pem" ubuntu@13.239.143.151:/home/ubuntu/ubuntu.pem
chmod 400 /home/ubuntu/ubuntu.pem
sudo ssh -i /home/ubuntu/key.pem ubuntu@13.239.143.151
```

### Final Script Submitted 
Full contents of script provided, with: 
• Dated ZIP backup 
• SCP transfer 
• Full paths used for cron 
```bash
cat /usr/bin/testscript
```

### 3b-1 Reflection Questions
Why is using absolute paths important in scripts run by cron? 


What are the benefits of cloud exporting for backups? 


How does cron differ from manual execution? 


What happens if SSH keys are not accepted ahead of time? 
 

How can login messages help improve user/system engagement? 

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
