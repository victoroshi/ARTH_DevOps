
# Task 5 Notes

This section documents a troubleshooting scenario encountered during the setup and how it was resolved.

---

## Issue Identified

The application was not accessible via the browser using:

```

http://localhost:8080

````
![Error](./screenshots/application-not-opening.png)

---

## Diagnosis

### Check Running Containers

```bash
docker ps
````
![Check Running Container](./screenshots/app-disgnosis.png)

### What this does:

* Lists all running Docker containers
* Helps confirm whether the application container is active

---

### Check Port Usage

```bash
sudo lsof -i :8080
```

### What this does:

* Checks if port 8080 is being used
* Helps identify port conflicts or inactive services

---

## Root Cause

* The Docker container was not running
  OR
* Incorrect port mapping was used when starting the container

---

## Fix Applied

### Start Existing Container

```bash
docker start <container_id>
```

### OR Run Container Correctly

```bash
docker run -d -p 8080:80 myapp
```

### What this does:

* Starts the container or runs it with correct port mapping
* Ensures the application is exposed properly

---

## Verification

### Test with Curl

```bash
curl http://localhost:8080
```
![Fix Applied](./screenshots/apply-fix-and-verify.png)

### What this does:

* Sends a request to the application
* Confirms it is responding correctly

---

### Browser Test

Open:

```
http://localhost:8080
```
![Successful Output](./screenshots/browser-test.png)

Expected output:

```
<h1>Hello from Docker Application</h1>
<p>This is the web app served inside a Docker container.</p>```
---
