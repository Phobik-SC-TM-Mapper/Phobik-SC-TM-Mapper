<div align="center">

# Phobik SC-TM Mapper

**A Thrustmaster HOTAS configurator for Star Citizen.**

Map your sticks and throttle to Star Citizen commands, auto-generate and run a Thrustmaster TARGET script, and print a reference sheet — all from one app.

[![Latest Release](https://img.shields.io/github/v/release/Phobik-SC-TM-Mapper/Phobik-SC-TM-Mapper?label=download&style=for-the-badge)](../../releases/latest)
![Platform](https://img.shields.io/badge/platform-Windows%2011-blue?style=for-the-badge)

*by Land Hard Games*

</div>

---

## Overview

Phobik SC-TM Mapper turns the tedious job of binding a Thrustmaster HOTAS to *Star Citizen* into a guided, visual workflow. Browse the game's commands, assign them to your physical buttons and axes (or let the app auto-assign keyboard shortcuts for you), organize everything into profiles, then generate and run a complete Thrustmaster **TARGET** script — no hand-editing `.tmc` files required. When you're done, export a printable PDF reference sheet of your layout.

This repository hosts the **official downloads**. The application ships as a checksum-verified MSI installer and a portable ZIP.

## Features

- **Visual device mapping** — assign Star Citizen actions to buttons, axes, hats, and shift layers across multiple Thrustmaster devices (dual sticks + throttle supported).
- **Interactive 3D Device Workshop** — inspect your hardware in a 3D viewport and see each control's assignment per layer at a glance.
- **Command browser** — search the full Star Citizen action set, filtered by game branch (LIVE / PTU / EPTU).
- - **6-layer IOUMD mapping** — an In/Out shift combined with an Up/Middle/Down mode gives each control up to 6 distinct commands (12 with TEMPO short/long-press), turning the dual Sol-R sticks into hundreds of possible bindings across all six layers.
- **Automatic keyboard-shortcut binding** — auto-assign commands to keyboard shortcuts from a managed pool, **while preserving Star Citizen's default key bindings** so you can still fall back to keyboard-and-mouse play without conflicts.
- **Automatic TARGET script generation** — the app builds a complete, valid `.tmc` TARGET script from your mappings and **runs it for you, directly in the app** — no need to open the TARGET editor.
- **Built-in script editor** — review or fine-tune the generated TARGET script with syntax highlighting.
- **PDF mapping reference charts** — generate a printable reference sheet of your bindings with device schematic callouts, with an in-app preview before you export.
- **Profiles** — create, clone, import, export, and switch between multiple loadouts for different ships and play styles, with automatic backups.
- **Star Citizen integration** — auto-detects your install and active branch and imports the game's default bindings as a baseline.
- **Live device testing & diagnostics** — verify inputs and troubleshoot device detection in real time.
- **Built-in updater** — checks for new releases and installs them with SHA-256 verification.

## System Requirements

- Windows 11 (21H2 or later), 64-bit
- A **Star Citizen** installation (LIVE, PTU, or EPTU)
- A **Thrustmaster TARGET-supported device** — HOTAS stick(s) and/or throttle
- [Thrustmaster TARGET software](https://support.thrustmaster.com/) installed (used to detect devices and run generated scripts)
- ~300 MB free disk space

## Installation

Grab the latest build from the [**Releases**](../../releases/latest) page.

### MSI Installer (recommended)

1. Download `Phobik-SC-TM-Mapper-<version>.msi`.
2. Run it and follow the prompts.

> **Note:** the installer is currently unsigned, so Windows SmartScreen may warn you.
> Click **More info → Run anyway** to proceed.

### Portable

1. Download `Phobik-SC-TM-Mapper-v<version>-portable.zip`.
2. Extract it anywhere and run the executable. No installation required.

### Verifying your download

Each release includes `SHA256SUMS.txt`. To confirm your download is intact:

```powershell
Get-FileHash .\Phobik-SC-TM-Mapper-<version>.msi -Algorithm SHA256
```

Compare the output against the matching line in `SHA256SUMS.txt`.

## Getting Started

1. Launch Phobik SC-TM Mapper and let it detect your Thrustmaster devices and Star Citizen install.
2. Pick or create a **profile**.
3. Assign Star Citizen actions to your controls in the mapping views — or use automatic keyboard-shortcut binding to fill them in.
4. **Generate** — the app automatically builds the TARGET script and **runs it for you inside the app** (you do not need to open TARGET yourself).
5. **Load your bindings in Star Citizen** — open the game's keybinding settings and load your control profile. *Star Citizen does not load it automatically.*
6. Fly.

> Tip: generate a **PDF reference chart** for your profile and keep it handy while you learn a new layout.

## Updating

The app checks for updates on startup (toggle this in **Settings → Updates**). You can also check manually from the same screen. Updates download and install as SHA-256-verified MSI packages.

## Troubleshooting

- **SmartScreen warning on install** — expected for an unsigned build; choose *More info → Run anyway*.
- **Devices not detected** — make sure Thrustmaster TARGET is installed and your HOTAS is connected before launching.
- **Bindings not working in-game** — confirm you
- (1) ran the generated script from the app, and wait for script status to show green running this couuld take 60s for Bad Driver State Start
- (2) Run Star Citizen AFTER Script is Running,
- (3) loaded your control profile in Star Citizen's keybinding settings,
- (4) Last Resort for wrong Windows Joy ID is delete "/user/client/0/Profiles/default/actionmaps.xml" and then restart the script before running Star Citizen to force the Game to refresh device order(you will have to reload the controls in game from XML again.

## Support

Found a bug or have a request? Please open an [issue](../../issues).

## Disclaimer

This is an unofficial, community tool. It is not affiliated with, endorsed by, or associated with Cloud Imperium Games (*Star Citizen*) or Guillemot Corporation (*Thrustmaster / TARGET*). All trademarks belong to their respective owners.

---

<div align="center">
© Land Hard Games
</div>
