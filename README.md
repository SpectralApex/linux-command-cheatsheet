# 🐧 Linux Commands Cheat Sheet

A practical Linux command reference for cybersecurity, ethical hacking, system administration, and daily terminal usage.

---

# 📂 File & Directory Commands

| Command | Description |
|---|---|
| `pwd` | Show current directory |
| `ls` | List files |
| `ls -la` | Detailed list including hidden files |
| `cd folder` | Move into folder |
| `cd ..` | Move back one directory |
| `mkdir test` | Create directory |
| `rmdir test` | Remove empty directory |
| `rm file.txt` | Delete file |
| `rm -rf folder` | Force delete folder |
| `cp file1 file2` | Copy file |
| `mv old new` | Rename or move file |
| `touch file.txt` | Create empty file |
| `tree` | Show directory structure |

---

# 📄 File Viewing Commands

| Command | Description |
|---|---|
| `cat file.txt` | Display file content |
| `less file.txt` | Scroll through file |
| `more file.txt` | View file page by page |
| `head file.txt` | First 10 lines |
| `tail file.txt` | Last 10 lines |
| `tail -f logs.txt` | Live log monitoring |
| `nano file.txt` | Edit file using Nano |
| `vim file.txt` | Edit file using Vim |

---

# 🔍 Searching Commands

| Command | Description |
|---|---|
| `find / -name test.txt` | Find file by name |
| `locate test.txt` | Quickly locate file |
| `grep word file.txt` | Search word in file |
| `grep -r word .` | Recursive search |
| `which python` | Show binary location |
| `whereis bash` | Show binary/source/manual location |

---

# 👤 User & Permission Commands

| Command | Description |
|---|---|
| `whoami` | Current user |
| `id` | User/group IDs |
| `sudo command` | Run as root |
| `su` | Switch user |
| `passwd` | Change password |
| `chmod 755 file` | Change permissions |
| `chmod +x script.sh` | Make executable |
| `chown user:user file` | Change ownership |

---

# 🔐 Linux Permission Basics

| Number | Permission |
|---|---|
| `4` | Read |
| `2` | Write |
| `1` | Execute |

### Example

```bash
chmod 755 script.sh
```

Meaning:

- Owner → `rwx`
- Group → `r-x`
- Others → `r-x`

---

# 🌐 Networking Commands

| Command | Description |
|---|---|
| `ip a` | Show IP addresses |
| `ifconfig` | Network configuration |
| `ping google.com` | Test connectivity |
| `netstat -tulnp` | Open ports/services |
| `ss -tulnp` | Modern netstat alternative |
| `curl https://example.com` | Fetch webpage |
| `wget URL` | Download file |
| `nslookup domain.com` | DNS lookup |
| `dig domain.com` | Advanced DNS query |
| `traceroute google.com` | Route tracing |

---

# ⚙️ Process Management

| Command | Description |
|---|---|
| `ps aux` | Running processes |
| `top` | Real-time processes |
| `htop` | Interactive process viewer |
| `kill PID` | Kill process |
| `kill -9 PID` | Force kill |
| `jobs` | Background jobs |
| `bg` | Resume in background |
| `fg` | Bring to foreground |

---

# 💾 Disk & Storage Commands

| Command | Description |
|---|---|
| `df -h` | Disk usage |
| `du -sh folder` | Folder size |
| `mount` | Mounted drives |
| `lsblk` | Block devices |
| `fdisk -l` | Disk partitions |

---

# 📦 Package Management

## Debian / Ubuntu

| Command | Description |
|---|---|
| `sudo apt update` | Update repositories |
| `sudo apt upgrade` | Upgrade packages |
| `sudo apt install nmap` | Install package |
| `sudo apt remove nmap` | Remove package |

## Fedora / RHEL

| Command | Description |
|---|---|
| `sudo dnf install nmap` | Install package |
| `sudo dnf update` | Update packages |

---

# 🧠 System Information Commands

| Command | Description |
|---|---|
| `uname -a` | Kernel/system info |
| `hostname` | System hostname |
| `uptime` | System uptime |
| `free -h` | RAM usage |
| `lscpu` | CPU information |
| `neofetch` | System summary |

---

# 🔥 Cybersecurity & Ethical Hacking Commands

## Nmap

```bash
nmap 192.168.1.1
nmap -sV target
nmap -A target
nmap -Pn target
```

## Netcat

```bash
nc -lvnp 4444
nc target 80
```

## Wireshark / Tshark

```bash
tshark
```

## Hydra

```bash
hydra -l admin -P passwords.txt ssh://192.168.1.10
```

## Gobuster

```bash
gobuster dir -u http://target -w wordlist.txt
```

---

# 📁 Compression Commands

| Command | Description |
|---|---|
| `zip files.zip file.txt` | Create zip |
| `unzip files.zip` | Extract zip |
| `tar -cvf files.tar folder` | Create tar |
| `tar -xvf files.tar` | Extract tar |
| `tar -czvf files.tar.gz folder` | Create compressed tar |

---

# ⌨️ Useful Shortcuts

| Shortcut | Description |
|---|---|
| `CTRL + C` | Stop process |
| `CTRL + Z` | Suspend process |
| `CTRL + L` | Clear terminal |
| `TAB` | Auto-complete |
| `↑ / ↓` | Command history |
| `history` | Show command history |
| `clear` | Clear screen |

---

# 🧪 Bash Scripting Basics

## Simple Script

```bash
#!/bin/bash

echo "Hello Linux"
```

## Run

```bash
chmod +x script.sh
./script.sh
```

---

# 🚀 Useful Cybersecurity Workflow Commands

## Verify Connectivity

```bash
ping 192.168.16.102
```

## Port Scanning

```bash
nmap -sV 192.168.16.102
```

## Enumerate Services

```bash
netstat -tulnp
```

## Enumerate Users

```bash
cat /etc/passwd
```

## Monitor Traffic

```bash
tcpdump -i eth0
```
