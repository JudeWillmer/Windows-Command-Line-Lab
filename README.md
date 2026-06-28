# 🖥️ Lab 1 - Information Gathering (Windows 10 Pro)

## Objective

Practice gathering essential workstation, user, and network information before beginning troubleshooting. These commands are commonly used by IT Support and Help Desk technicians during the initial investigation of support incidents.

---

## 🖥️ Workstation Identification

### Commands

```cmd
hostname
whoami
ipconfig /all
```

### Scenario (IT Support)

An end user contacts the IT Help Desk reporting that they cannot access company resources. Before making any changes, the technician gathers basic workstation and network information to verify the correct device, confirm the logged-in user, and review the workstation's network configuration.

### Purpose

These commands provide the essential information required before troubleshooting begins.

- **hostname** identifies the workstation name, allowing the technician to verify they are connected to the correct computer and locate it within Active Directory, Microsoft Intune, or an asset inventory.
- **whoami** confirms which user is currently logged into the workstation, helping verify the correct user profile is being investigated.
- **ipconfig /all** displays detailed network configuration, including the IP address, subnet mask, default gateway, DNS servers, DHCP status, MAC address, and domain information. This helps identify network configuration issues before applying any fixes.

---

## 📸 Screenshot
<img width="1918" height="971" alt="image" src="https://github.com/user-attachments/assets/3540cb52-39d0-4e06-9c52-6a26c6c1bf26" />

---

## 🖥️ System Information

### Command

```cmd
systeminfo
```

### Scenario (IT Support)

A workstation issue cannot immediately be identified, so the technician gathers detailed operating system and hardware information before escalating the incident or continuing with advanced troubleshooting.

### Purpose

The **systeminfo** command provides detailed information about the workstation, including:

- Windows edition and build
- Computer name
- Domain membership
- System manufacturer and model
- Installed RAM
- Processor information
- Boot time
- Installed hotfixes
- Network adapter information

This information helps technicians verify system specifications, identify outdated systems, confirm domain membership, and collect information required for documentation or escalation.

---

## 📸 Screenshot
<img width="1918" height="971" alt="image" src="https://github.com/user-attachments/assets/33af6079-8d2c-435e-b245-8e59a5f9f17a" />

---

## 🖥️ Running Processes

### Command

```cmd
tasklist
```

### Scenario (IT Support)

An end user reports that their computer is running slowly or that an application has become unresponsive. Before ending any processes, the technician reviews the currently running processes to identify potential resource usage or hung applications.

### Purpose

The **tasklist** command displays every running process along with its Process ID (PID) and memory usage.

This allows technicians to:

- Identify running applications
- Locate processes consuming excessive memory
- Obtain Process IDs (PIDs) before using **taskkill**
- Confirm whether expected services and applications are running

Reviewing processes first helps prevent unnecessary termination of critical Windows services and supports informed troubleshooting decisions.

## 📸 Screenshot
<img width="1918" height="970" alt="image" src="https://github.com/user-attachments/assets/c4f36b25-1e8f-4c31-9000-4d3debb843e2" />

# Lab 2 - Network Troubleshooting (Windows 10 Pro)

## Objective

Practice troubleshooting common network connectivity and DNS-related issues using built-in Windows Command Prompt tools. Learn when to use each command to diagnose network problems and verify workstation connectivity.

---

## 🌐 IP Configuration

### Commands

```cmd
ipconfig
ipconfig /release
ipconfig /renew
```

### Scenario (IT Support)

An end user reports they are experiencing network connectivity issues after reconnecting their workstation to the company network. The technician reviews the current IP configuration, releases the existing DHCP lease, and requests a new IP address to restore network connectivity.

### Purpose

These commands are commonly used to refresh or verify a workstation's network configuration when troubleshooting connectivity issues.

* **`ipconfig`** displays the workstation's current IP configuration, allowing the technician to quickly verify the assigned IP address, subnet mask, and default gateway.
* **`ipconfig /release`** releases the current DHCP-assigned IP address, disconnecting the workstation from the network so a new address can be requested.
* **`ipconfig /renew`** requests a new IP address from the DHCP server. This is commonly used after moving desks, reconnecting to the network, or resolving DHCP-related connectivity issues.


### Screenshot
<img width="1918" height="841" alt="image" src="https://github.com/user-attachments/assets/0352802b-76d2-413e-b3b0-a05843d7e7c6" />
<img width="1918" height="792" alt="image" src="https://github.com/user-attachments/assets/232e624a-01cb-4eb0-9f80-db5010184cb0" />

## 🌐 DNS Troubleshooting

### Commands

```cmd
ipconfig /flushdns
nslookup
```

### Scenario (IT Support)

A user reports they cannot access a company website or internal resource by hostname. The technician clears the local DNS cache and verifies that DNS records resolve correctly using the configured DNS server.

### Purpose

These commands help verify and troubleshoot DNS-related problems that can prevent users from accessing websites or internal resources.

* **`ipconfig /flushdns`** clears the local DNS resolver cache, removing outdated or incorrect DNS records that may cause name resolution issues.
* **`nslookup`** queries a DNS server to verify that hostnames resolve to the correct IP addresses, helping determine whether a problem is caused by DNS or general network connectivity.


### Screenshot
<img width="1918" height="660" alt="image" src="https://github.com/user-attachments/assets/02759928-0e71-4049-80db-0364268b13cc" />

## 🌐 Connectivity Testing

### Commands

```cmd
ping
tracert
```

### Scenario (IT Support)

A user reports they cannot connect to a network resource. The technician tests basic connectivity to a remote host and traces the network path to identify where communication may be failing.

### Purpose

These commands are used to verify network connectivity and identify where communication problems occur.

* **`ping`** tests whether another device or server is reachable across the network by sending ICMP Echo Requests and measuring the response time.
* **`tracert`** displays every network hop between the workstation and the destination, helping technicians identify where connectivity or latency issues occur along the route.


### Screenshot
<img width="1918" height="783" alt="image" src="https://github.com/user-attachments/assets/44a35332-33a0-4890-b6c1-0941fe0671d5" />
