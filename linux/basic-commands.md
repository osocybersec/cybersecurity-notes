# Linux Basic Commands

Personal reference sheet of essential Linux commands.

---

## 📁 Navigation

| Command | What It Does |
|---|---|
| `pwd` | Print current directory (where am I?) |
| `ls` | List files in current directory |
| `ls -la` | List all files including hidden, with details |
| `cd foldername` | Move into a folder |
| `cd ..` | Go back one folder |
| `cd ~` | Go to home directory |
| `cd /` | Go to root directory |

---

## 📄 File & Folder Management

| Command | What It Does |
|---|---|
| `touch file.txt` | Create an empty file |
| `mkdir foldername` | Create a new folder |
| `cp file.txt /destination` | Copy a file |
| `mv file.txt /destination` | Move or rename a file |
| `rm file.txt` | Delete a file |
| `rm -r foldername` | Delete a folder and everything inside |
| `cat file.txt` | Display contents of a file |
| `nano file.txt` | Open a file in a simple text editor |

---

## 🔍 Finding Things

| Command | What It Does |
|---|---|
| `find / -name file.txt` | Search entire system for a file |
| `grep "word" file.txt` | Search for a word inside a file |
| `grep -r "word" /folder` | Search for a word inside all files in a folder |
| `locate file.txt` | Quickly find a file by name |
| `which python3` | Find where a program is installed |

---

## 👤 Users & Permissions

| Command | What It Does |
|---|---|
| `whoami` | Show current logged in user |
| `id` | Show user ID and group info |
| `sudo command` | Run a command as administrator |
| `su username` | Switch to another user |
| `passwd` | Change your password |
| `chmod 777 file.txt` | Change file permissions |
| `chown user file.txt` | Change file owner |

### Permission Numbers Cheat Sheet
| Number | Permission |
|---|---|
| `7` | Read, write, execute |
| `6` | Read and write |
| `5` | Read and execute |
| `4` | Read only |

---

## 🌐 Networking

| Command | What It Does |
|---|---|
| `ifconfig` | Show network interfaces and IP addresses |
| `ip a` | Modern version of ifconfig |
| `ping google.com` | Test connection to a host |
| `netstat -tulnp` | Show open ports and connections |
| `ss -tulnp` | Modern version of netstat |
| `curl https://example.com` | Fetch content from a URL |
| `wget https://example.com/file` | Download a file from the internet |
| `nmap 10.10.x.x` | Scan a host for open ports |
| `traceroute google.com` | Show the path packets take to a host |

---

## ⚙️ System Info

| Command | What It Does |
|---|---|
| `uname -a` | Show system and kernel info |
| `top` | Show running processes (live) |
| `htop` | Better version of top (may need installing) |
| `df -h` | Show disk space usage |
| `free -h` | Show memory (RAM) usage |
| `ps aux` | List all running processes |
| `kill PID` | Stop a process by its ID |
| `history` | Show command history |
| `clear` | Clear the terminal screen |

---

## 📦 Installing Software (Debian/Ubuntu)

| Command | What It Does |
|---|---|
| `sudo apt update` | Refresh list of available packages |
| `sudo apt upgrade` | Upgrade all installed packages |
| `sudo apt install nmap` | Install a program (e.g. nmap) |
| `sudo apt remove nmap` | Uninstall a program |

---

## 💡 Useful Shortcuts

| Shortcut | What It Does |
|---|---|
| `Ctrl + C` | Stop a running command |
| `Ctrl + L` | Clear the screen |
| `Tab` | Autocomplete a command or filename |
| `↑ Arrow` | Scroll through previous commands |
| `!!` | Repeat the last command |
| `sudo !!` | Repeat last command with sudo |
