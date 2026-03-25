# Task 6 Notes

This section demonstrates creating a simple shell script to check system health, including disk usage, memory usage, nginx status, and application port availability.

---

## Create Script File

```bash
nano check.sh
````

### What this does:

* Creates and opens a new file named `check.sh` for editing

---

## Script Content

```bash
#!/bin/bash

echo "Disk Usage:"
df -h

echo "Memory Usage:"
free -h

echo "Nginx Status:"
systemctl status nginx | grep Active

echo "Application Port Check:"
ss -tulnp | grep 8080
```

---

## Explanation of Script

* `#!/bin/bash` → Specifies the script should run using Bash shell
* `echo` → Prints text to the terminal
* `df -h` → Shows disk usage in human-readable format
* `free -h` → Displays memory usage
* `systemctl status nginx | grep Active` → Shows nginx status (running or not)
* `ss -tulnp | grep 8080` → Checks if port 8080 is listening

---

## Make Script Executable

```bash
chmod +x check.sh
```

### What this does:

* Grants permission to execute the script

---

## Run Script

```bash
./check.sh
```

### What this does:

* Executes the script and displays system information

---

## Screenshots

> Place your screenshots inside the `screenshots` folder and reference them below.

![Script Creation](./screenshots/script-create.png)

![Script Output](./screenshots/script-output.png)

````