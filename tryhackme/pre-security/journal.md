# Day 1 — July 27, 2026
##  Setup & Environment
- Installed **WSL + Ubuntu**
- Installed CLI tools: `nmap`, `curl`, `wget`, `git`, `netcat`, `python3`, `pip`
- Created Python virtual environment at `~/cybersec-lab/venv`
- Installed Python packages: `requests`, `beautifulsoup4`
- Set up **VS Code** with the WSL extension
- Configured VS Code integrated terminal to default to **Ubuntu** instead of PowerShell
- Created **TryHackMe** account
- Initialized tracking checklist at `~/cybersec-lab/learning-checklist.md`

##  Notes & Concepts
- **WSL:** Understood why having a native Linux environment on Windows is essential for security tool compatibility.
- **`sudo`:** Learned why administrative privileges are required for system-level package management.
- **Virtual Environments (`venv`):** Learned how isolated Python environments prevent dependency conflicts between system packages and lab projects.
- **Shell Differences:** Recognized operational differences between PowerShell and the Ubuntu Bash terminal. 

# Day 2-3 — July 29-30 2026
##  Introduction to Cybersecurity and Computer Fundamentals
### Computer System
- Desktop vs. Laptop: Recognized performance differences; desktops prioritize cooling and sustained power, while laptops sacrifice power for mobility and battery life.
- Workstations: Identified high-end desktop systems optimized for precision, stability, and high-performance computing using specialized components (like ECC memory).
- Servers: Understood headless systems built for high availability ($99.999\%$ uptime) that run 24/7 to serve files, websites, or applications to network clients.
- IoT & Embedded Systems: Distinguished between IoT devices (network-connected, single-purpose hardware like smart sensors) and Embedded systems (offline microchips built into appliances).
- Engineering Trade-offs: Learned how mobility, reliability, and cooling dictate system hardware selection for different IT workloads.

### Computer Types
- CPU (Central Processing Unit): Acts as the brain; executes instructions, performs calculations, and controls operations.
- RAM (Random Access Memory): Functions as short-term memory; volatile storage holding active programs and data for fast CPU access.
- Storage (SSD/HDD): Acts as long-term memory; non-volatile storage keeping the OS, apps, and files saved permanently.
- Motherboard & PSU: The motherboard serves as the nervous system connecting components, while the Power Supply Unit (PSU) acts as the heart delivering electrical current.
- UEFI / BIOS Firmware: Low-level software stored on motherboard chips that initializes hardware components before handing over control. Replaced legacy BIOS.
- POST (Power-On Self Test): Diagnostics run by UEFI to verify hardware integrity (RAM, CPU, peripherals) before system startup.
- The Boot Sequence: Hardware initializes via PSU $\rightarrow$ UEFI starts $\rightarrow$ POST executes $\rightarrow$ Boot Device selected $\rightarrow$ Bootloader transfers OS into RAM.

## Client Server 
- **Client & Server:** The client initiates network requests (e.g., web browser), while the server listens for connections and provides resources.
- **Request & Response:** Communication loop where clients ask for resources and servers return data along with status codes (e.g., `200 OK` or `404 Not Found`).
- **Protocol:** A standardized set of rules, syntax, and formatting that allows computers to understand each other (e.g., HTTP, HTTPS, FTP).
- **Port:** Virtual channels identifying specific services running on a server (e.g., Port 80 for HTTP, Port 443 for HTTPS).
- **DNS & IP Address:** DNS resolves human-friendly domain names (`site.com`) into numerical IP addresses (`192.168.1.10`) so packets can reach their destination.

## HTTP Protocol Basics
- **HTTP Methods (Commands):** Define the action a client wants to perform on a server resource.
- **`GET`:** Retrieves data/pages without modifying server state (Read).
- **`POST`:** Sends data to create new resources or submit forms (Create).
- **`PUT` / `PATCH`:** Updates server resources (`PUT` replaces fully, `PATCH` modifies partially).
- **`DELETE`:** Removes specified files or data from the server.
- **`HEAD` & `OPTIONS`:** Diagnostic requests (`HEAD` fetches response headers only; `OPTIONS` checks allowed server methods).

## GET
- **Scheme:** Defines the communication protocol used (`http://` vs. `https://`).
- **Host:** The domain name identifying the server target.
- **Filename / Path:** Specifies the exact resource requested from the server (`/` defaults to `index.html`).
- **IP Address (127.0.0.1):** The network address of the host (`127.0.0.1` is localhost/your local machine).
- **HTTP Status Codes:** Server feedback on request results (e.g., `200 OK` for success, `404 Not Found` for missing resources).

# Day 4 — July 31, 2026

## Computer Fundamentals
## Virtualisation Basics
- Virtualisation: Technology allowing a single physical server to safely share hardware (CPU, RAM, storage) across multiple virtual environments.
- Hypervisor: Core management software layer that divides physical hardware, enforces isolation, and manages VM lifecycles (start, stop, clone, delete).
- Type 1 Hypervisor (Bare-Metal): Installs directly on physical server hardware (e.g., ESXi, Proxmox); fast and efficient for enterprise data centers.
- Type 2 Hypervisor (Hosted): Runs as an application inside an existing host OS (e.g., VirtualBox, VMware Workstation); ideal for desktop labs and learning.
- Virtual Machines (VMs): Emulated systems running their own complete operating system (Windows, Linux) isolated from other VMs and the host.
- Containers: Lightweight environments that package a single application and its dependencies, sharing the host OS kernel instead of virtualizing a full OS.
- Cybersecurity Applications: Isolating untrusted malware in sandbox VMs and running multi-OS security labs (like Kali Linux) safely.

## Cloud Computing Basics
### Cloud Benefits & Characteristics
- Scalability: Easily scale computing resources up or down based on application demand.
- On-Demand Self-Service: Instantly provision or remove servers and storage without waiting for physical hardware installation.
- Pay-As-You-Go: Eliminates upfront hardware costs by charging strictly based on resource usage.
- High Availability & Security: Guarantees continuous uptime during component failures while leveraging strong cloud provider security controls.
- Global Access: Deploys applications globally to ensure access for users anywhere in the world.

### Cloud Deployment Models
- Public Cloud: Shared infrastructure managed by third-party providers; cost-effective and highly scalable for most general use cases.
- Private Cloud: Dedicated infrastructure built for single organizations; provides maximum control, customization, and strict compliance for sensitive data.
- Hybrid Cloud: Combines public and private clouds to keep sensitive operations private while bursting to the public cloud during high traffic.

### Cloud Service Models
- Infrastructure as a Service (IaaS): Rents fundamental resources (VMs, storage, networking); user manages OS, apps, and data, while provider manages hardware.
- Platform as a Service (PaaS): Provider manages the underlying hardware, network, and OS; user focuses strictly on writing and deploying application code.
- Software as a Service (SaaS): Complete end-user applications delivered over the web (e.g., Gmail, Zoom); provider manages all underlying infrastructure and application code.

# Day 5 — August 3, 2026
## Operating System Introduction

- Operating System (OS): Core software coordinating hardware, applications, and users into a unified system.

### System Privilege Layers
- Kernel Space: Unrestricted core of the OS with direct hardware access.
- User Space: Restricted environment where standard applications run.
- System Calls: Requests from user applications asking the kernel to perform hardware tasks.

### OS Responsibilities
- Process Management: Schedules CPU time across programs for smooth multitasking.
- Memory Management: Allocates RAM and uses virtual memory when RAM runs low.
- File System Management: Controls directories, file paths, metadata, and permissions.
- User Management: Authenticates logins and enforces account privacy.
- Device Management: Employs drivers to standardise hardware interactions.

### OS Security & Interfaces
- Security Controls: Enforces authentication, file permissions, space isolation, and system protection.
- Interfaces: Offers visual interaction via GUI or direct command-line control via CLI.

### OS Types
- Desktop OS: General-purpose computing (Windows, macOS, Linux).
- Server OS: Built for continuous uptime and hosting (Windows Server, Linux Server, Unix).
- Mobile OS: Touch-optimized for battery efficiency (Android, iOS).
- Embedded / RTOS: Lightweight, task-specific systems with instant execution (Embedded Linux, FreeRTOS).
- Cloud / Container OS: Minimal systems optimized for virtual workloads (Amazon Linux, Alpine Linux).

# Windows Basics
## Windows Interface & Built-In Tools
- Desktop: Workspace for hosting files, folders, and application shortcuts.
- Taskbar: Navigation bar for switching open applications and accessing notifications.
- Start Menu: Primary launcher for applications, system settings, and power controls.
- Search: Quick access tool for locating applications, settings, and files.
- File Explorer: Graphical file manager used to browse and organize directory structures.
- Windows Update: Servicing engine for applying OS patches, security updates, and driver fixes.
- Microsoft Store: Marketplace for downloading and managing verified application packages.
- Windows Settings: Modern control portal for system, device, and network preferences.
- Control Panel: Legacy management console for advanced system configurations.
- Task Manager: System utility for monitoring real-time processes, memory, and performance.
- Windows Security: Management dashboard for native antivirus and threat protection tools.
- Windows Defender Firewall: Network filtering service for monitoring inbound and outbound traffic.

# Day 6,7,8 — August 4-6, 2026
## Linux CLI Basics
### File System Navigation & Operations
- `pwd`: Print Working Directory; displays the absolute path of your current directory.
- `ls -la`: Lists all directory contents (including hidden files starting with `.`) with detailed permissions, ownership, and file sizes.
- `cd <path>`: Change Directory; navigates to a target folder (`cd ..` moves up one level, `cd ~` goes to home directory).
- `mkdir <folder>` & `rmdir <folder>`: Creates a new directory / Removes an empty directory.
- `touch <filename>`: Creates an empty file or updates the timestamp of an existing file.
- `cp <src> <dest>` & `mv <src> <dest>`: Copies files or directories / Moves or renames files and directories.
- `rm -rf <path>`: Recursively and forcefully deletes files and folders (use with caution).

### File Viewing & Text Processing
- `cat <file>`: Outputs the entire contents of a file directly to the terminal.
- `less <file>`: Opens a file in a scrollable, paginated reader (press `q` to exit).
- `head -n 10 <file>` & `tail -n 10 <file>`: Displays the first or last 10 lines of a file (`tail -f` monitors live log updates).
- `grep "<pattern>" <file>`: Searches for specific text or regular expressions within a file or command output.

### Permissions & System Ownership
- `chmod <permissions> <file>`: Modifies file read, write, and execute permissions (e.g., `chmod +x script.sh` makes a file executable).
- `chown <user>:<group> <file>`: Changes the owner user and group of a specified file or directory.
- `sudo <command>`: Executes a command with elevated root (administrative) privileges.

### System Enumeration & Networking
- `whoami` & `id`: Displays your current active username, user ID (UID), and assigned security groups.
- `uname -a`: Prints detailed kernel and system architecture information.
- `ps aux`: Lists all active running processes across the system.
- `top` / `htop`: Displays real-time CPU, RAM, and process activity.
- `ip a` (or `ifconfig`): Displays active network interface configurations and assigned IP addresses.
- `netstat -tuln` (or `ss -tuln`): Lists active listening ports and services on the machine.
- `man <command>`: Opens the full system manual page for detailed documentation (press `q` to exit).
- `-h` / `--help`: Flag appended to commands to print short usage instructions directly in the console.
- `apropos <keyword>`: Searches manual page descriptions to discover commands related to a query.
- `ssh <user>@<ip>`: Establishes an encrypt.ed remote shell session to a host over network Port 22.
- `history`: Outputs the chronological log of previously executed terminal commands; use `!<number>` to rerun an entry.
- `su -`: Switches user to the `root` administrative account while fully initializing the root environment and login profile

# Windows CLI Basics
### Core Command Prompt (CMD) Commands
- `cd <path>`: Navigates between directory structures (`cd ..` moves up one level, `cd \` moves to drive root).
- `dir`: Lists files and directories within the current working folder (displays attributes, modification date, and file sizes).
- `dir /a`: Displays all files and folders, including hidden and system files.
- `type <filename>`: Outputs the contents of a text file directly to the console (equivalent to Linux `cat`).
- `whoami`: Displays the currently logged-in user account name.
- `whoami /priv`: Lists assigned user privileges and security rights for the active session.
- `systeminfo`: Provides detailed system configuration information, including OS version, architecture, and installed updates.
- `hostname`: Displays the fully qualified domain name of the computer.
- `ipconfig` & `ipconfig /all`: Displays basic network configuration; `/all` provides detailed interface settings, DNS servers, and MAC addresses.
- `netstat -an`: Shows all active network connections and listening ports in numerical format.
- `net user`: Lists all local user accounts created on the operating system.
### PowerShell Essentials
- `Get-Location` (alias `pwd` / `gl`): Displays the current working directory path.
- `Get-ChildItem` (alias `dir` / `ls`): Retrieves items and child elements in the specified directory location.
- `Get-Content <file>` (alias `cat` / `type`): Reads and displays text file contents.
- `Get-Service`: Lists all installed system services and their current operational status (Running / Stopped).
- `Get-Process`: Displays active processes running on the machine along with memory and CPU utilization.
- `Get-Help <cmdlet>`: Accesses integrated documentation and usage examples for specific PowerShell commands.

# Day 9 — August 7, 2026
## Operating System Security
### The CIA Triad
* `Confidentiality` — Ensures secret, private files and sensitive data are accessible **only** to authorized users.
* `Integrity` — Guarantees that files and network transmissions remain accurate and cannot be altered or tampered with by unauthorized parties.
* `Availability` — Ensures systems, services, and data are operational and accessible whenever legitimate users need them.
---
### Key System Vulnerabilities
1. `Authentication Failures` — Weak, reused, or stolen passwords allow unauthorized users to breach system boundaries and compromise accounts.
2. `Weak File Permissions` — Misconfigured access rights (such as overly permissive read/write flags) expose sensitive files to unauthorized local users or processes.
3. `Malicious Programs (Malware)` — Viruses, trojans, and ransomware designed to compromise system integrity, spy on sensitive data, or deny system access.
---
### Privilege Management & Administration
* `root` *(The Superuser / "Boss")* — The top-level administrative account in Unix/Linux systems with unrestricted access to all files, processes, and system configurations.
* `sudo` *(Superuser Do / "Ask Permission")* — A utility that allows authorized users to temporarily execute administrative commands with elevated privileges, adhering to strict security policies without needing to log in directly as `root`.

# Day 10 — August 9, 2026
## Data Representation 
* `Bit` — Short for binary digit; the fundamental unit of data holding either a `0` or a `1`.
* `Byte` — A sequence of 8 bits (also called an *octet*), capable of representing 256 distinct values ($2^8 = 256$).
* `Binary` *(Base-2)* — Uses only two symbols (`0` and `1`). Each position corresponds to a power of 2 ($1, 2, 4, 8, 16, 32, 64, 128$).
* `Octal` *(Base-8)* — Uses digits `0–7`. Groups binary bits into sets of 3 ($2^3 = 8$; place values $1, 8, 64$).
* `Decimal` *(Base-10)* — Standard human counting system using digits `0–9`. Place values increase by powers of 10 ($1, 10, 100$).
* `Hexadecimal` *(Base-16)* — Uses characters `0–9` and `A–F` ($A=10, B=11, C=12, D=13, E=14, F=15$). Groups binary bits into sets of 4 ($2^4 = 16$). A 2-digit hex pair represents a full 8-bit byte.
---
### Hex Colors & RGB Representation
* `Hex Color Code` — A 6-character hexadecimal string representing red, green, and blue light intensity (`#RRGGBB`).
* `RGB (Red, Green, Blue)` — Combines 3 color channels, each assigned 1 byte (8 bits / 2 hex digits), offering 256 levels of intensity per channel ($0\text{–}255$).
* `Color Spectrum` — $256 \times 256 \times 256 = 16,777,215$ total color combinations (~17 million).
  * Example: `#FFFFFF` (Max Red `FF`, Max Green `FF`, Max Blue `FF`) = `rgb(255, 255, 255)` (Pure White).

# Day 11 — August 10, 2026
## Data Encoding
* `Encoding` — The process of converting data from one format into another for efficient storage, processing, and transmission.
---
### Character Encodings & Standards
* `ASCII (American Standard Code for Information Interchange)` — A 7-bit character encoding standard that defines 128 characters, covering standard English letters, numbers (`0–9`), and basic punctuation marks.
* `Unicode` — A universal character encoding standard that assigns a unique number (code point) to every character across all modern and historical writing systems worldwide. It allows different languages and special characters to coexist seamlessly within a single file or message without requiring language-specific standards.
---
### UTF (Unicode Transformation Format)
UTF defines how Unicode code points are stored as bytes in memory or transmitted across networks:
* `UTF-8` *(Variable-Length: 1–4 Bytes)*
  * Uses 1 to 4 bytes per character based on complexity.
  * Fully backward-compatible with original 7-bit ASCII (uses 1 byte for English/ASCII characters).
  * Highly efficient—used by nearly 90% of all websites globally because it saves space on standard English text while supporting all international scripts and emojis.
* `UTF-16` *(Variable-Length: 2 or 4 Bytes)*
  * Uses either 2 or 4 bytes per character.
  * Offers better storage efficiency for languages with large character sets, such as Chinese, Japanese, and Korean (CJK).
  * Commonly used internally within operating systems like **Windows** and programming environments like **Java** and **JavaScript**.
* `UTF-32` *(Fixed-Length: 4 Bytes)*
  * Uses a fixed 4 bytes (32 bits) for every character regardless of complexity.
  * Simplifies internal processing for certain software applications because every character occupies the exact same memory offset.
  * Consumes significant memory, making it highly inefficient for general file storage and web transmission.

  # Day 12 — August 11, 2026
## Python Simple Demo
- **Python**: A high-level, interpreted programming language known for its readability and versatility.
# Programming Fundamentals (Python Overview)
### Core Pillars of Imperative Programming
* **Variables** — Used to store data in memory (e.g., target IP addresses, passwords, or status codes).
* **Conditionals (`if` / `else`)** — Allow the program to make decisions based on specific conditions (e.g., checking if a login request succeeded).
* **Loops (`while`)** — Repeat a block of code continuously as long as a specified condition remains true (e.g., attempting passwords from a list until the correct one is found).
---
### Key Takeaways for Cybersecurity
* **Reading > Writing:** As a beginner in cybersecurity, focus on **understanding and explaining** how a program flows rather than writing code completely from scratch.
* **Practice Over Memorization:** Syntax writing requires practice over time, but recognizing logic patterns is what matters immediately for security work.
* **Language Flexibility:** Core concepts (variables, conditionals, loops) are universal across languages. Modern web applications heavily use **JavaScript** (in browsers for interactivity and server-side via Node.js), so comparing how different languages structure these concepts helps broaden your technical perspective.

# Day 13 — August 12, 2026
## JavaScript Simple Demo
- **JavaScript**: A high-level, interpreted scripting language primarily used to build interactive web applications and power server-side logic (Node.js).
# Programming Fundamentals (JavaScript Overview)
### Core Pillars of Imperative Programming
* **Variables (`let` / `const`)** — Used to store dynamic data in memory (e.g., session tokens, target ports, or user roles).
* **Conditionals (`if` / `else` & `switch`)** — Allow the program to evaluate rules or select exact choices (e.g., checking if user permissions are set to `"admin"` or matching HTTP status codes).
* **Loops (`while` & `for`)** — Repeat code continuously based on a condition (`while`) or iterate over a fixed range/list (`for`) (e.g., iterating through network ports from `20` to `22` until an open port is discovered).
---
### Key Takeaways for Cybersecurity
* **Web Exploitation Foundation:** JavaScript powers the web. Understanding client-side JavaScript is essential for identifying vulnerabilities like Cross-Site Scripting (XSS) and client-side authentication bypasses.
* **Template Literals:** Always use backticks (`` `...` ``) instead of standard quotes when injecting variables into strings using `${variable}` format.
* **Logic Over Memorization:** Searching for syntax (e.g., looking up `prompt()` vs Python's `input()`) is standard practice for professional developers and security analysts—focusing on algorithm design matters most.

# Day 14 — August 14, 2026
## Database SQL Basics
- **SQL (Structured Query Language)**: A standardized programming language used to manage and manipulate relational
- DBMS (Database Management Systems). It allows users to create, read, update, and delete (CRUD) records efficiently.
* **Tables** — Structured collections of data organized into rows and columns, representing specific entities (e.g., user accounts, access logs, or system credentials).
* **Rows (Records / Tuples)** — Individual horizontal entries within a table containing data for each defined field (e.g., a single user's profile details).
* **Columns (Fields / Attributes)** — Vertical structures that define specific data types and categories stored across all records (e.g., `username`, `password_hash`, or `ip_address`).

### Core SQL Commands
* `SELECT` — Retrieves specific data from one or more tables based on defined criteria.
* `INSERT` — Adds new records into a table.
* `UPDATE` — Modifies existing records in a table based on specified conditions.
* `DELETE` — Removes records from a table based on defined criteria.
* `CREATE TABLE` — Defines a new table structure with specified columns and data types.
* `ALTER TABLE` — Modifies an existing table's structure (e.g., adding or removing columns, changing data types).
* `DROP TABLE` — Permanently deletes a table and all its data from the database.
* `JOIN` — Combines rows from two or more tables based on a related column, allowing for complex queries across multiple datasets.
* `WHERE` — Filters records based on specified conditions, enabling targeted data retrieval.
* `GROUP BY` — Aggregates records with similar values in specified columns, often used with aggregate functions like `COUNT`, `SUM`, or `AVG`.
* `ORDER BY` — Sorts query results in ascending (`ASC`) or descending (`DESC`) order based on one or more columns.
* `LIMIT` — Restricts the number of records returned by a query, useful for pagination or testing.
* `DISTINCT` — Ensures that query results contain only unique values, eliminating duplicates from the output.

# Day 15 - August 18, 2026
## What is Networking?
## What is Networking?
* `Networking`: Networks are simply things connected (e.g., a friendship circle connected by similar interests, hobbies, or skills).
* `Internet`: One giant network consisting of many small networks within itself.
* `World Wide Web`: Invented by Tim Berners-Lee in 1989.
* `Private Network`: Like the inside of your own home—a safe, local network for your internal devices.
* `Public Network`: The massive highway outside your front door—the global Internet accessible to everyone.
# Identifying Devices on a Network
* `IP Address`: Assigned to a device when it joins a network; can change depending on where you connect (e.g., home Wi-Fi vs. coffee shop Wi-Fi).
* `MAC Address`: A unique physical identifier tied directly to the device’s network card (NIC) that stays the same behind the scenes.
* `MAC Spoofing`: Software technique that lets you temporarily change or "fake" your device's permanent MAC address fingerprint.
### Public IP
* `IPv4`: Uses 4 groups of numbers separated by dots (e.g., `86.157.52.21`).
* `IPv6`: Uses 8 groups of numbers and letters separated by colons (e.g., `2a00:22c4:a531:c500:425f:cce6:c36b:f64d`).
# PING
* `PING / ICMP`: Uses ICMP (Internet Control Message Protocol) packets to determine the performance of a connection between devices (e.g., checking if a connection exists or is reliable).

# Network Fundamentals Study Log
# Day 16 — August 20, 2026

## LAN Topologies
* `Star Topology`: All devices plug into a central hub or switch; easy to manage, but fails completely if the central device breaks.
* `Bus Topology`: Devices connect along a single main backbone wire; inexpensive to set up, but heavy traffic slows it down and a cable break drops the network.
* `Ring Topology`: Devices connect in a continuous circle; prevents data collisions, but a single broken connection disables the entire loop.

## Core Networking Hardware
* `Router`: Connects separate networks together and routes data packets along the best path to their destination.
* `Switch`: Connects local devices via dedicated physical ports and directs traffic specifically to target MAC addresses without flooding the network.

## Subnetting & Addressing
* `Subnetting`: Splits a large network into smaller, isolated mini-networks (subnets) for increased performance, organization, and security.
* `Network Address`: The starting IP of a subnet (`192.168.1.0`) that acts as the "street name" for the entire neighborhood.
* `Host Address`: The unique IP (`192.168.1.100`) assigned to a specific endpoint device inside the subnet.
* `Default Gateway`: The exit IP (`192.168.1.254`) assigned to the router, enabling local devices to communicate with external networks.

## Address Resolution Protocol (ARP)
* `ARP`: Protocol used to dynamically map a known layer 3 IP address to an unknown physical layer 2 MAC address.
* `ARP Cache`: A temporary local ledger stored on a host that records discovered IP-to-MAC address pairings.
* `ARP Process`: A host broadcasts an ARP Request ("Who owns this IP?") to the network, and the owner responds directly with an ARP Reply containing its MAC address.

## Dynamic Host Configuration Protocol (DHCP)
* `DHCP`: An automated protocol that leases temporary IP addresses and network settings to joining devices using a four-step process (DORA).
* `DHCP Discover (D)`: The client broadcasts a request searching for available DHCP servers on the local network.
* `DHCP Offer (O)`: A DHCP server responds with an offered IP address available for lease.
* `DHCP Request (R)`: The client sends a response accepting the specific offered IP address.
* `DHCP ACK (A)`: The server acknowledges the agreement, confirming the IP address lease duration (e.g., 24 hours) for the client.

# Day 17 - August 22, 2026
# OSI models

### 📦 1. Packets & Frames
* **Packet (Layer 3):** Outer envelope. Uses **IP Address** to travel the internet.
* **Frame (Layer 2):** Inner envelope. Uses **MAC Address** to deliver data on local Wi-Fi/LAN.
* **4 Main Labels:** 
  * `TTL` (Self-destruct timer)
  * `Checksum` (Damage check)
  * `Source IP` (Return address)
  * `Destination IP` (Target address)
  ### 🔄 2. TCP vs. UDP
* **TCP (Careful):** Reliable and slow. Uses a **3-Way Handshake** (`SYN` ➡️ `SYN/ACK` ➡️ `ACK`) to guarantee data arrives safely.
* **UDP (Fast):** Unreliable and lightweight. Drops data continuously without checking (great for streaming & gaming).
### 🚪 3. Layer 4: Common Ports Cheatsheet
* **Port 21 (FTP):** File transfer
* **Port 22 (SSH):** Encrypted remote terminal
* **Port 53 (DNS):** Website name to IP translator
* **Port 80 (HTTP):** Plain web traffic
* **Port 443 (HTTPS):** Encrypted web traffic
* **Port 445 (SMB):** Local network file/printer sharing
* **Port 3389 (RDP):** Remote Desktop
* **Port 25565:** Minecraft server hosting
* **Ports 49,152–65,535:** Random temporary client return ports
### 🛡️ 4. Security & Exploitation Context
* **Netcat (`nc`):** A command-line utility used to manually read/write to network ports.
* **Lures vs. Exploits:**
  * **Lures (Phishing/Malware):** Tricking users into opening a **Reverse Shell** connection back to the attacker.
  * **Direct Exploits:** Attacking software/OS bugs directly on listening open ports.

  # Day 18 - August 23, 2026

  # Network & Security Fundamentals Notes
---
## 1. Network Traffic & Security Layers
* **HTTP (Unencrypted):** Like a glass house. Anyone on the path can read your data, passwords, and messages in plain text.
* **HTTPS (Encrypted Content):** Like a locked house. Your data is scrambled, but snoopers can still see your IP address and which destination website you are visiting.
* **VPN (Encrypted Tunnel):** Like an armored car. Hides your real IP address and conceals where your traffic is traveling to from your ISP or local snoopers.
* **HTTPS + VPN (Double-Layer Protection):** Maximum security. HTTPS encrypts the payload so even the VPN provider can't read it, while the VPN hides your destination and origin IP address.
---
## 2. Port Forwarding & IP Addresses
* **Port Forwarding (The Receptionist's Rule):** A router rule that directs incoming traffic from the outside internet directly to a specific private device on your local network.
* **Public IP Address:** Your home or network’s unique identity on the global internet (visible to the outside world).
* **Private IP Address:** The internal address assigned to a device inside your local home or office network.
---
## 3. Defense Mechanisms: Firewalls vs. Antivirus
* **Firewall (The Gatekeeper):** Inspects incoming and outgoing network traffic, deciding which connections or ports are allowed to open.
* **Antivirus (The Internal Inspector):** Scans files already saved or executing on your device to detect and destroy malicious code.
### Firewall Types
* **Stateful Firewall (Smart Guard with a Memory):** 
  * Tracks active connections and context.
  * Automatically allows returning traffic if an internal device requested it first.
  * Requires more memory and processing power.
* **Stateless Firewall (Rule-Based Guard):** 
  * Has no memory of past traffic; evaluates every packet individually against strict filtering rules.
  * extremely fast, low memory overhead, ideal for stopping traffic floods.
---
## 4. VPN Technologies & Protocols
* **PPP (Point-to-Point Protocol):** Handles authentication and basic data encryption (The Safe Box & Secret Key). *Non-routable on its own.*
* **PPTP (Point-to-Point Tunneling Protocol):** Wraps PPP data to transport it across external networks (The Fast Delivery Van). Fast and easy to configure, but uses weak, outdated encryption.
* **IPSec (Internet Protocol Security):** Modern standard encrypting traffic at the IP layer (The Heavy Armored Tank). Offers robust security, though it requires more setup configuration.
---
## 5. Core LAN Devices & Virtual Isolation
* **Router (Border Control):** Connects separate networks together (e.g., your home LAN to the public internet) and determines the best path for data.
* **Switch (The Hallway):** Connects multiple local devices within the same network floor or room, directing traffic straight to its local target device.
* **VLAN (Virtual Local Area Network):** 
  * Logically divides a single physical switch into separate, isolated virtual networks (Separate Locked Rooms).
  * Prevents direct communication between isolated groups (e.g., Guests vs. Staff) without passing through a router first.

  # Day 19 - August 25, 2026
  # DNS in detail

  # DNS Fundamentals & Lookup Process
---
## 1. DNS Basics & Domain Structure
**DNS (Domain Name System)** translates human-friendly domain names (like `google.com`) into computer-friendly IP addresses. It functions as the internet's giant address book.
      admin  .  tryhackme  .  com
         |         |             |
     Subdomain    SLD           TLD

* **TLD (Top-Level Domain):** The suffix at the very end of a domain.
  * **gTLD (Generic TLD):** Denotes purpose (e.g., `.com` for commercial, `.org` for organization, `.edu` for education, `.gov` for government).
  * **ccTLD (Country Code TLD):** Denotes geographical location (e.g., `.ca` for Canada, `.co.uk` for United Kingdom).
* **SLD (Second-Level Domain):** The unique name registered directly to the left of the TLD (e.g., `tryhackme` in `tryhackme.com`).
  * *Rules:* Max 63 characters + TLD. Allows `a-z`, `0-9`, and hyphens (cannot start/end with hyphens or use consecutive hyphens).
* **Subdomain:** Sits to the left of the SLD, separated by a dot (e.g., `admin` in `admin.tryhackme.com`).
  * *Rules:* Full domain length must be 253 characters or less. You can create an unlimited number of subdomains.
---
## 2. Common DNS Record Types

| Record | Function | Kid-Friendly Analogy |
| :--- | :--- | :--- |
| **A** | Maps domain to an **IPv4** address. | **The Home Address:** "TryHackMe lives at House #104.26.10.229." |
| **AAAA** | Maps domain to an **IPv6** address. | **The Futuristic Address:** Same as A Record, but uses longer, newer numbers because we ran out of regular numbers. |
| **CNAME** | Maps a domain/subdomain to another domain name. | **The Nickname:** "Store is a nickname for Shopify's house—go look up Shopify's address instead!" |
| **MX** | Points to the mail servers for handling domain emails (includes priority flags). | **The Mailbox:** "Send letters to Mailbox #1. If it's full, try backup Mailbox #2." |
| **TXT** | Holds plain text data (used for security, verification, and email authentication). | **The Sticky Note:** A note on the door verifying ownership or telling carriers who is allowed to drop off packages. |

---

## 3. The Step-by-Step DNS Request Journey
When you request a domain that is not saved in your browser, your query goes on a full relay race across the internet:
1. **Local Cache Check (Your Memory):** Your computer checks its own local cache. If it looked up the site recently, it uses the saved address instantly.
2. **Recursive DNS Server (Neighborhood Guide):** Usually provided by your ISP. It checks its own cache. If found, the trip ends. If not, it begins the query race on your behalf.
3. **Root Server (Grandfather of the Internet):** Directs the guide to the correct TLD manager based on the extension (e.g., points `.com` requests to `.com` servers).
4. **TLD Server (Neighborhood Manager):** Holds records for the specific TLD and directs the request to the official nameserver for that domain.
5. **Authoritative Server (Official Record Keeper):** Holds the master rulebook for the domain. It looks up the requested record and hands over the real IP address.
6. **TTL & Response (Sticky Note Timer):** The Recursive Server receives the address, caches it locally with a **TTL (Time To Live)** expiration timer (e.g., 300 seconds), and hands the address back to your computer.

# Day 20 - August 30, 2026
# HTTPS in detail

# HTTP Basics Quick Reference
---
## 1. URL Anatomy
`https://user:pass@example.com:443/blog?id=1#section2`
* **Scheme (`https`):** Protocol used.
* **User (`user:pass`):** Optional login details.
* **Host (`example.com`):** Server domain/IP.
* **Port (`443`):** Connection port (`80`=HTTP, `443`=HTTPS).
* **Path (`/blog`):** Location of the file/page.
* **Query (`?id=1`):** Extra data passed to the path.
* **Fragment (`#section2`):** Direct link to a spot on the page.

---
## 2. HTTP Methods & Status Codes
| Method | Action |
| :--- | :--- |
| **GET** | Fetch data |
| **POST** | Create new record |
| **PUT** | Update record |
| **DELETE** | Remove record |
| Code Range | Meaning | Key Codes |
| :--- | :--- | :--- |
| **100–199** | Informational | Rare/Continue |
| **200–299** | Success | **200** (OK), **201** (Created) |
| **300–399** | Redirection | **301** (Moved Permanently), **302** (Found) |
| **400–499** | Client Error | **400** (Bad Request), **401** (Unauthorized), **403** (Forbidden), **404** (Not Found), **405** (Method Not Allowed) |
| **500–599** | Server Error | **500** (Internal Error), **503** (Service Unavailable) |
---
## 3. Core Headers
### Request (Client $\rightarrow$ Server)
* **Host:** Specifies target site on a shared server.
* **User-Agent:** Identifies browser/device type.
* **Content-Length:** Size of submitted request data.
* **Accept-Encoding:** Supported compression (e.g., `gzip`).
* **Cookie:** Sends saved session/login keys.
### Response (Server $\rightarrow$ Client)
* **Set-Cookie:** Hands client a session/login key to save.
* **Cache-Control:** How long to store page locally.
* **Content-Type:** Data type returned (HTML, PNG, JSON).
* **Content-Encoding:** How data was compressed for transfer.

# Day 20 - September 6, 2026
# Putting it all Together

# Web Architecture Quick Reference

**Core Components**
* **Load Balancer (Traffic Cop):** Distributes web traffic across servers to prevent crashes[cite: 1].
* **CDN (Local Warehouse):** Serves cached static files (images, CSS, JS) from nearby servers for faster loading[cite: 1].
* **Database (Filing Cabinet):** Stores and retrieves application data securely[cite: 1].
* **WAF (Security Guard):** Inspects incoming HTTP requests to block malicious attacks (SQLi, XSS) and bots[cite: 1].
* **Web Server (Waiter):** Receives requests and serves website files (e.g., Nginx, Apache)[cite: 1].
* **Virtual Host (Apartment Building):** Allows one server to host multiple domain names[cite: 1].
* **Static Content:** Unchanging files (CSS, images) delivered directly to the browser[cite: 1].
* **Dynamic Content:** Personalised data generated in real-time by the backend[cite: 1].
* **Backend Languages (Chef):** Server-side code (PHP, Python, Node.js) processing logic and database queries[cite: 1].

---

**Request Flow Lifecycle**
1. **DNS Lookup:** Browser checks local cache, then queries DNS servers to find the website's IP address[cite: 1].
2. **WAF Inspection:** Request is filtered for malicious payloads and rate limits[cite: 1].
3. **Load Balancer:** Directs the request to the healthiest available web server[cite: 1].
4. **Web Server & Backend:** Server handles the HTTP request, executes code, and queries the database[cite: 1].
5. **Browser Render:** Client receives HTML, CSS, and JS to display the web page[cite: 1].

# Day 21 - September 10, 2026
# The CIA Triad & The Security Mindset

---
## 1. Core Principles of Security (The CIA Triad)

### **Confidentiality**
* **Core Goal:** Restrict data access strictly to authorized users.
* **Impact of Failure:** Unauthorized exposure leads to data leaks, financial loss, privacy violations, and severe legal penalties.
* **Key Defense:** Access controls, encryption, and proper permissions.

### **Integrity**
* **Core Goal:** Prevent unauthorized modification, deletion, or tampering of data.
* **Impact of Failure:** Corrupted or altered data ruins trust and can cause dangerous operational consequences.
* **Key Defense:** Parameterized queries, input validation, hashing, and database constraints.

### **Availability**
* **Core Goal:** Ensure systems, services, and data are consistently accessible to legitimate users when needed.
* **Impact of Failure:** Unplanned downtime halts business operations, resulting in major financial and reputational loss.
* **Key Defense:** Automated scripts, WAF rate limiting, load balancing, auto-scaling, and failover redundancy.

---

## 2. The Security Mindset (The 3 Questions)

When auditing, building, or testing any feature or web application, evaluate every request against these core questions[cite: 1]:
## Security Mindset
- Was sensitive data exposed to unauthorized individuals?
- Was data being modified without permission?
- Were systems or services unavailable to users when they needed? 


# Day 22 - September 11, 2026
# Cryptography Concepts

---
## 1. Fundamentals
* **Cryptography:** The science of encoding and decoding messages to protect data from unauthorized access[cite: 1].
* **Plaintext:** Human-readable data in its original form (e.g., `HELLO` or `Patient name: Alice Smith`)[cite: 1].
* **Ciphertext:** Scrambled, unreadable data generated by encryption (e.g., `KHOOR`)[cite: 1].
* **Key:** The secret value/password used by an algorithm to lock or unlock data[cite: 1].
* **Algorithm:** The public mathematical steps/recipe for encrypting and decrypting data; security relies on keeping the key secret, not the algorithm[cite: 1].

### Core Processes
* **Encryption:** $\text{Plaintext} + \text{Algorithm} + \text{Key} \longrightarrow \text{Ciphertext}$[cite: 1]
* **Decryption:** $\text{Ciphertext} + \text{Algorithm} + \text{Key} \longrightarrow \text{Plaintext}$[cite: 1]

---
## 2. Encryption Types
### **Symmetric Encryption**
* **Mechanism:** Uses a single shared secret key for both encryption and decryption[cite: 1].
* **Analogy:** A house door where every family member carries a duplicate copy of the same physical key[cite: 1].
* **Characteristics:** Fast and computationally efficient, ideal for large datasets[cite: 1].
* **Examples:** Caesar Cipher (historical substitution)[cite: 1], AES (Advanced Encryption Standard)[cite: 1].
* **Weakness:** Key Distribution Problem—transmitting the shared key securely without interception is difficult[cite: 1].

### **Asymmetric Encryption**
* **Mechanism:** Uses a key pair—a **Public Key** (shared openly to encrypt) and a **Private Key** (kept secret to decrypt)[cite: 1].
* **Analogy:** A front porch mailbox. Anyone can drop a letter through the slot (Public Key), but only the owner has the door key (Private Key) to open it[cite: 1].
* **Characteristics:** Solves the key distribution problem, but computationally slower than symmetric encryption[cite: 1].
---
## 3. The Hybrid Approach (TLS/SSL Handshake)
Modern web security combines both types to maximize speed and secure key distribution[cite: 1]:
1. **Key Request:** Browser requests the server's public key[cite: 1].
2. **Public Key Transfer:** Server sends its public key inside a digital certificate[cite: 1].
3. **Asymmetric Key Exchange:** Browser and server use asymmetric encryption to negotiate a brand-new shared symmetric key[cite: 1].
4. **Symmetric Data Transfer:** System switches to symmetric encryption using the shared key for fast session communication[cite: 1].

> **Certificate Authority (CA):** A trusted third party that issues and validates digital certificates to verify website ownership[cite: 1].

# Day 23 - September 15, 2026
# Become a Hacker: The Mindset & Methodology

# Security Journal: Offensive Security & Defensive Controls
---
## 1. Offensive Security Fundamentals
* **Offensive Security:** Proactively testing systems by attempting to break into them to identify weaknesses before malicious actors can exploit them.
### Core Terms
* **Red Teaming (Real-world testing):** A structured, authorized attack methodology simulating a real adversary to test defenses and identify vulnerabilities within a defined scope.
* **Penetration Test (The Inspection):** A structured security assessment where authorized testers identify and exploit vulnerabilities within a defined scope to measure real-world risk.
* **Vulnerability (The Flaw):** A weakness or bug in a system, application, or configuration that could be abused.
* **Exploit (The Trick):** A technique, method, or script used to take advantage of a vulnerability to achieve a specific outcome (e.g., unauthorized access).
* **Scope (The Rules):** The exact legal boundaries of an engagement defining which systems, applications, and actions are permitted and what is off-limits.
* **Enumeration:** Collecting details about a target system, users, and services to locate weak points.
* **Credentials:** Login details (usernames and passwords) that grant system access.
* **Authentication:** The process of verifying whether an entity is who they claim to be during login.
* **Dictionary Attack:** Automated testing of a predefined wordlist to guess valid usernames, passwords, or directory paths.
---
## 2. Reconnaissance & Testing Tools
* **Gobuster:** A command-line tool that uses dictionary wordlists to discover hidden files, directories, and unlinked endpoints on a web server.
* **Hydra:** A fast command-line tool designed to perform dictionary attacks to guess credentials across web forms and network protocols.
---
## 3. Thinking Like a Hacker
### Core Philosophy
Ethical hacking requires looking beyond intended UI functionality to discover how a system can be misused, manipulated, or bypassed—always within authorized scope.
### Practical Principles
* **Ask "What If?":** Never assume logic is secure just because it works on the UI.
* **Input Unpredictability:** Supply unexpected data types, sizes, and formats to catch missing server-side validation. 
* **Vulnerability Chaining:** Link multiple minor flaws together to demonstrate maximum risk and business impact.
* **Adversarial Perspective:** Approach every target with a specific threat model: *What is the most valuable asset here, and how can it be compromised?*
---
## 4. Authenticated Attack Surface: A Valuable Target

### Core Threat
Valid credentials allow an attacker to bypass perimeter security and act with the legitimate permissions of a compromised account.
### Accessible High-Value Targets
* **Sensitive Functionality:** Core operations (executing transactions, modifying records, triggering backend processes) reserved for logged-in users.
* **User Data & PII:** Private personal data (emails, addresses, account histories) subject to theft, abuse, or resale.
* **Administrative Controls:** High-privilege settings and user management panels granting full control over application state.
* **Expanded Exploit Surface:** Additional endpoints, API parameters, and backend workflows exposed only after authentication, enabling privilege escalation and lateral movement.
---
## 5. Essential Defensive Controls
| Security Control | Primary Function | Attacks / Threats Mitigated |
| :--- | :--- | :--- |
| **Rate Limiting** | Throttles excessive request volume per IP/User | Brute-force attacks (Hydra), web scraping, DoS |
| **Parameterized Queries** | Separates database code from user data | SQL Injection (SQLi) |
| **Input Sanitization** | Cleans/escapes untrusted user input | Cross-Site Scripting (XSS), HTML injection |
| **Access Control (RBAC)** | Enforces server-side permissions per user | IDOR, horizontal/vertical privilege escalation |
| **Secure Cookie Flags** | Secures session tokens (`HttpOnly`, `SameSite`) | Session hijacking, XSS token theft, CSRF |
| **CAPTCHA / WAF** | Identifies bots & filters malicious traffic payloads | Automated credential stuffing, Gobuster scans |

# Day 23 - September 17, 2026
# Become a Defender: The Mindset & Methodology

# Security Journal: Defensive Security (Blue Team)
---
## 1. Defensive Core Principles
* **Defensive Security:** The discipline of protecting systems by implementing security controls, maintaining continuous visibility, and responding to incidents to mitigate risk.
### The 4 Defensive Questions
* **1. Assets (What am I protecting?):** Identifying all critical infrastructure, databases, endpoints, and services.
  * **City Analogy:** Police and security protecting homes, businesses, and citizens.
  * **Tech Equivalent:** Physical/cloud servers, production databases, user accounts, and laptops.
  * **Core Concept:** You cannot protect an asset you don't know exists. Asset discovery is step zero.

* **2. Visibility (Can you see what you are protecting?):** Maintaining continuous logs and telemetry across all systems.
  * **City Analogy:** CCTV cameras, security patrols, and community reporting.
  * **Tech Equivalent:** System event logs, network flow data, and SIEM security alerts.
  * **Core Concept:** Attackers thrive in blind spots. High visibility exposes malicious activity early.

* **3. Detection (What classifies suspicious behavior?):** Defining normal baselines to flag anomalies.
  * **City Analogy:** Spotting someone testing door handles or a car slowly circling a street at 3 AM.
  * **Tech Equivalent:** Flagging 50 failed logins in 5 seconds or concurrent logins from two different countries.
  * **Core Concept:** Effective detection relies on separating standard operational traffic from anomalous patterns.

* **4. Response (How do you respond to threats?):** Executing containment, eradication, and recovery procedures.
  * **City Analogy:** Blockading roads, dispatching officers, or issuing emergency curfews.
  * **Tech Equivalent:** Applying firewall blocking rules, revoking session tokens, or isolating infected endpoints.
  * **Core Concept:** Detection without automated or rapid manual response is ineffective.

---

## 2. Functions of a Defender
* **Prevention:** Proactively blocking attacks before execution (e.g., firewalls, access controls, patching).
* **Detection:** Monitoring networks and endpoints to flag suspicious events using log telemetry.
* **Mitigation:** Acting during an active event to limit blast radius (e.g., isolating hosts, blocking malicious IPs).
* **Analysis:** Performing forensic reviews of logs and evidence to determine root causes and attack vectors.
* **Response & Improvement:** Restoring compromised assets and hardening controls to prevent re-exploitation.

---

## 3. Defensive Mindset
* **Threat Anticipation:** Continually asking *"What if?"* and mapping hypothetical attack paths against assets.
* **Attack Awareness:** Studying standardized attack frameworks (e.g., MITRE ATT&CK) to understand adversary tactics.
* **Risk Prioritization:** Allocating defensive resources to high-impact, critical assets first.
* **Continuous Adaptation:** Updating rules, signatures, and architecture as attack techniques evolve.
---
## 4. Key Terminology
* **Blue Team:** The defensive security personnel tasked with securing infrastructure and responding to threats.
* **Client Infrastructure:** The combined network, servers, devices, and applications managed by an organization.
* **Threat:** Any potential circumstance or event with the capacity to adversely impact an asset.
* **Risk:** The combined metric of threat likelihood and business impact.
---
## 5. Infrastructure Mapping & Risk Matrix
### City Analogy Overview
| Component | Technical Purpose | City Analogy |
| :--- | :--- | :--- |
| **Employee Devices** | Workstations used to access enterprise resources | Homes |
| **Web Server** | Hosts public applications, portals, and web services | Shops / Public Buildings |
| **Mail Server** | Manages inbound and outbound organization email | Post Office |
| **Firewall** | Filters and controls incoming and outgoing network traffic | City Gate |
| **Outside Internet** | Untrusted public networks outside the perimeter | Beyond City Limits |
---
### Threat & Defense Matrix

| Component | Risk / Threat Scenario | Defensive Controls |
| :--- | :--- | :--- |
| **Employee Devices** | Phishing execution, unauthorized downloads, malware infection | Antivirus/EDR, OS patch management, least-privilege policies |
| **Web Server** | Web app exploits (SQLi, XSS), unauthorized data extraction | Web Application Firewall (WAF), HTTPS, rate limiting, input validation |
| **Mail Server** | Business Email Compromise (BEC), phishing, malicious attachments | Email spam filtering, attachment sandboxing, SPF/DKIM/DMARC |
| **Firewall** | Unsolicited connection requests, port scanning, unauthorized ingress | Strict Access Control Lists (ACLs), IP reputation feeds, port disabling |
| **Outside Internet** | Distributed Denial-of-Service (DDoS), botnet probes, credential stuffing | Inbound traffic restrictions, network flow monitoring, edge rate-limiting |

# Day 24 - September 23, 2026

# Search Skills

## 1. Offensive Reconnaissance & Threat Intelligence Tools

- **Shodan:** A search engine for internet-connected devices, allowing users to find exposed services, open ports, and vulnerable systems.
- **VirusTotal:** A search engine for malware samples, allowing users to analyze file hashes, scan results, and community comments.
---
## 2. Key Differences: Google vs. Shodan

| Feature | Google / Bing | Shodan |
| :--- | :--- | :--- |
| **Primary Target** | Web pages, text, images, HTML content | Connected devices, IP addresses, open ports |
| **Discovery Method** | Web crawlers following hyperlinks | Port scanning public IP address ranges |
| **Primary Data Collected** | Page content and metadata | Service banners (e.g., HTTP headers, SSH versions) |

* **When to Use Shodan:**
  * **Passive Reconnaissance:** Gathering open port and service telemetry without direct target interaction.
  * **External Asset Auditing:** Verifying that organization IP ranges do not expose unwanted management ports (e.g., SSH 22, RDP 3389, DB 3306).
  * **Infrastructure Threat Hunting:** Locating widespread vulnerable server software versions across public subnets.

* **When NOT to Use Shodan:**
  * **Web Application Pen-Testing:** Identifying application-layer logic flaws, XSS, or SQLi (requires OWASP ZAP or Burp Suite).
  * **Real-Time Active Port Validation:** Verifying live port status immediately after firewall changes (requires Nmap).
---
## 3. Shodan Search Syntax & Operators


# Basic Syntax Pattern
filter:value
filter:"spaced value"

# Practical Search Examples
ip:"1.1.1.1"               # Inspect a specific target IP
net:"192.168.1.0/24"       # Scan an entire CIDR subnet range
port:"3389"                # Locate open Remote Desktop Protocol (RDP) ports
org:"Target Company"       # Search devices belonging to a specific organization
hostname:"*.edu"           # Filter hostnames belonging to educational domains
vuln:"CVE-2021-44228"      # Find servers flagged for Log4Shell vulnerability
product:"Apache" version:"2.4.41" # Target specific server software versions
