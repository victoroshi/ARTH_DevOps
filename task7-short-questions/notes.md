# Task 7 Notes

This section provides concise explanations of key DevOps concepts.

---

## Difference Between Docker Image and Container

- **Docker Image**:
  - A static blueprint or template used to create containers
  - Contains application code, libraries, and dependencies

- **Docker Container**:
  - A running instance of a Docker image
  - Executes the application in an isolated environment

---

## Difference Between systemctl start and systemctl enable

- **systemctl start**:
  - Starts a service immediately
  - Does not persist after reboot

- **systemctl enable**:
  - Configures a service to start automatically at system boot

---

## What is Nginx Reverse Proxy Used For?

- Nginx reverse proxy is used to:
  - Forward client requests to backend servers
  - Improve performance through load distribution
  - Enhance security by hiding backend services

---

## How to Check Which Process is Using a Port in Linux

```bash
lsof -i :PORT
````

### Example:

```bash
lsof -i :80
```

### What this does:

* Displays the process using a specific port

---

## What is AWS EC2 Used For?

* Amazon EC2 is used to:

  * Launch virtual servers in the cloud
  * Host applications and services
  * Provide scalable computing capacity

---

## What is Jenkins Used For?

* Jenkins is an automation server used for:

  * Continuous Integration (CI)
  * Continuous Deployment (CD)
  * Automating build, test, and deployment processes

---

## What is CodePipeline?

* AWS CodePipeline is a service used to:

  * Automate software release processes
  * Build, test, and deploy applications automatically
  * Integrate with other AWS services and CI/CD tools

````