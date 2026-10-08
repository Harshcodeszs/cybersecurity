## Environment
- wsl Windows Subsystem for Linux.
- nmap — network scanner (discovers hosts, open ports)
- curl — transfers data from/to URLs (testing web servers)
- wget — downloads files from the internet
- git — version control (for cloning repos and scripts)
- netcat — network Swiss Army knife (read/write network connections)
- python3 + pip — Python and its package manager

## Terms
- UEFI - Unified Extensible Firmware Interface
- BIOS - Basic Input/Output System
- POST - Power On Self Test
- BOOTLOADER - loads the Operating System (Windows/Linux) from storage into RAM.
- DNS - Domain Name System
- IP - Internet Protocol
- HTTP - Hypertext Transfer Protocol
- SSH - Secure shell
- HTTPS - Hypertext Transfer Protocol Secure:
- SSL - Secure Sockets Layer
- TLS - Transport Layer Security

# Computer Systems
- Central Processing Unit (CPU) - the brain of the computer
- Random Access Memory (RAM) - short term memory
- Storage Drive (HDD/SSD) - long term memory
- Motherboard - connects all the components
- Power Supply Unit (PSU) - provides power
- Graphics Card (GPU)- Visual processing 

## Basic Input/Output System
- Step-by-Step Breakdown
1. **Press Power Button (Sending Electricity)**
- What happens: Pressing the power button sends an electrical signal to the Power Supply Unit (PSU), which starts sending power/electricity through the motherboard to wake up the hardware.
- Human analogy: Pressing snooze on an alarm—your eyes open, oxygen flows, and blood starts pumping.
2. **Firmware Starts (The Basic Instructions)**
- What happens: The CPU wakes up, but it doesn't know what to do yet. It reads instructions from a tiny chip on the motherboard called UEFI (Unified Extensible Firmware Interface).
## Note: Older computers used BIOS for this, but modern systems use UEFI.
- Human analogy: You are awake, but your brain hasn't fully booted up or realized where you are yet.
3. **Power-On Self Test / POST (The Health Check)**
- What happens: The UEFI chip runs a quick hardware diagnostic called POST. It checks: "Is RAM present? Is the CPU okay? Is the keyboard plugged in?" If something is broken (like missing RAM), it won't boot and will make a beep sound or show an error.
- Human analogy: Stretch your arms and legs to make sure nothing hurts bef  ore getting out of bed.
4. **Select Boot Device (Finding the OS)**
- What happens: Once all hardware checks pass, UEFI checks its priority list (the Boot Order) to find where the Operating System is installed (e.g., SSD, Hard Drive, or USB drive).
- Human analogy: Looking at your schedule or alarm to figure out where you need to go for the day.
5. **Initiate Bootloader (Handing over Control)**
What happens: UEFI finds the target drive and triggers a tiny program called the Bootloader. The bootloader loads the Operating System (Windows/Linux) from storage into RAM. UEFI then hands full control of the computer over to the Operating System.
- Human analogy: Your mind becomes fully alert and you start your day.
# Computer Types
## Computers You directly Interact With
### These are the systems designed for direct human input using screens, keyboards, or touch interfaces.
- Laptop
- Desktop
- Workstation
- Server
## Hidden & Specialized Computers
### Many of the most critical computers operate quietly in the background without a dedicated monitor or keyboard attached.
- **Server** - provide services, host websites, or manage data for many users over a network.
- **Internet of things (IoT)** - Small, single-purpose devices connected to a network to report data or receive remote commands
- **Embedded Computers** - Dedicated microchips built directly into non-computer machines
---
- **Smartphone** - Pocket-size computer optimize for battery life and connectivity
- **Tablet** - Touch-first computer with larger screen 
- **Iot device** - Network connected device with a single purpose (read/control)
- **Embedded Computer** - Computer with built in device
## The Core Engineering Trade-offs
### Choosing the right computer comes down to two major compromises:
- **Mobility vs. Performance**: Shrinking a device down to fit in a pocket or backpack limits battery size and heat dissipation, which costs overall computing power.
- **Reliability vs. Cost**: Systems that cannot afford to crash—like servers and workstations—use redundant hardware (such as dual power supplies and backup drives) to prevent system failure, which increases costs.
# Client Server 
1. **Client and Server** (Who initiate and Who responds) 
-  Client: The device or software (like your web browser) that initiates the request.
- Server: The remote computer waiting 24/7 to receive requests and send back data (like serving a website).
2. **Request and Response**
- Request: The client asks the server for a specific file or webpage (e.g., HTTP GET /index.html).
- Response: The server processes the request and sends back the content along with a status message (e.g., 200 OK or 404 Not Found if the page doesn't exist).
3. **Protocol**(The shared rules and language)
- A Protocol defines the precise rules, syntax, and formatting that computers use to talk to each other. For example:
- HTTP / HTTPS: Protocols used for transferring web pages.
- FTP: Protocol used for sending files.
4. **Port** (The specific door or service access point)
- A single server can run multiple services at once. Ports act as specific doors/channels to reach those distinct services:
- Port 80: HTTP (Unencrypted web traffic).
- Port 443: HTTPS (Secure, encrypted web traffic).
- Port 22: SSH (Secure command-line access).
5. **DNS & IP Address** (Finding the exact location)
- Domain Name: Human-readable web address (e.g., google.com or tryhackme.com).
- IP Address: Numerical location identifier used by devices to route traffic over the internet (e.g., 192.168.1.10).
- DNS (Domain Name System): The phonebook/GPS of the internet that automatically translates human domain names into numerical IP addresses.
## HTTP commands
1. **GET** (READ)
- Requests data or a web page from a server. It only retrieves information and does not alter anything on the server (e.g., loading a home page).
2. **POST** (CREATE) 
- Sends data to the server to create a new resource (e.g., submitting a registration form, logging in, or posting a comment).
3. **PUT** (UPDATE/REPLACE)
- Uploads data to completely replace an existing resource or create it if it doesn't exist yet.
4. **DELETE**
- Removes a specified resource or file from the server.
5. **PATCH** (PARTIAL UPDATE)
- Applies partial modifications to a resource (unlike PUT, which replaces the entire item, PATCH only updates specific fields like changing just your password).
6. **HEAD** (Metadata check)
- Works exactly like a GET request, but the server returns only the headers and no actual page content. Security tools use this to check file sizes or server types quickly without downloading full files.
7. **OPTIONS** (Permission Check)
- Asks the server which HTTP methods are allowed for a specific URL (e.g., checking if DELETE or PUT are enabled).
8. **CONNECT** (Tunneling)
- Establishes a two-way tunnel connection with the server, commonly used for SSL/TLS encrypted traffic passing through a proxy.
9. **TRACE** (Diagnostic loopback)
- Echoes back the exact request the server received. It is used for debugging network paths, but is often disabled on production servers due to security risks. 
## GET
- **Scheme**: Tells us which protocol was used: HTTP or HTTPS.
- **Host**: Tells us the name of the host we request resources from.
-  **Filename**: Indicates which file we requested from the host. In our request, this is "/", which actually translates to "index.html".
- **Address**: Displays the IP address where the website is hosted. In our example, we are hosting the website on the same device. That's why the
address 127.0.0.1 is shown.
- **Status**: Status: This field indicates whether the request was successful. In our example, we received a "200 OK" status, which means that the request was successful.
# Virtualisation Basics
- **Virtualisation** is a technology that lets you create multiple simulated environments or dedicated resources from a single physical hardware system. Instead of needing five separate physical computers to test different operating systems, you can run five Virtual Machines (VMs) on one computer.
- Before the concept of virtualization, the rule of thumb in IT was:
"One server = one application."
## Understanding the Apartment Building Analogy
1. The Problem (Traditional Physical Server):
- Running one operating system or app on a huge physical server is like one tenant living in a 10-story building.
- It's expensive, wasteful, and underutilizes CPU, RAM, and storage space.
2. The Solution (Virtualization): 
- Splitting that big server into separate virtual apartments lets multiple isolated Virtual Machines (VMs) share the same physical server.
3. How the Analogy Maps to Technology:
- **Physical Server** = The Apartment Building: The raw hardware (CPU, RAM, Hard Drives, Power).
- **Hypervisor** = The Building Manager: The management software layer that safely splits physical resources and acts as a referee between virtual machines.
- **Virtual Machines (VMs)** = The Apartments: Isolated environments with their own privacy, doors, and walls.
- **Apps / Operating Systems** = The Tenants: The software running independently inside each virtual machine without interfering with other VMs.
## Hypervisors core role
- Specialized software that creates, isolates, and manages virtual machines on a physical host.
- Resource Division: Allocates specific shares of host CPU, memory (RAM), and storage to each VM.
- Isolation & Security: Enforces strict boundaries so VMs operate independently without accessing each other's data.
Lifecycle Management: Controls VM states, including starting, stopping, pausing, cloning, and deleting.
## Types of Hypervisors
1. Type 1 (Bare-Metal Hypervisors): Runs directly on physical hardware without a host OS underneath; offers maximum performance and efficiency for servers and enterprise data centers. (eg Production server, Database server, Cloud server)
2. Type 2 (Hosted Hypervisors): Runs as an application inside an existing host operating system; easiest setup for desktop testing, learning, and home labs. (eg software testing, Kali Linux, home labs)
## Virtual Machine (VM)
- A software-emulated computer created by a hypervisor that behaves like a physical system with its own virtualized hardware (CPU, RAM, Storage, Network).
- OS Flexibility: Can run any supported operating system (Windows, Linux, macOS) on top of the host system.
- Fault Tolerance & Isolation: Complete separation from other VMs; if one VM crashes, gets corrupted, or gets infected, the host and other VMs remain unaffected.
- Type 2 Software Examples: Tools like Oracle VirtualBox and VMware Workstation allow running multiple operating systems on a personal computer.
### Common Cybersecurity Use Cases:
- Malware Analysis: Safely executing and testing suspicious files in an isolated sandbox environment to protect the host OS.
- Multi-OS Labs: Running security-focused operating systems (like Kali Linux) on an existing host machine without buying additional physical hardware.
## Container 
- A lightweight, isolated environment that packages a single application along with all its required dependencies, libraries, and configurations.
- Kernel Sharing: Instead of running a full virtual operating system, containers share the host OS kernel (the core system layer managing hardware and memory).
### Key characteristics:
- Instant Startup & Low Overhead: Highly efficient because they don't need to boot an entire guest OS.
- Host OS Dependency: Must match the host operating system type (e.g., native Windows containers cannot run on a Linux kernel).
- Consistency & Portability: Ensures applications run identically across development, testing, and production environments.
- Application-Level Isolation: Prevents a misbehaving or buggy container from crashing other containers running on the same host.
# Cloud Computing Basics
- Cloud Computing: Delivery of computing resources (servers, storage, databases, networking, software) over the internet on-demand, eliminating the need for local infrastructure.

1. **Benefits** -
Before the cloud, companies had to buy physical servers, put them in a dedicated server room, pay high electricity bills, and hire team members to maintain the hardware. If a website suddenly got popular, it would crash because adding new physical hardware took weeks.
- **Scalability**: You can increase or decrease your computing power in seconds as web traffic changes.
- **On-demand Self-service**: You can launch a new virtual server with a few clicks instead of ordering physical equipment.
- **Pay-As-You-Go**: You don't pay massive upfront costs; you only pay for the exact minutes or hours you use a server.
- **High Availability & Global Access**: Provider servers are located all over the world. If one physical server breaks, your app automatically shifts to another without going offline.
2. **Cloud Deployment Models** -
Depending on a company's budget, privacy requirements, and industry regulations, they choose where their cloud runs:
- **Public Cloud** (e.g., AWS, Microsoft Azure, Google Cloud): You share hardware infrastructure with other companies, but your data stays logically separated and secure. It's affordable and easy to scale.
- **Private Cloud**: The cloud infrastructure is exclusively used by one organization (like a government agency or bank) for strict security, privacy, and compliance.
- **Hybrid Cloud**: A mix of both. A company keeps sensitive customer data on a private cloud while running its public-facing website on a public cloud.
3. **Cloud Service Models** - Cloud services are split into three main tiers depending on how much control you want versus how much work you want the provider to handle:
- **IaaS (Infrastructure as a Service)**: You rent virtual hardware (servers, storage, network setup). You are responsible for installing the OS, updating security patches, and running your software.
- **PaaS (Platform as a Service)**: The provider handles the OS, server maintenance, and environment updates. You just upload your code and run your application.
- **SaaS (Software as a Service)**: Completely managed end-user software running in a browser. You don't manage code, servers, or operating systems—you just log in and use it (e.g., Gmail, Netflix).


# Operating System Introduction
- - OS is the core software that coordinates everything happening on a computer. It sits between the user, applications, and the system’s physical hardware, acting as the invisible manager that keeps the entire machine running as one unified system. (Hardware, Applications, and Operating System)

## System Privilege Layers
- Kernel space: The highly secure core of the OS. It has unrestricted, direct access to all hardware.
- User space: The restricted environment where standard programs run. They cannot touch hardware directly.
- System calls: When an app in user space needs to save a file or send network traffic, it asks the kernel to execute the request on its behalf.

## OS Responsibilities
- Process Management: Creates, schedules, prioritizes, and terminates running programs. The OS decides how much CPU time each process gets, making multitasking feel seamless
- Memory Management: Allocates RAM to processes, protects the app's memory from other processes, and reclaims memory when apps are closed. When RAM runs low, the OS uses virtual memory to keep your system stable
- File System Management: Organizes files into directories, handles naming, paths, permissions, metadata (name, size, type, timestamps)
- User Management: Authenticates logins and enforces file privacy between accounts.
- Device Management: Uses drivers to give apps a unified way to talk to hardware (e.g., printing or playing audio).

### Operating System Security
- Authentication: Verifies who you are through login passwords and biometrics
- Permissions: Controls exactly what each user and app is allowed to read, write, or execute
- Isolation: Keeps every process in its own protected box (kernel/user space separation)
- System Protection: Safeguards critical system files and settings from unauthorized changes

## OS Interface
- Graphics User Interface(GUI):  It provides a graphical representation of all the information you want to access on your computer. Think of folder icons, windows for your applications, and menus for settings. We can imagine the analogy of using a navigation application. You tap an icon of the place you want to visit, and the app generates directions for you, eliminating the need for typing.
- Command Line Interface (CLI): Instead of clicking on icons, you tell the computer exactly what you want using words and syntax that the system understands. This gives you far more precision, control, and speed, especially for advanced tasks, but it requires familiarity with the commands. Back to the maps analogy. Using the CLI is like entering the exact GPS coordinates of your destination. It’s direct and extremely accurate, but only if you know the correct information to type.

### Operating System types
- **Desktop**: Personal computers, daily work, gaming, content creation
- **Windows**: The most widely used operating system on personal computers
Windows 10 (end-of-life), Windows 11
- **macOS**: Apple's desktop OS, known for its polished GUI and integration with other Apple devices
Sonoma (14), Sequoia (15), Tahoe (26)
- **Linux**: Not a single OS but a family of open-source operating systems called distributions
Ubuntu, Debian, Fedora
---
- **Server**: 	Web hosting, databases, cloud services, back-end
- **Windows**: Used in large networks, data centers, and corporate environments
Server 2016, 2019, 2022, 2025
- **Linux**: The vast majority of web servers, trusted for its reliability and open-source nature
Ubuntu Server, Debian, CentOS, Red Hat
- **Unix**: Large enterprises, finance, telecom, government
IBM AIX, Oracle Solaris
---
- **Mobile**: Smartphones, tablets
- **Android**: Google's mobile OS, used in smartphones and tablets
- **iOS**: Apple's mobile OS, used
---
- **Embedded and IoT**: Appliances, cars, IoT devices, smart TVs, routers
- **Embedded Linux**: Specialized OS built into devices with dedicated functions
OpenWrt, Ubuntu Core, Yocto Project
- **Real-time OS**: Designed for apps where tasks need guaranteed response times (aircraft controls)
FreeRTOS, VxWorks, QNX
---
- **Virtual/Cloud**: Lab machines, containers, cloud instances
- **Cloud/VM** - Massive data centers that host websites, apps, and streaming services
Ubuntu LTS, Amazon Linux, Rocky Linux
- **Container-optimized** - Lightweight alternatives to VMs that package just the app and its dependencies
Alpine Linux, Bottlerocket AWS, Flatcar Linux

### Why so many OS
- Different devices and environments require different capabilities from an OS. A laptop must be user-friendly and support multitasking. Servers require stability, security, and must be able to run continuously without interruption. Mobile devices need power efficiency and hardware integration to extend battery life. Embedded systems use lightweight operating systems designed for a specialized purpose.

# Windows Basics

## Logging in and Authentication
- **Guest** - A restricted account intended for temporary access, with minimal permissions and no ability to change system settings
- **Standard** - A user account for everyday tasks, such as running applications and changing personal settings, without access to system-wide changes
- **Administrator** - An account that has full control over the system, including installing software, changing settings, and managing other user accounts
---
- Windows Settings: A modern, centralized location for configuring system, device, personalization, and security settings in Windows
- Control Panel: A legacy management interface that provides access to older system configuration tools still required for specific administrative tasks

## Task Manager
1. **Processes**: Currently running apps and background processes, and their resource usage
2. **Performance**: Graphs and statistics for system resources such as CPU, memory, and network
3. **Users**: Currently logged-in users and used resources 
4. **Details**: A more technical view of running processes, including process IDs (PIDs)
5. **Services**: Windows services and their current status (running or stopped)

## Windows Security 
1. **Virus & threat protection**: Helps detect and remove malicious software using real-time protection and customizable scans
2. **Firewall & network protection**: Controls incoming and outgoing network traffic to help prevent unauthorized access
3. **App & browser control**: Protects users from potentially unsafe apps, files, and websites
4. **Device security**: Provides hardware-based protections that help secure the system

## Windows Defender Firewall: 
is a built-in firewall designed to help protect your computer from unauthorized network traffic. It monitors network connections and applies rules that determine whether the connections are allowed or denied. The firewall operates on different network profiles, allowing you to create custom rules or specify applications that are permitted.
- **Domain**: Used when a system is connected to an organization’s domain network
- **Private**: Intended for trusted networks, such as a home or lab environment 
- **Public**: Used for untrusted networks, such as public Wi-Fi

## Windows Interface & System Tools

- Desktop: The primary workspace holding files, folders, and application shortcuts.
- Taskbar: Navigation bar providing access to open applications, quick settings, and notifications.
- Start Menu: Main menu for accessing installed applications, system settings, and power controls.
- Search: Built-in utility for quickly locating apps, settings, and files via keyword queries.
- File Explorer: File management tool used to navigate, organize, and manage system directories.
- Windows Update: Native utility for installing OS patches, driver updates, and security fixes.
- Microsoft Store: Application marketplace for downloading and installing verified software.
- Windows Settings: Centralized configuration hub for system preferences, devices, and security settings.
- Control Panel: Legacy configuration interface for managing advanced system and administrative settings.
- Task Manager: System monitoring utility for viewing active processes, resource usage, and performance metrics.
- Windows Security: Dashboard for managing built-in protection tools, including antivirus and threat detection.
- Windows Defender Firewall: Network security control designed to filter and block unauthorized network traffic.

# Linux CLI Basics
- **Terminal**: The command-line interface (CLI) where users type commands to interact with
- **Directory**: A folder that organizes files and other directories in a hierarchical structure in linux

# Windows CLI Basics
- **Command Prompt** or **PowerShell**: The command-line interface (CLI) in Windows where users type commands to interact with the operating system.
- **Directory**: A folder that organizes 

# Operating System Security

### CIA
- **Confidentiality**: You want to ensure that secret and private files and information are only available to intended persons.
- **Integrity**: It is crucial that no one can tamper with the files stored on your system or while being transferred on the network.
- **Availability**: You want your laptop or smartphone to be available to use anytime you decide to use it.
---
- 3 weakneses target by malicious users:
1. Authentication: Weak or stolen passwords can allow unauthorized access to systems and data.
2. Weak File Permissions: Improperly configured file permissions can expose sensitive data to unauthorized users.
3. Malicious Programs: Malware, viruses, and ransomware can compromise system integrity and availability.
---
- sudo(ask permission): A command that allows a permitted user to execute a command as the superuser or another user, as specified by the security policy. It is commonly used for administrative tasks that require elevated privileges.
- root(boss): The root user is the superuser account in Unix and Linux systems that has unrestricted access to all commands, files, and resources. It can perform any action on the system, including modifying system files, changing configurations, and managing user accounts.

# Data Representation
- **Bit** It is short for binary digit, and it can be either 0 or 1..
- **Byte**:On modern systems, a byte is 8 bits. It is also referred to as an octet.
- **Hex Color** (Hexadecimal Color Code): A color is represented as a combination of red, green, and blue on computer systems. If one byte is assigned for each of the primary colors (red, green, and blue), we can get more than 16 million color combinations.

- **RGB (Red, Green, Blue)** (FF FF FF): 3 colors that can be combined in different intensities to create a wide spectrum of colors. Each color channel is typically represented by 8 bits, allowing for 256 levels of intensity per channel, resulting in over 16 million possible colors (256 x 256 x 256) 3 binary digits.
- **Binary Representation**: 4 bits (0s and 1s) can represent 16 different values (2^4 = 16). Each bit can be either 0 or 1, and the combination of these bits allows for the representation of numbers, characters, and other data in a digital format and 4 binary digits that represent those values 8, 4, 2, 1.
- **Hexadecimal Digits**(base 16): Hexadecimal representation makes it easy to combine 4 bits into a single character (0-9, A-F). Each hex digit represents 16 values (0-15), and two hex digits can represent a full byte (8 bits) of data. This is commonly used in computing for memory addresses, color codes, and more.
- **Decimal Representation**(base 10): The standard base-10 number system that uses digits 0-9 to represent values. Each digit's position represents a power of 10, allowing for the representation of large numbers in a compact form.
- **Binary**(base 2): Uses only two symbols, 0 and 1, to represent all values. Each position represents a power of 2 (1, 2, 4, 8, etc.), making it the fundamental language of computers.
- **Octal**(base 8): Uses digits 0-7 to represent values. Each position represents a power of 8 (1, 8, 64, etc.). Octal is less commonly used today but was historically significant in computin the octal system uses base 8 and groups 3 bits.
---
**Example**:
- Hex color: A3EA2A
- Hexadecimal: A3 EA 2A
- Binary: 10100011 11101010 01010
- Decimal(RGB): 163 234 42  

# Data Encoding
- **Encoding**: The process of converting data from one format to another for efficient storage,
## ASCII (American Standard Code for Information Interchange)
-  is a 7-bit standard that defines 128 characters covering English letters, digits, and basic punctuation
## Unicode
- is a universal character encoding standard. It assigns unique code points to characters from all modern and historical writing systems worldwide. Unicode supports the interchange, processing, and display of text in diverse languages. In other words, we don’t need to worry about picking a specific encoding standard that is compatible with the language we are using
- *UTF(Unicode Transformation Format)* - UTF as deciding what size shipping boxes to use when sending characters over the internet:
---
- **UTF-8**: Variable-length encoding that uses 1 to 4 bytes per character. It is backward compatible with ASCII and is the most widely used encoding on the web. It is used on almost 90% of all websites on Earth because it doesn't waste space when writing English, but can still display any emoji or language when needed.
- **UTF-16**: Variable-length encoding that uses 2 or 4 bytes per character. It is commonly used in Windows environments and some programming languages. It is more efficient for languages with large character sets, such as Chinese, Japanese, and Korean. Mainly used internally inside operating systems like Windows and languages like Java / JavaScript.
- **UTF-32**: Fixed-length encoding that uses 4 bytes for every character. It is simple and fast but consumes more memory, making it less efficient for storage and transmission. Mainly used internally inside operating systems like Windows and languages like Java / JavaScript. It makes computer processing very easy for certain programs because every single character is guaranteed to be the exact same length in memory. But it wastes way too much storage space for files or internet transmission.

# Python Simple Demo
- Python is a high-level, interpreted programming language known for its simplicity and readability. It is
used extensively in various applications, including web development,

# 1. VARIABLES (Store data)
target_ip = "10.10.10.10"
port = 80

# 2. IF / ELSE CONDITIONALS (Make decisions)
if port == 80:
    print("Web server target detected")
else:
    print("Other service detected")

# 3. WHILE LOOPS (Repeat tasks)
while port <= 83:
    print(f"Scanning port: {port}")
    port += 1  # Always remember to increment to avoid infinite loops!

# JAVASCRIPT Simple Demo
- JavaScript is a high-level, interpreted programming language primarily used for creating interactive and dynamic content

### Example:
let failedLogins = 0;
let maxAllowed = 3;
while (failedLogins < maxAllowed){
    failedLogins += 1;
    console.log(`Warning! Failed attempt ${failedLogins}`);
}
console.log("ALERT: Account locked due to multiple failed logins!"); 

- for loop - The starting and ending points are clearly defined.
- while loop - It needs to run indefinitely (while (true)) until manually stopped or interrupted.
- if else - when you are checking ranges of numbers, comparing values with >, <, >=, or combining multiple conditions with && (AND) or || (OR) option based conditons.
- switch case - Use a switch statement when you have one specific variable and you want to test it against many exact values (like a menu, status codes, or command names) choices.

# Database SQL Basics
- SQL (Structured Query Language) is a standardized programming language used to manage and manipulate relational databases
- tables - A table is a structured collection of data organized into rows and columns. Each row represents a single record, and each column represents a specific attribute or field of that record.
- rows - A row, also known as a record or tuple, is a single entry in a database table that contains data for each column defined in the table's schema.
- columns - A column, also known as a field or attribute, is a vertical entity in a database table that defines a specific type of data stored for each record (row) in the table. 

# SQL commands
- `SELECT` - retrieves data from a database
- `INSERT` - adds new records to a table
- `UPDATE` - modifies existing records in a table
- `DELETE` - removes records from a table
- `ORDER BY` - orders the result set based on a specified column
-  `ASC` - sorts the result set in ascending order (from smallest to largest)
- `DESC` - sorts the result set in descending order
- `WHERE` - filters the result set based on a specified condition

# What is Networking?
- Networks are simply things connected. For example, your friendship circle: you are all connected because of similar interests, hobbies, skills and sorts.
# What is Internet?
- The Internet is one giant network that consists of many, many small networks within itself
- Tim Berners-Lee invented the World Wide Web in 1989
- **Private Network** - A private network is like the inside of your own home
- **Public Network** - A public network (the Internet) is like the massive highway outside your front door
# Identiying Devices on a Network
- **IP Address(Internet Protocol)** - Assigned to a device when it joins a network. It can change depending on where you connect (e.g., home Wi-Fi vs. coffee shop Wi-Fi).
- **MAC Address(Media Access Control)** - A unique physical identifier tied directly to the device’s network card (NIC). Even if a device changes its IP address, its MAC address stays the same behind the scenes.
- **MAC Spoofing** - MAC address is supposed to be like a permanent fingerprint burned into your device. However, software allows you to temporary change or "fake" that fingerprint.
### Public IP
- **IPv4** - Uses 4 groups of numbers separated by dots (e.g., 86.157.52.21).
- **IPv6** - Uses 8 groups of numbers and letters separated by colons (e.g., 2a00:22c4:a531:c500:425f:cce6:c36b:f64d).
# PING
- ICMP - (Internet Control Message Protocol) packets to determine the performance of a connection between devices, for example, if the connection exists or is reliable.


# INTRO to LAN

## LAN topologies
- LAN - LOCAL ARE NETWORK
1. **Star topology** - is like a wheel on a bicycle: all the computer "spokes" connect to one central "hub" in the middle
- The Referee (The Central Switch or Hub): Every single computer is plugged into one main box in the middle.
- Passing Messages: If Computer A wants to send a picture to Computer B, it sends the picture to the referee first. The referee then hands it directly to Computer B.
2. **Bus topology** - is like a single school bus route: if the road gets blocked anywhere along the main path, the whole bus route stops working
- The Main Hallway (The Backbone Cable): All computers plug into one long wire stretched across the room.
- Shouting Down the Hallway: When Computer A wants to send a message to Computer B, it shouts the message down the main hallway wire. Every single computer hears the shout, but only Computer B pays attention to it.
3. **Ring topology** - s like a human chain holding hands: if just one person lets go, the whole chain breaks
- The Circle (The Loop): Every computer connects directly to its two neighbors—one on the left and one on the right—forming a complete circle.
- Passing Notes: If Computer 1 wants to send a picture to Computer 4, it passes the note to Computer 2. Computer 2 hands it to Computer 3, and Computer 3 finally hands it to Computer 4.
- Who Goes First?: A computer will only pass along someone else's note if it doesn't have a note of its own to send first!
---
- **Router** - A Router is like a smart GPS navigation app: it looks at all available roads between networks and guides your data along the best path to reach its target destination 
- The Bridge Between Networks: A router's main job is to connect two or more different networks together (like connecting your private home Wi-Fi network to the massive public Internet).
- Finding the Best Path (Routing): When you click on a video, your computer packages that request into data packets. The router looks at the destination address and picks the fastest, safest road across the web to deliver those packets.
- **Switches** - A Switch is like a smart power strip for internet cables: it plugs lots of local devices together and delivers data directly to the exact target device without spamming everyone else
- The Connection Powerhouse: A switch is a box packed with plug sockets (called ports—usually 8, 16, 24, or more). Computers, printers, and gaming consoles plug directly into these ports using Ethernet cables to join the local network.
- Smart Direct Delivery: A switch learns and remembers which specific device is plugged into each port (using its MAC Address).
- Targeted Messaging: If Computer A wants to send a document to Printer B, the switch sends that data only to Printer B's port. It does not bother any other computer on the network!
---
- **Subnetting** - Subnetting is like turning one giant open-plan warehouse into separate, private offices with their own doors so everyone stays organized and secure
- Slicing the Cake: You have one big IP network (the whole cake), but you don't want every single computer in the building talking over each other in one huge room.
- Creating Smaller Neighborhoods (Subnets): You divide the big network into smaller, organized mini-networks (subnets)—like reserving one room for the Accounting team, one room for Human Resources, and one room for IT.
- The Rules (Subnet Mask): A special code called a subnet mask acts like a wall. It tells the computer: "This part of your IP address is your room number, and this part is your personal seat number inside that room."
--- 
### Subnets use IP addresses in three different ways
- **The Network Address** (192.168.1.0): - The Street Name: This isn't a specific house, but the name of the whole neighborhood. It tells the mailman, "Hey, this entire block of houses is called 192.168.1.0!" No individual computer can use this number as its own address because it represents the whole neighborhood.
- **The Host Address** (192.168.1.100): - Your Specific House Number: This is the exact house number assigned to your computer inside the neighborhood. It lets other computers on the same street send messages directly to your front door!
- **The default Gateway** (192.168.1.254): - The Security Guard / Exit Gate: This is the neighborhood's main exit gate (usually your router). If your computer wants to send a letter to a friend in a different city (the public Internet), it hands the letter to this exit guard, who opens the gate and sends it out into the world.
---
- **ARP** (Address Resolution Protocol) - ARP is just a computer shouting, "Who owns this desk number?" so it can figure out who to hand the letter to!
- The Address Book (ARP Cache): Every computer keeps a little notebook that lists two things together: a device's IP Address (its desk number) and its MAC Address (its real name or fingerprint).
- When It Doesn't Know: If Computer A wants to send a note to "Desk 5" (IP Address), but doesn't know who is actually sitting there (MAC Address), it can't deliver the note yet.
---
- **DHCP** (Dynamic Host Configuration Protocol) -  DHCP is an automatic system where your computer asks a host for an IP address, gets an offer, accepts it, and gets the final thumbs-up—all in a fraction of a second!
- DCHP Discover - Hey im new here is there anyone who can give me an IP address?
- DHCP Offer - Hey! Sure thing you can have 192.168.1.10
- DHCP Request - Yes that would be brilliant! ill start using 192.168.1.10
- DHCP ACK - okay great, You can use that ip address for 24hrs

# OSI models

- **OSI** (Open Systems Interconnection) -  The OSI model (or Open Systems Interconnection Model) is an absolute fundamental model used in networking. This critical model provides a framework
dictating how all networked devices will send, receive and interpret data.

## The 7 layers of the OSI model
7. **Application**(The app you use) - Is the user menu(GUI) of the internet—it takes complicated network data and turns it into readable websites, emails, and files you can actually interact with
- DNS finds the address.
- HTTP fetches the web page.
- SMTP delivers the email.
6. **Presentation**(Translator) - This layer acts as a translator for data to and from the application layer (layer 7). The receiving computer will also understand data sent to a computer in one
format destined for in another format. For example, when you send an email, the other user may have another email client to you, but the contents of the email
will still need to display the same.
5. **Session**(The Phone Call Host) - The session layer (layer 5) synchronises the two computers to ensure that they are on the same page before data is sent and received. Once these checks are in
place, the session layer will begin to divide up the data sent into smaller chunks of data and begin to send these chunks (packets) one at a time. This dividing up is
beneficial because if the connection is lost, only the chunks that weren't yet sent will have to be sent again - not the entire piece of the data (think of it as
loading a save file in a video game).
- Packets - Small chuncks of data that are sent from one computer to another.
4. **Transport**(The Delivery Truck Inspector) - This layer is responsible for the delivery of the data
 - 1. **TCP**(Transimission Control Protocol) - TCP trades speed for 100% accuracy. It is like sending a registered mail package where the driver insists on getting a signature for every single piece
 - pros
-  Super Accurate: Zero missing data! Perfect for downloading files, loading web pages, or sending emails where every word counts.
- Pacing Control: It talks to the other device so it doesn't flood it with too much data all at once.
- cons 
- Slower Speed: Because it constantly checks, counts, and confirms every packet, it takes extra time.
- Can Cause Delays: If one tiny piece goes missing, everything else has to stop and wait until that missing piece is re-sent and delivered.
- 2. **UDP**(User Datagram Protocol) - UDP trades speed for 100% accuracy. It is like sending a regular package where the driver doesn't care if it gets a signature or not.
- pros
- Blazing Fast: Much faster than TCP because it doesn't waste time checking for errors or waiting for confirmation replies.
- No Reserved Line: It doesn't lock up a continuous connection on your device like TCP does.
- cons
- Doesn't Care About Lost Data: If a packet drops, UDP keeps going without fixing it.
- Terrible on Bad Wi-Fi: If your internet is laggy or unstable, UDP will result in frozen video calls or glitchy games.
3. **Network**(The GPS or Mailman) - The third layer of the OSI model (network layer) is where the magic of routing & re-assembly of data takes place (from these small chunks to the larger chunk).
Firstly, routing simply determines the most optimal path in which these chunks of data should be sent.
- uses IP addresses to stamp destination home addresses on data, and routers act like GPS systems to send those packets down the fastest, most reliable roads
- OSPF(Open Shortest Path First) 
- RIP(Routing Information Protocol) 
- . What path is the shortest? I.e. has the least amount of devices that the packet needs to travel across.
- . What path is the most reliable? I.e. have packets been lost on that path before?
- . Which path has the faster physical connection? I.e. is one path using a copper connection (slower) or a fibre (considerably faster)?
2. **Data Link**(The Local House Delivery) - The data link layer focuses on the physical addressing of the transmission. It receives a packet from the network layer (including the IP address for the remote
computer) and adds in the physical MAC (Media Access Control) address of the receiving endpoint. Inside every network-enabled computer is a Network
Interface Card (NIC) which comes with a unique MAC address to identify it.
- Your personal name tag so the delivery person hands the package directly to you, not your roommate!
- **NIC**(The Network Interface Card) -  The NIC is the physical interface between the computer and the network. It is the physical connection between the computer and the network.
1. **Physical**(The Cable or Highway) - This layer is one of the easiest layers to grasp. Put simply, this layer references the physical components of the hardware used in networking and is the lowest
layer that you will find. Devices use electrical signals to transfer data between each other in a binary numbering system (1's and 0's).

# Packet and Frames
- Instead of shoving the whole giant, heavy box through the mail slot at once, you break it down into small pieces and send them in tiny, easy-to-carry envelopes.
- Packet (Layer 3): This is the Outer Envelope. It has the IP Address stamped on it (the street address for where it needs to travel across the internet).
- Frame (Layer 2): Inside that outer packet is the Inner Envelope. Once the packet reaches your local neighborhood, it peels off the IP wrapper to reveal the Frame—which holds the MAC Address (the name tag for your exact phone or laptop) and the actual puzzle piece inside!
### 4 Important Label Stickers
- **Time to live** (Expiration Date) - A self-destruct countdown timer.
- **Checksum** (Quality Seal) - A special math code that checks if the packet got damaged on its journey.
- **Source Address** (Return Address) - The IP address of the computer that sent the packet.
- **Destination Address** (Target Address) - The IP address of the computer that should receive the packet.
---
- **TCP/IP**  - The TCP/IP protocol consists of four layers
and is arguably just a summarised version of the OSI model. These layers are:
- Application
- Transport 
- Internet
- Network Interface
--- 
## TCP (Transmission Control Protocol/Internet Protocol)
- Stateful , Careful
Header - the first part of the packet that contains the information about the packet. It contains the following information:
1. Where it's going (IP & Ports)
- Source IP & Destination IP: The street address of your building vs. the target building's address.
- Source Port: A random temporary apartment door number your computer opens to send the message.
- Destination Port: The specific apartment door number on the server (like Door 80 for websites).
2. Keeping the Puzzle in Order (Numbers & Integrity)
- Sequence Number: The page number stamped on this specific package (e.g., "This is Page 1").
- Acknowledgement Number: The reply saying what page to send next (e.g., "I got Page 1, send me Page 2!").
- Checksum: A security seal that breaks if the box got crushed or damaged on the way.
3. The Package Contents & Directives (Data & Flags)
- Data: The actual item inside the box (like part of a web page image).
- Flags: Little colored sticky notes on top that tell the receiver what to do (like a "SYN" note for "Hello!" or an "ACK" note for "Got it!").
--- 
- SYN, SYN/ACK, ACK: Setting up the call (Handshake).
- DATA: The actual chat. file you ask for
- FIN: Saying a polite goodbye. finish
- RST: Emergency phone slam reset if theres a problem.

## UDP (User Datagram Protocol)
- Stateless , Careless
Header
- Time to Live (TTL): The self-destruct timer so lost packets don't circle the internet forever.
- Source Address & Destination Address: The IP addresses showing where the packet came from and where it needs to go.
- Source Port & Destination Port: The apartment doors on each computer so the right app gets the data.
- Data: The actual message, like a slice of your voice in a Discord call or your character moving in Fortnite!

## Ports 101
- a virtual slot or numbered communication channel inside your computer that allows it to sort and organize different types of internet traffic at the same time.
1. 0 – 1,023: The global rules (Web, Email).
- Port 21 (File Transfer Protocol) - This channel is used exclusively for hauling huge stacks of heavy files, like moving all the furniture from one house to another. It is the designated highway for pure file sharing.
- Port 22 (Secure Shell) -  This is a super-secure channel used by tech experts to sneak into another computer from far away. Everything sent through this pipe is encrypted in a secret code so spies can't read it.
- Port 50 (DNS) - Turns website names (like google.com) into IP addresses.
- Port 80: (HyperText Transfer Protocol) - he standard, open channel for looking at regular websites. Anyone can walk in and read the books, but it doesn't have a security guard at the door.
- Port 443 (HyperText Transfer Protocol Secure) - This is the modern, upgraded version of Port 80. It does the exact same thing (loads websites), but it wraps all the data in an unbreakable armored laser grid. This is what you use when buying toys online or typing passwords.
- Port 445 (Server Message Block SMB ) - This channel lets computers on the same home or office Wi-Fi network talk directly to each other. It is used to easily share a physical printer, or to drag-and-drop folders straight onto your sibling's computer.
2. 1,024 – 49,151: The gaming and app servers (Minecraft).
- Port 3389: (Remote Desktop Protocol RBP) - This channel lets you project your computer's screen onto a completely different computer across the world. It is like plugging a wireless controller into your school computer so you can control your gaming PC at home.
- Port 25565: Famous for being the channel used to host a Minecraft server!
3. 49,152 – 65,535: Your computer's temporary "Return Channels."
- Remember when we talked about the Source Port—the temporary channel you create just to listen for a reply? This is where your computer picks those numbers!
- They are completely random, temporary, and private.


# Extending your network

### Port Forwarding
- **Port Forwarding:** (The Receptionist's Rule): Without Port Forwarding, if someone on the internet drives up to the hotel on Port 80, the door is locked.
- **Public IP:** - Your computer's public IP address, which is the address you use to connect to the internet. 
- **Private IP:** - Your computer's private IP address, which is the address you use to connect to your local network. 

### Firewalls 101
- **Firewall** - Decides who gets to come in, where they are allowed to go, and which doors (ports) they can use.
- **Antivirus** - Scans whatever actually made it inside and destroys it if it's a bad file.

### Firewall Category 
1. Stateful Firewall (The Smart Guard with a Memory) - It tracks the whole conversation (the "state" of the connection). It remembers who started talking to whom.
- Smart, remembers the whole story, uses more computer memory. Great for daily network security.
- Example: If you open a browser to visit a website, the firewall remembers you asked for it. When the website replies, the firewall automatically lets the data back in because it says, "Oh yeah, I remember you ordered this data!"
2. Stateless Firewall (The Dumb Guard) - It has zero memory. It looks at every single packet individually and checks a simple list of strict rules: "Is this going to Port 80? Yes? Pass. No? Block."
- Dumb, reads rules like a robot, super fast. Great for high-speed networks and stopping traffic floods.
- Example: It doesn't care if you requested the website data or if a hacker randomly sent it to you. It only checks: "Does this packet follow Rule #1?"

### VPN 
- The VPN (Virtual Private Network) is a way to connect to a network that is not directly accessible from your computer. It creates a secure tunnel between your computer and the VPN server, allowing you to access the network as if you were physically connected to it.
#### VPN Technology
- PPP (The Safe Box & Secret Key): It locks up your data and checks your ID (key) to make sure it's really you. But it has no wheels—it can't travel anywhere on its own.
- PPTP (The Fast, Cheap Delivery Van): It takes PPP's safe box and actually drives it across the internet! It's super fast and easy to set up, but the locks on the van are cheap and easy for bad guys to break.
- IPSec (The Heavy Armored Tank): A completely different, modern way to move data. It is harder to set up, but it puts your data inside a heavy-duty armored tank with super strong locks that nobody can crack.

### LAN Networking Devices

- **Router** - Connects your local network to the outside world (the Internet) or to a completely different network. It inspects traffic and decides how to route it out of your building.
- **Switch** - Connects all devices in the same room or floor together. If Computer A wants to send a message to Printer B in the same building, the switch directs the traffic directly between them.
- **VLAN (Virtual Local Area Network)** - Creates virtual, separate networks using the same physical switch. It acts like an invisible wall inside the hallway—putting guests on one side and official staff on the other so they can't talk to or see each other, even though they're plugged into the exact same box.
- The separate locked rooms inside.

# DNS in detail

- **DNS** is a system that translates domain names into IP addresses. It's like a phone book for the internet. When you type a website's name into your browser, like "google.com," DNS translates that into an IP address, which is the computer's address on the internet. 

### TLD( Top Level Domain) 
-  **gTLD (Generic Top Level)** -  gTLD was meant to tell the user the domain name's purpose; for example, a .com would be for commercial purposes, .org for an organisation, .edu for education and .gov for government
- **ccTLD (Country Code Top Level)** -  was used for geographical purposes, for example, .ca for sites based in Canada, .co.uk for sites based in the United Kingdom and so on.

### Second Level Domain 
- Taking tryhackme.com as an example, the .com part is the TLD, and tryhackme is the Second Level Domain. When registering a domain name, the second-level domain is limited to 63 characters + the TLD and can only use a-z 0-9 and hyphens (cannot start or end with hyphens or have consecutive hyphens).

## Subdomain
- A subdomain sits on the left-hand side of the Second-Level Domain using a period to separate it; for example, in the name admin.tryhackme.com the admin part is the subdomain.
- But the length must be kept to 253 characters or less. There is no limit to the number of subdomains you can create for your domain name.
## DNS record types 

- **A Record** (The Home Address): Gives you the basic street address using standard numbers (IPv4).

- Analogy: "TryHackMe lives at House #104.26.10.229."

- **AAAA Record** (The New Modern Address): Does the exact same thing as an A Record, but uses longer, newer numbers (IPv6) because the world ran out of regular house numbers.

- Analogy: "TryHackMe’s brand-new futuristic address is #2606:4700..."

- **CNAME Record** (The Nickname): Tells you that one name is actually just a nickname for another name.

- Analogy: You ask for "Store", and the card says: "Oh, Store is just a nickname for Shopify's House. Go look up Shopify's address instead!"

- **MX Record** (The Mailbox): Points specifically to where emails should be sent, not website visits. It comes with a priority number (like #1, #2, #3) so if the main mail carrier is busy, the mail goes to the backup carrier!

- Analogy: "Send all letters for TryHackMe to Google Mailbox #1. If it's full, try Google Mailbox #2."


- Step 1: Check Your Own Memory (Local Cache)
Before leaving the house, your computer thinks: "Did I visit TryHackMe yesterday?"
If it remembers the address, it goes straight there! If it forgot, it asks for help.

- Step 2: Ask the Neighborhood Guide (Recursive DNS Server)
Your computer asks your ISP's guide (the Recursive Server).

If it knows: "Oh, everyone visits Google and TryHackMe! Here’s the map." (Journey ends!)

If it doesn't know: The guide says, "I don't know, but I'll go find out for you!" and starts a relay race.

- Step 3: Ask the Grandfather of the Internet (Root Server)
The guide runs to the Root Server, who knows where everything generally is.

The Root Server says: "I don't have the exact house address for tryhackme.com, but I know who handles all the .com addresses! Go ask the .com Manager over there."

- Step 4: Ask the Neighborhood Manager (TLD Server)
The guide runs to the .com Manager (Top Level Domain Server).

The manager looks at their list and says: "Ah, TryHackMe! Their official records are kept at Cloudflare's filing cabinet (Authoritative Server). Go ask them!"

- Step 5: Ask the Official Record Keeper (Authoritative Server)
The guide finally arrives at the Authoritative Nameserver. This server holds the actual master rulebook for the domain.

It checks the book and hands over the exact house number: 104.26.10.229.

- Step 6: Bring It Home & Set a Timer (TTL)
The guide runs back to your computer with the address.
Before handing it over, the guide writes it down on a Sticky Note with an expiration timer (TTL / Time To Live)—for example, 300 seconds.

# HTTP in detail
- **http** (HyperText Transfer Protocol) - HTTP is what's used whenever you view a website, developed by Tim Berners-Lee and his team between 1989-1991. HTTP is the set of rules used for communicating with web servers for the transmitting of webpage data, whether that is HTML, Images, Videos, etc.
- **https** (HyperText Transfer Protocol Secure) - HTTPS is the secure version of HTTP. HTTPS data is encrypted so it not only stops people from seeing the data you are receiving and sending, but it also gives you assurances that you're talking to the correct web server and not something impersonating it.

- **Url** (Unit Resource Locator) - If you’ve used the internet, you’ve used a URL before. A URL is predominantly an instruction on how to access a resource on the internet. The below image shows what a URL looks like with all of its features (it does not use all features in every request).
Scheme: This instructs on what protocol to use for accessing the resource such as HTTP, HTTPS, FTP (File Transfer Protocol).

- **User**: Some services require authentication to log in, you can put a username and password into the URL to log in.

- **Host**: The domain name or IP address of the server you wish to access.

- **Port**: The Port that you are going to connect to, usually 80 for HTTP and 443 for HTTPS, but this can be hosted on any port between 1 - 65535.

- **Path**: The file name or location of the resource you are trying to access.

- **Query String**: Extra bits of information that can be sent to the requested path. For example, /blog?id=1 would tell the blog path that you wish to receive the blog article with the id of 1.

- **Fragment**: This is a reference to a location on the actual page requested. This is commonly used for pages with long content and can have a certain part of the page directly linked to it, so it is viewable to the user as soon as they access the page.

## HTTP methods
- GET Request - This is used for getting information from a web server.
- POST Request - This is used for submitting data to the web server and potentially creating new records
- PUT Request - This is used for submitting data to a web server to update information
- DELETE Request -This is used for deleting information/records from a web server.

## HTTP status codes

- **100-199** - Information Response - These are sent to tell the client the first part of their request has been accepted and they should continue sending the rest of their request. These codes are no longer very common.
- **200-299** - Success - This range of status codes is used to tell the client their request was successful.
- **300-399** - Redirection - These are used to redirect the client's request to another resource. This can be either to a different webpage or a different website altogether
- **400-499** - Client Errors - Used to inform the client that there was an error with their request. 
- **500-599** - Server Errors - This is reserved for errors happening on the server-side and usually indicate quite a major problem with the server handling the request.

## Common HTTP Status Codes

- **200** - OK	The request was completed successfully.
- **201** - Created	A resource has been created (for example a new user or new blog post).
- **301** - Moved Permanently	This redirects the client's browser to a new webpage or tells search engines that the page has moved somewhere else and to look there instead.
- **302** - Found	Similar to the above permanent redirect, but as the name suggests, this is only a temporary change and it may change again in the near future.
- **400** - Bad Request	This tells the browser that something was either wrong or missing in their request. This could sometimes be used if the web server resource that is being requested expected a certain parameter that the client didn't send.
- **401** - Not Authorised	You are not currently allowed to view this resource until you have authorised with the web application, most commonly with a username and password.
- **403** - Forbidden	You do not have permission to view this resource whether you are logged in or not.
- **405** - Method Not Allowed	The resource does not allow this method request, for example, you send a GET request to the resource /create-account when it was expecting a POST request instead.
- **404** - Page Not Found	The page/resource you requested does not exist.
- **500** - Internal Service Error	The server has encountered some kind of error with your request that it doesn't know how to handle properly.
- **503** - Service Unavailable	
This server cannot handle your request as it's either overloaded or down for maintenance.

## Common Request Headers
- ﻿These are headers that are sent from the client (usually your browser) to the server.
- **Host**: Some web servers host multiple websites so by providing the host headers you can tell it which one you require, otherwise you'll just receive the default website for the server.
- **User-Agent**: This is your browser software and version number, telling the web server your browser software helps it format the website properly for your browser and also some elements of HTML, JavaScript and CSS are only available in certain browsers.
- **Content-Length**: When sending data to a web server such as in a form, the content length tells the web server how much data to expect in the web request. This way the server can ensure it isn't missing any data.
- **Accept-Encoding**: Tells the web server what types of compression methods the browser supports so the data can be made smaller for transmitting over the internet.
- **Cookie**: Data sent to the server to help remember your information (see cookies task for more information).

## Common Response Headers
- These are the headers that are returned to the client from the server after a request.
- **Set-Cookie**: Information to store which gets sent back to the web server on each request (see cookies task for more information).
- **Cache-Control**: How long to store the content of the response in the browser's cache before it requests it again.
- **Content-Type**: This tells the client what type of data is being returned, i.e., HTML, CSS, JavaScript, Images, PDF, Video, etc. Using the content-type header the browser then knows how to process the data.
- **Content-Encoding**: What method has been used to compress the data to make it smaller when sending it over the internet.


# How website work

- **Client side**(Frontend) - The client is the user's web browser. It is the client that sends the request to the server and receives the response from the server.
- **Server side**(Backend) - The server is the web server that hosts the website. It is the server that receives the request from the client and sends the response back to the client.
- **HTML** - The HTML file is the client's web browser that displays the website. It is the client's web browser that displays the website. It is the client's web browser that displays the website. 
- **Javascipt** - The Javascript file is the client's web browser that displays the website. It is the client's web browser that displays the website. It is the client's web browser that displays the website. 
- **HTML Injection** - (also known as a rendering attack) is a web security vulnerability that occurs when a web application accepts user input and renders it directly onto a webpage without proper sanitization or encoding.

# Putting it all together
- **Load Balancer** - load balancer acts like a traffic cop. When you visit a website, it checks which server has the least amount of work to do, and sends your request directly to that free server so the website loads super fast!
- **CDN (Content Delivery Network)** - CDN is a network of servers that are geographically distributed to deliver content to users with the lowest latency. s like putting a mini toy warehouse in every neighborhood around the world.
- **Databases** - Databases are a way to store and organize data. They are like a giant file cabinet that stores all your data in one place. 
- **Waf (Web Application Firewall)** - WAF is a security system that protects web applications from attacks. It is like a security guard that watches over your website and makes sure no one can break in and steal your data.
- **Web Servers** - Web servers are like the main hub of your website. They are like a giant computer that stores all your website's data and makes it available to the world. 
- **Virtual Host** - Virtual host is a way to run multiple websites on the same server. It is like having multiple houses on the same street. 
- **Static Cotent** - he Design & Frame: The colors, logos, layout, fonts, and background images. It’s like the empty form or the layout of a passport—it looks the same for everyone.
- **Dynamic Content** - The content that changes based on the user’s actions grabs the dynamic data from a database and drops it right into the static design frame before sending the finished page to your screen!
- **Scripting and Backend Languages** - Scripting and backend languages are like the code that makes your website work. They are like the instructions that tell the computer what to do. 

# Flow
- Request in your browser
- Check local cache for ip address
- Check you recursive DNS Server for Address
- Query root server to find authorative DNS server
- Authorative DNS server responds with IP address for website
- Request passes through a web application firewall
- Request passes through a load balancer
- Connect to Webserver on port 80 or 443
- Web server recives the GET request
- Web application talks to the database
- Your browser renders the HTML into a viewable website

# The CIA triad

- **Confidentiality** ensures that sensitive data can only be accessed by authorized individuals. If confidentiality is not maintained, unauthorized individuals can access the data, resulting in financial loss, privacy violations, or legal consequences.
- **Integrity**  ensures that unauthorized individuals do not modify data. Without integrity, data can be altered and no longer be trusted. Unauthorized changes in data can sometimes lead to dangerous consequences.
- **Availability** ensures that data and services are available to authorized users when needed. Although it comes as the third and last pillar of the CIA Triad, it is no less important than the other two. Most businesses rely heavily on their digital services, and if those services become unavailable, there is no more business, causing a huge loss to them. Even a short period of downtime can have serious consequences on the businesses and users.

## Security Mindset
- Was sensitive data exposed to unauthorized individuals?
- Was data being modified without permission?
- Were systems or services unavailable to users when they needed? 

# Cryptography Concepts

## Understanding the basics
- **Cryptography** - The science of encoding and decoding messages. It's a way to protect data from being read by unauthorized individuals.
- **Plaintext** - A message you can read normally. Like HELLO or Patient name: Alice Smith.
- **Ciphertext** - A scrambled version that's not supposed to make sense. Like KHOOR or Sdwlhqw qdph: Dolfh Vplwk.
**Key** - The secret ingredient that controls how scrambling and unscrambling work. Think of it as a password that the algorithm uses.
**Algorithm** - The public recipe—the set of steps that explain how to use the key on the message. Everyone can know the algorithm. Security comes from keeping the key secret.

- Encryption process: plaintext + encryption algorithm + key  → ciphertext
- Decryption process: ciphertext + decryptiong algorithm + key   → plaintext

- **Symmetric Encryption** - The most common type of encryption. It uses the same key for both encryption and decryption. It's fast and easy to use, but it's also the most vulnerable. If the key is compromised, the data can be read by anyone.
- A house door where everyone in the family has a duplicate copy of the same physical key.

- e key distribution problem, and it's the Achilles' heel of symmetric encryption when used alone.

- caesar cipher - a simple substitution cipher that shifts letters by a fixed number of positions in the alphabet. For example, a shift of 3 would turn "A" into "D", "B" into "E", and so on. 

- Advance Encyption Standard - are vastly more complex and secure. But they follow the same basic idea: algorithm + key + plaintext → ciphertext.

- **Asymmetric Encryption** - Uses two different keys: a public key and a private key. The public key can be shared with anyone, but the private key is kept secret. 
- A mailbox on your front porch. Anyone can drop a letter through the slot (Public Key), but only you have the cabinet key (Private Key) to open it and read the mail.

## HYBRID APPROACH
1. Your browser requests the website's public key.
2. The website sends back its public key wrapped in a certificate (more on this shortly).
3. Your browser and the website use asymmetric encryption to agree on a shared secret (a symmetric key) without anyone else being able to see it.
4. From there on, they switch to fast symmetric encryption using that shared secret for the rest of the session.
- Asymmetric encryption solves the problem of key distribution.
- Symmetric encryption handles the heavy lifting because it's way faster.

- **Certificate Authority** - A trusted third party that issues certificates to websites. 

# Become a hacker

- **Offensive Security** - focuses on proactively testing systems by attempting to break into them, with the goal of identifying weaknesses before real attackers can exploit them.

## Core offensive Security Terms
- **Red Teaming:**(Realworld testing) A structured, authorized attack methodology that simulates a real adversary to test the effectiveness of defenses and find
vulnerabilities within a defined scope
- **Penetration Test:**(The Inspection) A structured security assessment where an authorized tester attempts to identify and exploit vulnerabilities within a defined
scope to understand real-world risk
- **Vulnerability:**(The flaw) A weakness or flaw in a system, application, or configuration that an attacker could abuse
- **Exploit:**(The trick) A technique or method used to take advantage of a vulnerability to achieve a specific outcome, such as accessing restricted
functionality or data
- **Scope:**(The rules) The boundaries of what is allowed to be tested during an engagement. Scope defines which systems, applications, and actions are
permitted, and what is off-limits

- **Gobuster** - A tool for finding files and directories on a web server. It is a command-line tool that uses a dictionary to find files and directories on a web server. 

- **Hydra** - The command-line tool used to perform the dictionary attack.

## Thinking Like a Hacker

---
### 1. Core Philosophy
Ethical hacking requires looking beyond intended functionality to discover how a system can be misused, manipulated, or bypassed—always within authorized scope.
---
### 2. Practical Principles

* **Ask "What If?":** Never assume logic is secure just because it works on the UI.
* **Input Unpredictability:** Supply unexpected data types, sizes, and formats to catch missing server-side validation.
* **Vulnerability Chaining:** Link multiple minor flaws together to demonstrate maximum risk and business impact.
* **Adversarial Perspective:** Approach every target with a specific threat model: *What is the most valuable asset here, and how can it be compromised?*

## Authenticated Attack Surface: A Valuable Target
---
### 1. Core Threat
Valid credentials allow an attacker to bypass perimeter security and act with the legitimate permissions of a compromised account.
---
* **Sensitive Functionality:** Core operations (e.g., executing transactions, modifying records, triggering processes) reserved strictly for logged-in users.
* **User Data & PII:** Private personal data (emails, addresses, account histories) subject to theft, abuse, or black-market resale.
* **Administrative Controls:** High-privilege settings and user management panels that grant full control over application state and access.
* **Expanded Exploit Surface:** Additional endpoints, API parameters, and backend workflows exposed only after authentication, enabling privilege escalation and lateral movement.

## Key terms

- **Scope:** The exact systems and actions allowed during a security test
- **Vulnerability:** A hidden weakness in a system that an attacker could use to break in
- **Exploit:** A method or technique that takes advantage of a vulnerability
- **Enumeration:** Collecting details about a system, users, and services to find weak points
- **Credentials:** Login details such as usernames and passwords that unlock access
- **Authentication:** The step that checks if someone or something is really who they claim to be when logging in
- **Dictionary attack:** Trying a predefined wordlist to guess a password or username

# Essential Defensive Controls
---
## Defense Quick Reference

| Security Control | Primary Function | Attacks / Threats Mitigated |
| :--- | :--- | :--- |
| **Rate Limiting** | Throttles excessive request volume per IP/User | Brute-force attacks (Hydra), web scraping, DoS |
| **Parameterized Queries** | Separates database code from user data | SQL Injection (SQLi) |
| **Input Sanitization** | Cleans/escapes untrusted user input | Cross-Site Scripting (XSS), HTML injection |
| **Access Control (RBAC)** | Enforces server-side permissions per user | IDOR, horizontal/vertical privilege escalation |
| **Secure Cookie Flags** | Secures session tokens (`HttpOnly`, `SameSite`) | Session hijacking, XSS token theft, CSRF |
| **CAPTCHA / WAF** | Identifies bots & filters malicious traffic payloads | Automated credential stuffing, Gobuster scans |


# Become a defender

- **Defensive Security** - focuses on protecting systems by implementing security measures, monitoring for threats, and responding to incidents to prevent or mitigate attacks.

    ## Defensive questions
    1. **Assets**(What am I protecting?) - Identify the critical assets that need protection, such as sensitive data, intellectual property, and essential services.
    - City Analogy: In a real city, police and guards need to protect houses, public buildings, and citizens.
    - Security Equivalent: In tech, you are protecting physical/cloud servers, company databases, employee laptops, and user accounts.
    - Why it matters: You can't put a guard on a building you don't know exists. Step 1 of defense is knowing every system you own.
    2. **Visibility**(Can you see what you are protecting?) - Implement monitoring and logging to gain visibility into system activity, network traffic, and user behavior.
    - City Analogy: A city uses security cameras, neighborhood watches, and police patrols to keep an eye on things.
    - Security Equivalent: Security teams use system logs (records of who opened what file), network traffic monitoring, and security alerts.
    - Why it matters: If an attacker sneaks in quietly, you won't know they are there unless you have "cameras" (logging tools) watching the network.
    3. **Detection**(What classifies suspicious behavior?) -  Define what constitutes suspicious or anomalous behavior, and establish detection mechanisms to identify potential threats.
    - City Analogy: Someone walking down the street checking if car door handles are unlocked, or a unknown car slowly circling a neighborhood 10 times at 3 AM.
    - Security Equivalent: A single user trying 50 wrong passwords in 10 seconds, or a user account logging in from two different countries at the exact same time.
    - Why it matters: You need to know what "normal" looks like so you can spot "weird" activity immediately.
    4. **Response**(How do you respond to threats?) - Develop and implement incident response plans, including procedures for containment, eradication, and recovery from security incidents.
    - City Analogy: Calling the police, setting up road blockades, or enforcing a city curfew to trap a criminal.
    - Security Equivalent: Firewall rules blocking a bad actor's IP address, or automatically locking an account after too many bad password attempts.
    - Why it matters: Seeing a thief on camera (visibility) is useless if you don't have a way to lock the door and stop them (active response).

    ## What can you do as a defender?

    - **Prevention**: Putting security controls in place to stop attacks before they happen, such as firewalls, antivirus software, and regular patching.
    - **Detection**: Monitoring systems and networks to identify suspicious or malicious activity through logs, alerts, and security tools.
    - **Mitigation**: Taking action during an incident to limit damage, such as blocking traffic, isolating affected systems, or disabling compromised accounts.
    - **Analysis**: Investigating what happened, how it happened, and which systems were affected by reviewing logs and other evidence.
    - **Response and Improvement**: Recovering from the incident and improving defenses to reduce the risk of similar attacks in the future.

    ## Defensive Mindset
    - **Threat anticipation**: Review the systems you aim to protect and ask, "What if?" Imagine realistic paths an attacker may take to achieve their goal.
    - **Attack awareness**: Attacks typically follow recognizable stages. Studying common attack chains and frameworks is incredibly useful for defenders.
    - **Risk prioritization**: Not every part of your system carries equal risk. Defenders should identify high-value systems and targets.
    - **Continuous adaptation**: Defense is not a one-time set up. Threats and attackers evolve, techniques change, and vulnerabilities emerge.

    ## Key Terminology
    - **Blue Team**: A group of cyber security defenders tasked with protecting systems and responding to threats
    - **Client Infrastructure**: The networks, servers, devices, and applications belonging to an organization that need protection
    - **Visibility**: The ability to see and monitor activity across systems to spot potential issues
    - **Threat**: A potential danger, such as a hacker or malware, that could harm systems or data
    - **Prevention**: Stopping threats before they can cause harm by blocking, restricting, or reducing opportunities for attack
    - **Detection**: The process of identifying threats or suspicious activity in networks and systems
    - **Mitigation**: Actions taken to reduce or stop the impact of a threat once it's identified
    - **Risk**: The likelihood and potential impact of a threat successfully harming an organization

    ## City Analogy
    1. Employee Devices (Laptops, Phones, Tablets) - The homes of your employees. They contain personal and work-related information that needs protection.
    2. Web Servers - The office buildings where your company's services and data are hosted. They are the central hub of operations.
    3. Mail Servers - The post offices that handle all incoming and outgoing communications. They need to be secure to prevent interception or tampering.
    4. Firewalls - The security guards stationed at the entrances of your buildings. They control who can enter and exit, and what they can bring with them.
    5. Internet - The roads and highways that connect your buildings to the outside world. They are the pathways through which data travels, and they need to be monitored for suspicious activity.

    | Infrastructure Component | Real-World Purpose | City Analogy |
    | :--- | :--- | :--- |
    | **Employee Devices** | Workstations where users access resources | Homes |
    | **Web Server** | Hosts public applications and sites | Shops / Public Buildings |
    | **Mail Server** | Handles organization email traffic | Post Office |
    | **Firewall** | Filters traffic entering and leaving the network | City Gate |
    | **Internet** | Untrusted external networks | Outside the City |


    | Infrastructure Component | Risk / Threat Scenario | Defensive Controls |
    | :--- | :--- | :--- |
    | **Employee Devices** | Phishing clicks, unsafe downloads, malware execution | Antivirus/EDR, OS & software patch management |
    | **Web Server** | Web application attacks, unauthorized data extraction | WAF, HTTPS encryption, input validation, rate limiting |
    | **Mail Server** | Deceptive emails, phishing, malicious attachments | Email spam filters, attachment sandboxing, SPF/DKIM |
    | **Firewall** | Unsolicited connection attempts, network port scans | Strict IP access control lists (ACLs), IP reputation blocking |
    | **Outside Internet** | External botnets, automated probes, brute-force attacks | Restrict inbound traffic, continuous network flow monitoring |
