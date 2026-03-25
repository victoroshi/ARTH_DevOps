
# Task 1 Notes
This folder contains outputs and explanations for basic Linux setup including user creation, package installation, and system information.


## Commands Used for Task 1
## Create a new user and grant sudo access
```bash
sudo adduser devopsuser
### What this command does:
- sudo: runs command as admin (superuser)
- adduser: creates a new user
- devopsuser: the username to be created
## Grant Sudo Access
bash sudo usermod -aG sudo devopsuser
### What it means:
- usermod: modify user
- -aG: append to group
- sudo: admin group
This gives the user admin privileges
### Verify
bash groups devopsuser
Output should include:
bash sudo
### Update system
bash sudo apt update
### Waht it does
- Fetches latest package lists from internet
- Ensures latest version is installed
## Install Required Packages
bash sudo apt install -y git curl htop nginx docker.io
### Installs
git:	version control
curl:	test APIs/web
htop:	system monitor
nginx:	web server
docker.io:	container tool
The -y Automatically says YES to installation prompts
## Ssytem Information
lsb_release -a
### IP Address
bash ip a
### Memoru Usage
bash free -h
### Disk Usage
df -h
