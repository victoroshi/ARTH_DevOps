
# Task 2 Notes

This section covers managing services in Linux, specifically starting, enabling, and troubleshooting nginx, as well as checking port usage.

---

## Start Nginx Service

```bash
sudo systemctl start nginx
````

### What this does:

* Starts the nginx web server immediately

---

## Enable Nginx on Boot

```bash
sudo systemctl enable nginx
```

### What this does:

* Ensures nginx starts automatically when the system boots

---

## Check Service Status

```bash
sudo systemctl status nginx
```
![Nginx Status](./screenshots/check-service-status.png)

### What this does:

* Displays whether nginx is running or not
* Shows logs and any error messages

---

## Check Which Process is Using Port 80

```bash
sudo lsof -i :80
```
![Port Check](./screenshots/check-which-process-is-using-port-80.png)

### What this does:

* Lists all processes currently using port 80 (HTTP port)
* Helps identify conflicts if nginx fails to start

---

## Alternative Method to Check Port Usage

```bash
sudo netstat -tulnp | grep 80
```

### What this does:

* Displays active listening ports
* Filters output to show only port 80 usage

---

## Verification

To confirm nginx is working, open a browser and visit:

```
http://localhost
```

You should see the default nginx welcome page.

---
