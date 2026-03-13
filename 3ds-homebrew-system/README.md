# Nintendo 3DS Custom Firmware & Multi‑Platform Retro Environment

## Overview
Configured a Nintendo 3DS handheld system with **custom firmware and homebrew software** to support a curated multi-platform legacy gaming environment.  

The system integrates software from multiple classic platforms including NES, SNES, GBA, DS, N64, Virtual Boy, Sega Genesis, and native 3DS titles while maintaining system stability and usability.

This project demonstrates **embedded system modification, firmware management, software packaging, wireless file transfer, remote viewing, emulator configuration, and cross-platform troubleshooting.**

---

## Objectives

- Configure a stable custom firmware environment for the Nintendo 3DS
- Support multiple retro gaming platforms on a single handheld device
- Implement wireless file transfer and remote viewing capabilities
- Customize the system interface with themes and splash screens
- Document the configuration process for reproducibility and troubleshooting

---

## Hardware

- **Device:** Nintendo 3DS
- **Storage:** MicroSD storage for software libraries and homebrew applications

---

## Custom Firmware Environment

The system was configured using a custom firmware stack that enables system-level control and homebrew software execution.

**Boot Environment**
- **boot9strap (B9S)** – Bootloader enabling custom firmware
- **Luma3DS** – Custom firmware providing system patches and payload loading

**System Utilities**
- **GodMode9 (GM9)** – Low-level system file manager and NAND utility
- **FBI** – Title installer and package manager for `.cia` applications

---

## Software Packaging & Installation

### Game Boy Advance Injection
Game Boy Advance titles were converted to installable 3DS packages.

**Tool Used**
- **New Super Ultimate Injector for 3DS**

**Workflow**
1. Convert `.gba` ROMs to `.cia` packages
2. Install packages through FBI
3. Launch titles directly from the 3DS home menu using native GBA hardware support

---

### Nintendo DS Integration

Nintendo DS titles were implemented using:

- **`.nds` forwarders** for direct home menu launching
- **TWiLight Menu++** for managing and launching DS software
- **GBARunner2** for additional GBA compatibility within TWiLight

---

## Emulator Environment

Multiple emulators were configured to support additional retro platforms.

| Platform | Emulator |
|--------|--------|
| NES | VirtuaNES |
| SNES | Snes9x for 3DS |
| Sega Genesis | PicoDrive |
| Nintendo 64 | DaedalusX64 |
| Virtual Boy | Red Viper |
| Multi‑system / DS | TWiLight Menu++ |

Each emulator required configuration, compatibility testing, and performance tuning.

---

## Wireless File Transfer & System Management

The system supports wireless deployment and management of files.

**Tools Used**

- **ftpd** – Homebrew FTP server for wireless file transfer
- **WinSCP** – FTP client used to upload files to the device
- **FBI / GodMode9** – Local file management and installation

This setup allowed efficient deployment of software without removing the SD card.

---
```
PC
 │
 │ WinSCP / FTP
 ▼
3DS (ftpd server)
 │
 ├─ FBI → Install .cia packages
 ├─ Emulators
 ├─ TWiLight Menu++
 └─ BootNTR → NTRViewer (PC display)
```
---

## Remote Viewing / Streaming

The system was configured for **real‑time screen casting to a PC**.

**Tools Used**

- **BootNTR**
- **NTRViewer**

This configuration allows the 3DS screen output to be streamed to a computer for monitoring, recording, or demonstration purposes.

---

## Customization

The system interface was customized for usability and aesthetics.

**Customizations Implemented**

- Custom **boot splash screens**
- Custom **home menu themes**
- Organized home menu layout for multi-platform software access

---

## Workflow Summary

Typical process used when deploying software to the system:

1. Prepare software or ROM files
2. Convert compatible titles to `.cia` packages when necessary
3. Transfer files via FTP using WinSCP
4. Install packages through FBI
5. Configure emulator or forwarder
6. Test launch behavior and performance
7. Document compatibility and configuration steps

---

## Challenges & Solutions

**Challenge:** Managing multiple retro platforms within one device  
**Solution:** Integrated a combination of `.cia` injections, emulator environments, and forwarders.

**Challenge:** Efficient file management without removing SD storage  
**Solution:** Implemented FTP transfer with ftpd and WinSCP.

**Challenge:** Monitoring gameplay or debugging system behavior  
**Solution:** Configured BootNTR and NTRViewer for remote screen viewing.

---

## Skills Demonstrated

- Embedded system firmware modification
- Bootloader configuration and payload management
- Software packaging and installation workflows
- Wireless file transfer and remote device management
- Emulator configuration and compatibility testing
- Cross-platform troubleshooting
- Technical documentation and workflow design

---

## Future Improvements

- Automate ROM packaging and forwarder creation
- Expand emulator compatibility testing
- Document performance benchmarks for each emulator
- Add visual diagrams of the system architecture
