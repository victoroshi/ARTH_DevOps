
# Task 4 Notes

This section demonstrates how to configure nginx as a reverse proxy to forward incoming traffic from port 80 to an application running on port 8080.

---

## Edit Nginx Configuration File

```bash
sudo nano /etc/nginx/sites-available/default
````

### What this does:

* Opens the default nginx configuration file for editing

---

## Configure Reverse Proxy

Inside the `server` block, locate the `location /` section and replace it with:

```nginx
location / {
    proxy_pass http://localhost:8080;
}
```
![Nginx Config and Test](./screenshots/configure-reverse-proxy-and-test.png)

### What this does:

* Forwards all incoming requests on port 80 to the application running on port 8080
* Enables nginx to act as a reverse proxy

---

## Test Nginx Configuration

```bash
sudo nginx -t
```

### What this does:

* Checks for syntax errors in the nginx configuration file
* Ensures the configuration is valid before restarting

---

## Restart Nginx

```bash
sudo systemctl restart nginx
```

### What this does:

* Applies the new configuration changes

---

## Verify Application via Nginx

Open your browser and visit:

```
http://localhost
```
![App via Nginx](./screenshots/verify-app-via-nginx.)

### Expected Result:

* The application running on port 8080 should now be accessible via port 80

---

## Screenshots

> Place your screenshots inside the `screenshots` folder and reference them below.


![Nginx Test](./screenshots/nginx-test.png)


````