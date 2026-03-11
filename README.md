<div align="center">

# 🎮 C&C Generals Zero Hour Launcher

**مُشغّل احترافي | Professional Launcher**

![Version](https://img.shields.io/badge/Version-3.0.0-58a6ff?style=for-the-badge&logo=github)
![AutoHotkey](https://img.shields.io/badge/AutoHotkey-v2.0+-3fb950?style=for-the-badge&logo=autohotkey)
![Platform](https://img.shields.io/badge/Platform-Windows-0078d4?style=for-the-badge&logo=windows)
![License](https://img.shields.io/badge/License-Free-d29922?style=for-the-badge)

*A sleek, feature-rich launcher for Command & Conquer Generals: Zero Hour*

</div>

---

## ✨ Features

| Feature | Description |
|---|---|
| 🌐 **Generals Online** | Launch directly into Generals Online multiplayer |
| 🖥️ **Windowed Mode** | Run the game in a resizable window with auto GenTool activation |
| 🔧 **GenTool Manager** | Enable, disable, remove, or auto-download GenTool v8.9 |
| 🎨 **DXWrapper Support** | Fix black screen issues or reduce GPU load — two variants available |
| 🔍 **Smart Auto Detection** | Finds your game via Registry → Steam → Common Paths → Deep Scan |
| 🌙 **Dark / Light Theme** | Military Tactical dark theme + Desert Command light theme, or follow system |
| 🌐 **Arabic / English UI** | Full bilingual interface — switch at any time from inside the launcher |
| ⚡ **Admin Auto-Elevate** | Automatically requests admin rights on launch |
| 🔽 **System Tray Support** | Run in background, toggle tools, and restore window from tray |
| 📥 **Download Progress UI** | Real-time download progress window with percentage tracking |
| 🛡️ **File Integrity Checks** | Verifies file sizes and extraction success before applying changes |
| 🎖️ **Module Status Panel** | Live status cards for GenTool and DXWrapper (LOADED / STANDBY) |

---

## 📸 Preview

<div align="center">

![C&C Generals Zero Hour Launcher Preview](screenshot.png)

</div>

> The launcher features a professional military-tactical dark UI with a cinematic header, path banner, launch operation buttons, field tools section, and a live module status panel on the right.

**Dark Theme** — Military Tactical (deep olive/green palette)  
**Light Theme** — Desert Command (warm sand/khaki palette)

---

## 🚀 Getting Started

### Requirements
- Windows 10 / 11
- Command & Conquer Generals: Zero Hour (installed)

---

### ▶️ Option 1 — Run the EXE (Recommended)

No extra software needed. Just download and run.

1. Go to the [Releases page](../../releases)
2. Download `GeneralsLauncher.exe`
3. Run it directly — no installation required

---

### 🔧 Option 2 — Run from Source (AutoHotkey)

If you prefer to run the script directly:

1. Install [AutoHotkey v2.0+](https://www.autohotkey.com/)
2. Download or clone this repository
3. Double-click `GeneralsLauncher.ahk` to run it

---

### 📦 Option 3 — Compile AHK to EXE yourself

If you want to build your own `.exe` from the source script:

1. Install [AutoHotkey v2.0+](https://www.autohotkey.com/)
2. Open the **AutoHotkey Dash** (comes with AutoHotkey)
3. Click **Compile** → Open Ahk2Exe
4. Set `GeneralsLauncher.ahk` as the source file
5. Click **Convert** — your `.exe` will be generated

---

> The launcher will automatically search for your game installation on first run. If not found, it will prompt you to select the folder manually.

---

## 🎮 Launch Modes

### 🌐 Generals Online
Launches `GeneralsOnlineZH.exe` for online multiplayer. GenTool is automatically **disabled** before launch to ensure compatibility.

### 🖥️ Windowed Mode
Launches `Generals.exe -win` for offline skirmish or campaign. GenTool is **automatically enabled** (and downloaded if missing). Also launches `EdgeScroller.exe` if present.

---

## 🔧 Tools

### GenTool
Adds extra features to Zero Hour — required for Windowed Mode.

| Action | Description |
|---|---|
| **Enable** | Activates `d3d8.dll` in the game folder (renames `d3d8-.dll` → `d3d8.dll`) |
| **Disable** | Deactivates GenTool without deleting it (renames `d3d8.dll` → `d3d8-.dll`) |
| **Remove** | Permanently deletes both `d3d8.dll` and `d3d8-.dll` |
| **↓ Get** | Auto-downloads and installs GenTool v8.9 from ReizanTech GitHub |

### DXWrapper
Fixes display issues on modern GPUs. Two variants available:

| Variant | Use Case |
|---|---|
| 🎮 **GPU Fix — Black Screen** | Fixes black screen on launch with modern graphics cards |
| ⚡ **Reduce Settings** | Lowers GPU load for better performance |

> ⚠️ DXWrapper only works with **Generals Online** (`GeneralsOnlineZH.exe`), not the base `Generals.exe`

The launcher automatically detects which variant is installed by checking `dxwrapper.ini` file size and displays the correct type in the status panel.

---

## ⚙️ Configuration

Settings are saved automatically to `config.ini` in the launcher directory:

```ini
[Settings]
GamePath=C:\Games\Command and Conquer Generals Zero Hour
Language=en
Theme=auto
FirstRun=0
```

| Key | Values | Description |
|---|---|---|
| `GamePath` | folder path | Path to game directory containing `Generals.exe` |
| `Language` | `en` / `ar` | UI language |
| `Theme` | `auto` / `dark` / `light` | UI color theme |
| `FirstRun` | `0` / `1` | Whether this is the first launch |

---

## 🗂️ Game Search Priority

The launcher searches for your game automatically in this order:

1. **Windows Registry** — Checks EA / Origin install entries across multiple registry paths
2. **Steam** — Scans Steam library folders (auto-detected via registry or common paths)
3. **Common Paths** — Checks typical install locations (Program Files, Origin Games, R.G. Mechanics, etc.)
4. **Deep Search** — Recursively scans all drives up to 3 levels deep, skipping system/irrelevant folders

---

## 🎨 Theme System

| Theme | Description |
|---|---|
| 🔄 **Auto** | Follows Windows system dark/light mode setting |
| 🌙 **Dark** | Military Tactical — deep olive/green palette inspired by tactical HUDs |
| ☀️ **Light** | Desert Command — warm sand/khaki palette with army green accents |

Switch themes instantly from the language/theme controls inside the launcher. The theme is applied to the title bar, all controls, and dialogs.

---

## 🖥️ System Tray

The launcher minimizes to the system tray instead of closing. From the tray icon you can:

- **Double-click** to restore the main window
- Toggle **GenTool** on/off
- Toggle **DXWrapper** on/off
- Exit the application

---

## 💬 Support

Need help? Join the Discord support channel:

[![Discord](https://img.shields.io/badge/Discord-Support_Channel-5865f2?style=for-the-badge&logo=discord)](https://discord.com/channels/925092720538689536/1279438595190558853)

**Discord:** `reizanx`

---

## 👨‍💻 Author

Made with ❤️ by **ReizanTech**

---

<div align="center">

*Built with AutoHotkey v2 — Designed for the C&C community*

</div>
