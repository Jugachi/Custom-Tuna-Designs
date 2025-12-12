# 🎵 NeonMorph: A Reactive Tuna Theme

> **A shape-shifting, dark glassmorphism widget for OBS Studio & Tuna Plugin.**

[Preview of the Widget](https://github.com/user-attachments/assets/490b57b8-c5e4-4e26-9cbb-7008b882c08a)


**NeonMorph** is a high-performance HTML/CSS/JS overlay designed for the [OBS Tuna Plugin](https://github.com/univrsal/tuna). It features a reactive UI that morphs between a compact logo state and a full-width player upon song changes, complete with simulated neon-flicker typography and instant local file caching.

## ✨ Features

* **🔄 Morphing Transitions:** Seamlessly animates from a pill-shape to a circle and back when the song changes.
* **🌑 Dark Glassmorphism:** Modern frosted glass look with vibrant **#1DB954** neon accents.
* **⚡ Neon Typography:** "NOW PLAYING" sign with a realistic broken-neon flickering effect.
* **🚀 Instant Local Loading:** Bypasses network lag by reading cover art directly from your local disk.
* **📜 Smart Scrolling:** Auto-detects long titles and scrolls them only when necessary.
* **📏 Adaptive Layouts:** Includes a standard mode (with progress bar) and a "Compact Mode" (slim design).

---

## 🛠️ Prerequisites

1.  **OBS Studio** installed.
2.  **[Tuna Plugin](https://github.com/univrsal/tuna)** installed and running.
    * Ensure the **Web Server** is enabled in Tuna Settings (Port 1608).

---

## 📥 Installation

1.  **Download** this repository (or just the `.html` file and `logo.png`).
2.  Place all files into a permanent folder (e.g., `Documents/OBS-Assets/NeonMorph`).
3.  Add your own **logo** to this folder and name it `logo.png` (Recommended size: 200x200px, transparent background).

### 🎥 OBS Setup (Crucial!)

Since this widget uses centering animations, it needs to know the full canvas width.

1.  Add a **Browser Source** to your scene.
2.  **UNCHECK** the box "Local File" (This is important for parameters to work).
3.  In the **URL** field, enter the path to the file using the `file:///` protocol:
    ```text
    file:///C:/Users/YOUR_NAME/Documents/OBS-Assets/NeonMorph/tuna-widget.html
    ```
    *(Note: Use forward slashes `/`)*
4.  Set **Width** to `1920` (or your canvas width).
5.  Set **Height** to `400`.
6.  Delete everything in the "Custom CSS" field.

---

## ⚙️ Configuration

### 1. Compact Mode (No Progress Bar)
If you prefer a slimmer look without the timeline and progress bar, simply add `?nobar` to the end of the URL in OBS.

**URL Example:**
```text
file:///C:/.../tuna-widget.html?nobar
```
<img width="976" height="208" alt="Screenshot_20251212_193544" src="https://github.com/user-attachments/assets/221dec73-ab79-4ed6-bee4-7c2a2a5bd5d3" />


### 2. Local Cover Art (Zero Delay)
To ensure cover art appears instantly without waiting for Tuna to download it, place your album covers in the **same folder** as the HTML file.

**Naming Convention:**
* Start with `cover_`
* Replace spaces with underscores `_`
* Remove special characters (brackets, colons, `&`, `!`, etc.)
* File extension: `.png`

**Examples:**

| Album Name | File Name |
| :--- | :--- |
| `Thriller` | `cover_Thriller.png` |
| `Yokaze Nostalgia` | `cover_Yokaze_Nostalgia.png` |
| `Fly For Fun (FlyFF) [Lo-Fi]` | `cover_Fly_For_Fun_FlyFF_Lo-Fi.png` |

---

## 🎨 Customization

* **Logo:** Just replace `logo.png` in the folder with your own (keep the filename the same).
* **Colors:** Open the `.html` file in a text editor (like Notepad or VS Code) and search for `#1DB954`. Replace all occurrences of this Hex-Code to change the Spotify Green to your specific brand color.

---
