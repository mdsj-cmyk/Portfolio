# Home Lab: System Maintenance, Hardware Upgrades & Troubleshooting

## Overview
This home lab environment is used to practice **system diagnostics, hardware upgrades, and structured troubleshooting workflows**, reflecting real-world IT support and infrastructure operations.

Focus areas include:  
- Hardware diagnostics and upgrades  
- Storage migration and system optimization  
- System stability testing  
- Root-cause analysis and troubleshooting documentation  

---

## Tools & Technologies
- **Operating Systems:** Windows 10/11, Linux (bootable USB)
- **Hardware:** Dell OptiPlex 3020 SFF, Nvidia Quadro P1000, SSD/HDD storage
- **Software:** Macrium Reflect, DiskPart, GParted, Windows Disk Management
- **Networking Tools:** ping, ipconfig, tracert
- **Diagnostics:** Event Viewer, Task Manager, Resource Monitor, BIOS utilities

---

## Lab System
**Primary workstation:** Dell OptiPlex 3020 SFF  

**Upgrades & Tasks Performed:**  
- CPU upgrade to Intel Core i7-4790  
- Memory upgrade from 8GB to 16GB DDR3  
- **Storage migration from HDD to SSD**:
  - Cloned OS and data using **Macrium Reflect**  
  - Prepared SSD with **DiskPart** and **Windows Disk Management**  
  - Booted from **Windows USB to Linux/GParted** to erase, move and resize partitions  
  - Created **rescue media** for safe migration  
- Installed and tested Nvidia Quadro P1000 4GB GPU  
- BIOS configuration and system compatibility checks  
- Hardware diagnostics and stability testing  

---

## Network Environment
Configured a small local network including:  
- Desktop workstation  
- Wireless modem/router  
- Network printer  

**Tasks:**  
- LAN configuration  
- Printer installation and setup  
- Basic network diagnostics (`ping`, `ipconfig`, `tracert`)  

**System Diagnostics Tools:**  
- Windows Event Viewer, Task Manager, Resource Monitor  
- BIOS hardware diagnostics  
- Monitoring utilities  

---

## Troubleshooting Methodology
1. Identify system symptoms  
2. Review logs and error events  
3. Verify hardware configuration and drivers  
4. Check performance and resource usage  
5. Isolate hardware components if necessary  
6. Evaluate power and thermal constraints  
7. Determine root cause  
8. Implement corrective action and confirm stability  

---

## Example Case 1: HDD-to-SSD Migration
**Situation:** Upgrade an aging HDD to SSD for improved performance.  

**Challenges:** No direct transfer cable for hdd; preserve OS, apps, and data.  

**Solution:**  
- Used **DiskPart** and **Disk Management** to clean, format, and verify SSD
- Cloned OS/data with **Macrium Reflect**  
- Created **rescue media** to ensure bootable recovery
- Booted from **Windows USB to Linux/GParted** to format hdd (installed), then move & expand the partition copy on the SSD (USB to SATA 2.5")    

**Skills Demonstrated:**  
- Disk cloning, partition management, and boot recovery  
- Cross-platform troubleshooting (Windows + Linux)  
- Problem-solving under hardware constraints  
- Structured documentation  

---

## Example Case 2: GPU Artifacting During System Upgrade
**Situation:** Booted, situational graphical artifacting and instability after CPU, RAM, SSD, and GPU upgrades.  

**Troubleshooting:**  
- Verified GPU drivers and OS configuration  
- Checked temperatures and hardware seating  
- Reviewed Windows Event Viewer logs  
- Tested system stability under load  
- Isolated GPU to identify issue  

**Root Cause & Resolution:**  
- SFF power supply insufficient for GPU under load  
- Confirmed instability due to power limitations, not defective hardware  

---

## Skills Highlighted
- System troubleshooting & hardware diagnostics  
- Disk cloning, partitioning, and boot recovery  
- GPU and system stability testing  
- Cross-platform problem-solving (Windows + Linux)  
- Structured documentation and workflow implementation  
