# Hackintosh EFI – Intel i3-3210 & GT 710 (Monterey)
💻 OpenCore EFI for running **macOS Monterey** on an **Intel i3-3210 & GT 710** system.  

> 🚧 **Work in Progress** – This guide is still being updated as testing progresses.

---

## Project Status
| **macOS Version** | **Status** |
|------------------|-----------|
| macOS Monterey (`12.x`) | ✅ Stable |

---

## Hardware Compatibility
This EFI is designed for the following configuration:  

### System Specifications
| **Component** | **Details** |
|-------------|------------|
| **Motherboard** | ASUS P8H61-M LX R2.0 |
| **CPU** | Intel Core i3-3210 (Ivy Bridge) |
| **GPU** | NVIDIA GeForce GT 710 (Kepler) |
| **RAM** | 8GB DDR3 1333MHz |
| **Storage** | SATA SSD/HDD |
| **Wi-Fi & Bluetooth** | No built-in support (requires compatible USB adapter) |
| **Audio** | Realtek ALC887 |
| **SMBIOS** | MacPro6,1 |

---

## Limitations ⚠️
- ❌ **No Metal Support** – GT 710 is Kepler-based but lacks full Metal acceleration in macOS Monterey.
- ❌ **No AirDrop & Continuity** – Requires a native macOS-supported Wi-Fi/Bluetooth adapter.
- ⚠️ **Requires SMBIOS Tweaks** – Ensure proper configuration for iMessage, App Store, and FaceTime.

---

## What Works ✅
- ✅ **Graphics Acceleration (via OCLP)**
- ✅ **Audio (ALC887 with AppleALC)**
- ✅ **USB (Properly mapped)**
- ✅ **Ethernet (Realtek RTL8111)**
- ✅ **Sleep/Wake**
- ✅ **Basic macOS Functionality**

---

## Known Issues 🚨
- ❌ **No native Wi-Fi & Bluetooth**
- ❌ **No DRM support for Apple TV+ and Netflix in Safari**
- ❌ **Might require boot args tuning for stability**

---

## Installation Guide 🛠️
### **BIOS Settings**
Ensure the following settings are configured in your BIOS:
- **VT-d** → Disabled  
- **Secure Boot** → Disabled  
- **CSM (Legacy Boot Mode)** → Disabled  
- **Serial Port** → Disabled  
- **Above 4G Decoding** → Enabled (if available)  

### **Steps to Install**
1. **Prepare a macOS Monterey USB Installer** using OpenCore.
2. **Mount the EFI partition** of your USB.
3. **Copy the EFI folder** from this repository to your USB's EFI partition.
4. **Boot into OpenCore** and install macOS Monterey.
5. **Post-Install Tweaks** – Use OpenCore Post-Install (OCLP) for better GPU acceleration.

---

### **☕ Support Me on Ko-fi**
<script type='text/javascript' src='https://storage.ko-fi.com/cdn/widget/Widget_2.js'></script>
<script type='text/javascript'>kofiwidget2.init('Support me on Ko-fi', '#72a4f2', 'J3J612PNM4');kofiwidget2.draw();</script>

---

## Credits 🙌
- [Acidanthera](https://github.com/acidanthera) for OpenCore, Lilu, AppleALC, WhateverGreen.
- [Dortania’s OpenCore Guide](https://dortania.github.io/OpenCore-Install-Guide/) for documentation.
- Hackintosh communities for testing and feedback.

---

### 📜 Disclaimer  
⚠️ **This EFI is provided as-is.** I am not responsible for any issues that may arise from using this setup. Proceed at your own risk.
