# Nmap

Personal reference sheet for using Nmap — a network scanning tool used to discover hosts, open ports, and services on a network.

---

## 📌 What is Nmap?

Nmap (Network Mapper) is one of the most widely used tools in cybersecurity. It allows you to:
- Discover what devices are on a network
- See which ports are open on a target
- Identify what services and versions are running
- Detect the operating system of a target

---

## 🤝 How Nmap Works — The 3-Way Handshake

Nmap uses the TCP 3-way handshake to determine whether a port is open:

```
Step 1 — SYN:      Nmap sends a SYN packet to the target port
Step 2 — SYN/ACK:  If open, the target responds with SYN/ACK
Step 3 — ACK:      Nmap completes the connection with ACK
```

- If the port is **open** → target replies with SYN/ACK
- If the port is **closed** → target replies with RST (reset)
- If the port is **filtered** → no response (likely a firewall)

---

## 🖥️ Basic Syntax

```bash
nmap [options] [target]
```

Target can be:
- A single IP: `192.168.1.1`
- A hostname: `example.com`
- A range: `192.168.1.1-254`
- A subnet: `192.168.1.0/24`

---

## 🔍 Common Scans

| Command | What It Does |
|---|---|
| `nmap 10.10.x.x` | Basic scan of most common ports |
| `nmap -p 80 10.10.x.x` | Scan a specific port |
| `nmap -p 1-1000 10.10.x.x` | Scan a range of ports |
| `nmap -p- 10.10.x.x` | Scan all 65535 ports |
| `nmap -sV 10.10.x.x` | Detect service versions |
| `nmap -O 10.10.x.x` | Detect operating system |
| `nmap -A 10.10.x.x` | Aggressive scan (OS, version, scripts) |
| `nmap -sn 192.168.1.0/24` | Ping sweep — find live hosts |

---

## 🕵️ Scan Types

| Flag | Scan Type | What It Does |
|---|---|---|
| `-sS` | SYN scan | Fast, stealthy — doesn't complete handshake |
| `-sT` | TCP connect | Full 3-way handshake — louder but reliable |
| `-sU` | UDP scan | Scans UDP ports (slower) |
| `-sN` | Null scan | Sends no flags — used to evade firewalls |

---

## ⏱️ Timing Options

Controls how fast or slow the scan runs.

| Flag | Speed | Use Case |
|---|---|---|
| `-T0` | Paranoid | Very slow, avoids detection |
| `-T1` | Sneaky | Slow, avoids detection |
| `-T2` | Polite | Slow, reduces bandwidth |
| `-T3` | Normal | Default speed |
| `-T4` | Aggressive | Fast, used in CTFs |
| `-T5` | Insane | Very fast, may miss results |

---

## 💾 Saving Output

```bash
nmap -oN output.txt 10.10.x.x       # Save as normal text
nmap -oX output.xml 10.10.x.x       # Save as XML
nmap -oG output.grep 10.10.x.x      # Save as grepable format
nmap -oA output 10.10.x.x           # Save in all formats
```

---

## 💡 Useful Tips

- Always use `sudo` for more accurate results: `sudo nmap -sS 10.10.x.x`
- Use `-v` or `-vv` to see results in real time as the scan runs
- In CTFs, `-A -T4` is a reliable starting scan
- Never run Nmap against systems you don't have permission to scan

---

## 🔐 Common Ports to Know

| Port | Service |
|---|---|
| `21` | FTP |
| `22` | SSH |
| `23` | Telnet |
| `25` | SMTP (email) |
| `53` | DNS |
| `80` | HTTP |
| `443` | HTTPS |
| `3306` | MySQL |
| `3389` | RDP (Remote Desktop) |
