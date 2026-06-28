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

---

## 📸 Screenshot
<img width="1918" height="970" alt="image" src="https://github.com/user-attachments/assets/c4f36b25-1e8f-4c31-9000-4d3debb843e2" />
