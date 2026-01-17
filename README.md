# PixelDevVic Client (1.19.2)

**PixelDevVic Client** is a private, lightweight utility mod built for **Minecraft Forge 1.19.2**. It provides advanced "Quality of Life" survival features designed for stealth and safety on standard SMPs, Realms, and friends' servers.

> **Created by:** [PixelDev-Vic](https://github.com/PixelDev-Vic)  
> **Status:** Client-Side Only (No Server OP Required)

---

## ⚡ Features

### 💎 Stealth Ore ESP
A highly optimized scanner that draws clean tracers and boxes around valuable blocks.
* **Stealth Rendering:** Uses "SeeThrough" text rendering (Action Bar style logic) so names are visible through walls but blend in like vanilla nametags.
* **Smart Filtering:** Cycle through target lists to reduce screen clutter.
    * *Modes:* All, Diamond, Iron, Gold, Ancient Debris, Emerald.
* **Performance:** Uses `Matrix4f` rendering for zero-jitter, ensuring boxes stick perfectly to blocks even while moving fast.

### ⛏️ Safe Fast Break
A server-safe implementation of instant mining that avoids "Ghost Blocks."
* **Zero Delay:** Removes the hardcoded 5-tick cooldown between breaking blocks.
* **Legit Haste:** Automatically applies **Haste V (Amplifier 4)**. This mimics the speed of a maxed-out Beacon + Efficiency V, making it mathematically "possible" in vanilla, which prevents anti-cheats from autobanning you.

### 🛡️ Combat & Survival Utilities
* **AutoTotem:** Automatically moves a Totem of Undying from your inventory to your offhand if it is empty.
* **AutoTool:** Instantly switches your hotbar slot to the best tool for the block you are mining.
* **AutoEat:** Detects low hunger (< 8 shanks) and automatically eats food from your hotbar without stopping your movement.
* **NoFall:** Spoofs ground packets to prevent fall damage.
* **Flight:** Enables creative-mode flight in survival.

### 👻 Flash Notification System
Designed specifically for screen-sharing safety.
* **Action Bar Only:** Toggles appear briefly above the hotbar.
* **No Chat Logs:** Toggles are **never** saved to chat history. If you press `T`, the log is empty.
* **Flash Mode:** Notifications linger for only **0.75 seconds** before being force-cleared, making them nearly impossible to catch during a casual screen glance.

---

## 🎮 Controls & Keybinds

| Key | Feature | Description |
| :--- | :--- | :--- |
| **F** | **Flight** | Toggle Creative Flight. |
| **G** | **ESP Toggle** | Turn the Ore Scanner On/Off. |
| **H** | **ESP Filter** | Cycle ore targets (Diamond -> Iron -> Gold -> Debris -> etc). |
| **Y** | **AutoEat** | Toggle automatic eating. |
| **U** | **FastBreak** | Toggle "Safe" Fast Mine (Haste V + 0 Delay). |
| **I** | **AutoTool** | Toggle automatic tool switching. |
| **O** | **AutoTotem** | Toggle automatic offhand totem replacement. |

---

## 🛠️ Installation Guide

1.  **Prerequisites:**
    * Install [Minecraft Forge 1.19.2](https://files.minecraftforge.net/net/minecraftforge/forge/index_1.19.2.html).

2.  **Building the Mod:**
    * Clone this repository or download the source.
    * Open a terminal in the project folder.
    * Run: `gradlew build` (Windows) or `./gradlew build` (Linux/Mac).
    * The compiled mod file will appear in `build/libs/`.

3.  **Installing:**
    * Move the `pixeldevvic-1.0.jar` into your `.minecraft/mods` folder.
    * Launch Minecraft using the Forge profile.

---

## ⚠️ Disclaimer

This project is intended for **educational purposes** and for use on servers where you have permission (e.g., Anarchy servers, private SMPs).

* **Use at your own risk.** While features like "Safe Fast Break" and "Flash Notifications" are designed to avoid detection, aggressive server-side anti-cheats may still flag packet anomalies.
* The author is not responsible for any bans or account restrictions resulting from the use of this software.
