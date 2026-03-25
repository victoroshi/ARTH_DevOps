
# Task 1 Notes
This folder contains outputs and explanations for basic Linux setup including user creation, package installation, and system information.


## Commands Used for Task 1
## Create a new user and grant sudo access
``` sudo adduser devopsuser ```
### What this command does:
- sudo: runs command as admin (superuser)
- adduser: creates a new user
- devopsuser: the username to be created
sudo usermod -aG sudo devuser
sudo apt update
sudo apt install -y git curl htop nginx docker.io
lsb_release -a
ip a
free -h
df -h
