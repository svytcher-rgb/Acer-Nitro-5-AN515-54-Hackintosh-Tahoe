# Acer Nitro 5 AN515-54 Hackintosh — macOS Tahoe

OpenCore EFI for **Acer Nitro 5 AN515-54-52LB** running **macOS Tahoe 26.0**.

## Hardware

- Laptop: Acer Nitro 5 AN515-54-52LB
- CPU: Intel Core i5-9300H
- iGPU: Intel UHD Graphics 630
- dGPU: NVIDIA GeForce GTX 1650 — disabled in macOS
- Wi-Fi: Intel AX200
- Audio: Realtek ALC255
- Ethernet: Realtek RTL8111
- Storage: NVMe SSD

## Tested macOS

- macOS Tahoe 26.0
- Build: 25A354

## OpenCore

OpenCore version reported by NVRAM:

`REL-108-2026-08-12`

## What works

- macOS boot
- Intel UHD 630 graphics acceleration
- Internal keyboard
- Wi-Fi using itlwm
- Ethernet
- Audio
- Battery status
- Brightness control
- NVMe storage
- USB

## Known issues

- NVIDIA GTX 1650 is not supported by macOS and is disabled
- Sleep may not work correctly on all configurations
- Wi-Fi requires itlwm / HeliPort depending on configuration
- Some Apple services may require valid SMBIOS data

## SMBIOS

The SMBIOS data included in this repository is intentionally invalid.

Before using this EFI, generate your own:

- MLB
- SystemSerialNumber
- SystemUUID
- ROM

Do **not** use the placeholder values included in `config.plist`.

## BIOS settings

Recommended settings:

- UEFI boot
- Secure Boot: Disabled
- SATA Mode: AHCI
- Fast Boot: Disabled if boot issues occur

## Installation

1. Download or clone this repository.
2. Copy the `EFI` contents to your EFI System Partition.
3. Generate your own SMBIOS.
4. Check BIOS settings.
5. Reset NVRAM from the OpenCore picker after major config changes.
6. Boot macOS.

## Important

This EFI was created specifically for the Acer Nitro 5 AN515-54-52LB.

Other AN515-54 variants may use different:

- Wi-Fi cards
- audio codecs
- displays
- touchpads
- storage controllers

Use at your own risk.

## Credits

- Acidanthera / OpenCore
- Dortania OpenCore Install Guide
- Lilu
- WhateverGreen
- VirtualSMC
- AppleALC
- itlwm
- VoodooI2C
- VoodooPS2
- USBToolBox
