# 🎵 NeonMorph: A Reactive Tuna Theme

> **A shape-shifting, dark glassmorphism widget for OBS Studio & Tuna Plugin.**

[Preview of the Widget](https://github.com/user-attachments/assets/490b57b8-c5e4-4e26-9cbb-7008b882c08a)

**NeonMorph** is a high-performance HTML/CSS/JS overlay designed for the [OBS Tuna Plugin](https://github.com/univrsal/tuna). It features a reactive UI that morphs between a compact logo state and a full-width player upon song changes, complete with simulated neon-flicker typography and multiple data-source options.

## ✨ Features

* **🔄 Morphing Transitions:** Seamlessly animates from a pill-shape to a circle and back when the song changes.
* **🌑 Dark Glassmorphism:** Modern frosted glass look with vibrant **#1DB954** neon accents.
* **🤖 Firebot Integration:** Support for "On-Demand" display using Firebot commands and URL hash triggers.
* **📺 YouTube Music Support:** Directly pulls high-quality cover art URLs from the Tuna web server.
* **⚡ Neon Typography:** "NOW PLAYING" sign with a realistic broken-neon flickering effect.
* **🖼️ Smart Placeholders:** Immediately shows your logo or a vinyl record icon while transitioning to new cover art.
* **📜 Smart Scrolling:** Auto-detects long titles and scrolls them only when necessary.
* **✨ Smooth Animations:** Features a fade-in effect when the actual album cover is retrieved to prevent jarring transitions.

---

## 🛠️ Prerequisites

1.  **OBS Studio** installed.
2.  **[Tuna Plugin](https://github.com/univrsal/tuna)** installed and running.
    * Ensure the **Web Server** is enabled in Tuna Settings (**Port 1608**).
3.  **(Optional) [Firebot](https://firebot.app/)** for on-demand chat triggers.

---

## ⚙️ Configuration (URL Parameters)

Customize the widget by appending parameters to the URL in your OBS Browser Source:

| Parameter | Description |
| :--- | :--- |
| `?ws` or `?youtube` | **Recommended for YouTube Music.** Pulls cover art via web URL. |
| `?local` | Reads cover art from your local disk (see Naming Convention below). |
| `?nobar` | Removes the progress bar and time stamps for a cleaner look. |
| `?firebot` | **On-Demand Mode.** The widget stays hidden until triggered. |
| `?debug` | Displays a green status overlay for troubleshooting connections. |

---

## 📥 Installation & Setup

### 🎥 OBS Setup
1.  Add a **Browser Source** to your scene.
2.  **UNCHECK** the box "Local File" (Necessary for parameters to work).
3.  In the **URL** field, enter the path using the `file:///` protocol:
    ```text
    file:///your/path/to/neon-morph-player.html?ws&firebot
    ```
4.  Set **Width** to `1920` and **Height** to `400`.

### 🔥 Firebot Trigger Setup (Optional)
If you are using `?firebot` mode, the widget will only appear when signaled.
1.  Create a command (e.g., `!song`).
2.  Add the effect **OBS: Set Browser Source Url**.
3.  Set the URL to your file path and append `#$unixTimestamp` at the end:
    ```text
    file:///your/path/to/neon-morph-player.html?ws&firebot#$unixTimestamp
    ```
    *This ensures the URL changes every time, triggering the 15-second animation.*

---

## 🖼️ Cover Art Logic

The widget uses a prioritized loading sequence to ensure no "broken" images:
1.  **Immediate:** Displays `logo.png` (or a vinyl record icon if the logo is missing).
2.  **2-Second Delay:** Smoothly fades from the placeholder into the actual album art from your chosen source (`?ws` or `?local`).

### Local Naming Convention (only with `?local`)
Place `.png` files in the widget folder named: `cover_Album_Name.png` (replace spaces with underscores).

---

## 🎨 Customization

* **Logo:** Replace `logo.png` in the folder with your own (200x200px recommended).
* **Colors:** Edit the `.html` file and replace `#1DB954` with your preferred brand color.
* **Language:** The widget is fully localized to **English**. The initial state displays "Fetching information...".

---