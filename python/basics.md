# Python Basics

Personal reference sheet of core Python concepts for cybersecurity scripting.

---

## 📌 Running Python

| Command | What It Does |
|---|---|
| `python3` | Open interactive Python shell |
| `python3 script.py` | Run a Python file |
| `exit()` | Exit the Python shell |

---

## 📦 Variables & Data Types

```python
name = "Peter"          # String (text)
age = 19                # Integer (whole number)
height = 5.11            # Float (decimal number)
is_hacker = True        # Boolean (True or False)
```

| Type | Example | What It Stores |
|---|---|---|
| `str` | `"hello"` | Text |
| `int` | `42` | Whole numbers |
| `float` | `3.14` | Decimal numbers |
| `bool` | `True / False` | Yes or no values |

---

## 🖨️ Printing Output

```python
print("Hello, World!")
print("My name is", name)
print(f"My name is {name} and I am {age}")   # f-string (most common)
```

---

## ➕ Basic Math Operators

| Operator | What It Does | Example |
|---|---|---|
| `+` | Add | `5 + 3 = 8` |
| `-` | Subtract | `5 - 3 = 2` |
| `*` | Multiply | `5 * 3 = 15` |
| `/` | Divide | `5 / 2 = 2.5` |
| `//` | Floor divide | `5 // 2 = 2` |
| `%` | Remainder | `5 % 2 = 1` |
| `**` | Power | `2 ** 3 = 8` |

---

## 📋 Lists

Stores multiple values in order.

```python
ports = [22, 80, 443, 8080]

print(ports[0])         # 22 (first item)
print(ports[-1])        # 8080 (last item)

ports.append(3306)      # Add to end
ports.remove(22)        # Remove a value
print(len(ports))       # Number of items
```

---

## 📖 Dictionaries

Stores data as key-value pairs.

```python
host = {
    "ip": "192.168.1.1",
    "port": 80,
    "status": "open"
}

print(host["ip"])           # 192.168.1.1
host["port"] = 443          # Update a value
host["protocol"] = "https"  # Add new key
```

---

## 🔀 If Statements

```python
port = 80

if port == 80:
    print("HTTP port")
elif port == 443:
    print("HTTPS port")
else:
    print("Unknown port")
```

### Comparison Operators
| Operator | Meaning |
|---|---|
| `==` | Equal to |
| `!=` | Not equal to |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal |
| `<=` | Less than or equal |

---

## 🔁 Loops

### For Loop — repeat for each item
```python
ports = [22, 80, 443]

for port in ports:
    print(f"Scanning port {port}")
```

### While Loop — repeat until condition is false
```python
count = 0

while count < 5:
    print(f"Attempt {count}")
    count += 1
```

---

## 🧩 Functions

Reusable blocks of code.

```python
def scan_port(port):
    print(f"Scanning port {port}...")

scan_port(80)
scan_port(443)


def add_numbers(a, b):
    return a + b

result = add_numbers(5, 3)
print(result)   # 8
```

---

## 📁 Working With Files

```python
# Read a file
with open("log.txt", "r") as file:
    content = file.read()
    print(content)

# Write to a file
with open("output.txt", "w") as file:
    file.write("Scan complete")

# Append to a file
with open("output.txt", "a") as file:
    file.write("\nNew line added")
```

---

## 📥 User Input

```python
target = input("Enter target IP: ")
print(f"Scanning {target}...")
```

---

## 📚 Importing Libraries

```python
import os               # Operating system commands
import sys              # System functions
import socket           # Networking
import subprocess       # Run terminal commands from Python

# Example — get your hostname
import socket
print(socket.gethostname())
```

---

## 🔐 Cybersecurity Relevant Libraries

| Library | What It Does | Install |
|---|---|---|
| `socket` | Low level networking | Built-in |
| `requests` | Make HTTP requests | `pip install requests` |
| `scapy` | Packet crafting and sniffing | `pip install scapy` |
| `paramiko` | SSH connections | `pip install paramiko` |
| `os` | Interact with the OS | Built-in |
| `subprocess` | Run shell commands | Built-in |

---

## 💡 Good Habits

```python
# Always add comments to explain your code
# This makes it easier to read later

# Use descriptive variable names
target_ip = "192.168.1.1"    # Good
x = "192.168.1.1"            # Bad

# Use f-strings for clean output
print(f"Connecting to {target_ip}...")
```
