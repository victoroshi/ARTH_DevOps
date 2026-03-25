
# Task 3 Notes
This section demonstrates how to create and run a simple web application using Docker, including building an image and exposing it via a port.

---

## Create Application Directory

```bash
mkdir myapp && cd myapp
````

### What this does:

* `mkdir myapp` → Creates a new directory named `myapp`
* `cd myapp` → Moves into the directory

---

## Create HTML File

```bash
nano index.html
```

### Add the following content:

```html
<h1>Hello from Docker Application</h1>
<p>This is the web app served inside a Docker container.</p>
```

### What this does:

* Creates a simple web page that will be served by nginx

---

## Create Dockerfile

```bash
nano Dockerfile
```

### Add the following content:

```dockerfile
FROM nginx:latest
COPY index.html /usr/share/nginx/html/index.html
```

### What this does:

* `FROM nginx:latest` → Uses nginx as the base image
* `COPY` → Replaces the default nginx web page with our custom page

---

## Build Docker Image

```bash
docker build -t myapp .
```
![Docker Build](./screenshots/docker-build.png)

### What this does:

* Builds a Docker image from the Dockerfile
* `-t myapp` → Tags the image with the name "myapp"
* `.` → Uses the current directory as build context

---

## Run Docker Container

```bash
docker run -d -p 8080:80 myapp
```

### What this does:

* `-d` → Runs container in background (detached mode)
* `-p 8080:80` → Maps port 8080 (host) to port 80 (container)
* `myapp` → Name of the image to run

---

## Verify Running Container

```bash
docker ps
```
![Running Container](./screenshots/run-and-verify-running-cointainer.png)

### What this does:

* Lists all running containers

---

## Verify Application in Browser

Open your browser and visit:

```
http://localhost:8080
```
![Application Output](./screenshots/verify-application-in-browser.png)

You should see:

```
Hello from Docker Application
This is the web app served inside a Docker container.
```

---
