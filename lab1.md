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
