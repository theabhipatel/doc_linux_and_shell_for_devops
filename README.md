# 🔥 Deep Dive: Linux & Shell for DevOps

---

## 1️⃣ Linux Basics

👉 Start with basics.

### 🔹 Navigation & Files

- `pwd` → show current path
- `ls -l` → list files with permissions
- `cd` → change directory
- `find / -name "file.txt"` → search files
- `grep "keyword" file.txt` → search inside files

### 🔹 File Operations

- `touch file.txt` → create
- `cp file1 file2` → copy
- `mv file1 file2` → move/rename
- `rm file.txt` → delete
- `cat`, `less`, `head`, `tail -f` (view logs)

### 🔹 Hands-on Practice

- Create a directory `projects/` and practice creating/moving files.
- Use `tail -f /var/log/syslog` to watch logs live.

---

## 2️⃣ Permissions & Ownership 🔒

👉 This is where DevOps engineers often work (managing who can access what).

### 🔹 Key Commands

- `ls -l` → shows `-rw-r--r--` style permissions
- `chmod 755 script.sh` → give execute permissions
- `chown user:group file.txt` → change ownership
- `umask` → default file permissions

### 🔹 Hands-on Practice

- Create a script and make it executable only by you.
- Create a shared directory where only one group can write.

---

## 3️⃣ Processes & Services ⚙️

👉 You’ll manage running apps, databases, and web servers daily.

### 🔹 Process Management

- `ps aux` → list processes
- `top` or `htop` → monitor CPU/memory usage
- `kill -9 PID` → force kill a process

### 🔹 Service Management (systemd)

- `systemctl start nginx` → start a service
- `systemctl status nginx` → check status
- `systemctl enable nginx` → auto-start at boot

### 🔹 Hands-on Practice

- Install **nginx** and start/stop it.
- Run a background process with `&` and kill it.

---

## 4️⃣ Shell Scripting 📝

👉 This is where Linux becomes automation-friendly.

### 🔹 Core Concepts

- Variables: `NAME="Abhi"` → `echo $NAME`
- Conditions:
  ```bash
  if [ -f /etc/passwd ]; then
    echo "File exists"
  fi
  ```
- Loops:
  ```bash
  for user in $(cat users.txt); do
    echo "Creating $user"
  done
  ```
- Functions:
  ```bash
  greet() {
    echo "Hello $1"
  }
  greet Abhi
  ```

### 🔹 Hands-on Projects

1. Write a script to **backup logs** to `/backup/` folder.
2. Script to **check if a service is running**; if not, start it.
3. Script to **monitor disk usage** and alert when >80%.

---

## 5️⃣ DevOps-Specific Linux Skills 🚀

👉 These are things you’ll actually use in pipelines/servers.

- **Environment Variables**: `export PATH=$PATH:/usr/local/bin`
- **Crontab (scheduling)**: `crontab -e` → run scripts at intervals
- **Log Management**: `/var/log/syslog`, `/var/log/nginx/error.log`
- **Networking on Linux**:
  - `netstat -tulnp` or `ss -tulnp` → check open ports
  - `curl -I http://localhost` → test service
  - `ufw allow 8080` → firewall rule

---

## 6️⃣ Real-World Hands-On Projects 💡

Here’s how you connect it to DevOps practice:

1. **Web Server Automation**

   - Write a script to install nginx, start it, and open port 80.

2. **Log Rotation**

   - Script to move yesterday’s logs to `/archive` with a timestamp.

3. **User Management**

   - Script to bulk-create users from a file with proper permissions.

4. **Health Check**
   - Script that checks if `nginx` is running, otherwise restarts it.

--- 
DevOps road map =>
Linux → Git → CI/CD → Cloud → Docker → Kubernetes → Terraform → Monitoring → Security → Scaling.
