
# Task 1 Notes

This folder contains outputs and explanations for basic Linux setup including user creation, package installation, and system information.
## Create a New User
---

```bash
sudo adduser devopsuser
````
![adding-new-user](./screenshots/adding-new-user.png)
### What this command does:

* `sudo`: runs command as admin (superuser)
* `adduser`: creates a new user
* `devopsuser`: the username to be created

---

## Grant Sudo Access

```bash
sudo usermod -aG sudo devopsuser
```

![create-user-and-add-sudo-access](./screenshots/create-user-and-add-sudo-access.png)

### What it means:

* `usermod`: modify user
* `-aG`: append to group
* `sudo`: admin group

This gives the user admin privileges.

---

## Verify User Group

```bash
groups devopsuser
```

Output should include:

```bash
sudo
```

---

## Update System

```bash
sudo apt update
```

### What it does:

* Fetches latest package lists from internet
* Ensures latest versions are installed

---

## Install Required Packages

```bash
sudo apt install -y git curl htop nginx docker.io
```

### Installs:

* `git` → version control
* `curl` → test APIs/web
* `htop` → system monitor
* `nginx` → web server
* `docker.io` → container tool

`-y` automatically confirms installation.

---

## System Information

### OS Version

```bash
lsb_release -a
```
![OS-Version](./screenshots/OS-Version.png)

---

### IP Address

```bash
ip a
```
![IP-Address](./screenshots/IP-Address.png)

---

### Memory Usage

```bash
free -h
```
![Memory-Usage](./screenshots/Memory-Usage.png)

---

### Disk Usage

```bash
df -h
```
![Disk-Usage](./screenshots/Disk-Usage.png)
