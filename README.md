# 🎨 OBS Tuna Themes Collection

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![OBS Studio](https://img.shields.io/badge/OBS-Studio-blue.svg)](https://obsproject.com/)
[![Tuna Plugin](https://img.shields.io/badge/Plugin-Tuna-orange.svg)](https://github.com/univrsal/tuna)

**A community-driven collection of custom HTML/CSS/JS themes for the [OBS Tuna Plugin](https://github.com/univrsal/tuna).**

This repository serves as a hub for streamers and designers to share their custom "Now Playing" overlays. From simple minimalist bars to complex, reactive, and animated widgets—find the perfect look for your stream here.

---

## 📂 Available Themes

| Preview | Theme Name | Description | Author |
| :---: | :--- | :--- | :--- |
| <img width="976" height="208" alt="Screenshot_20251212_193544" src="https://github.com/user-attachments/assets/b4724dc2-5130-482e-822f-188244436ef3" /> | **[NeonMorph](./NeonMorph)** | A dark glassmorphism widget that morphs shapes on song change. Includes neon effects and local caching. | Jugachi |
| *Place screenshot here* | *Next Theme* | *Description coming soon...* | *You?* |

> *Click on the **Theme Name** to navigate to the specific folder and installation instructions.*

---

## 🛠️ Prerequisites

To use any of these themes, you need:

1.  **[OBS Studio](https://obsproject.com/)**
2.  **[Tuna Plugin](https://github.com/univrsal/tuna)** installed.
3.  **Enable the Web Server** in Tuna:
    * Go to `Tools` -> `Tuna Settings` -> `Web`.
    * Check **Enable Web Server**.
    * Default Port: `1608`.

---

## 🚀 General Installation

While each theme might have specific settings (check the `README.md` inside the theme folder), the general setup is:

1.  **Download** this repository (or just the folder of the theme you want).
2.  Open **OBS Studio**.
3.  Add a **Browser Source**.
4.  Point the URL to the `index.html` (or `theme.html`) file of the chosen theme.
    * *Tip:* Some themes require disabling "Local File" and using the `file:///path/to/file.html` method to support parameters.
5.  Set the **Width** and **Height** as recommended by the theme creator.

---

## 🤝 How to Contribute

Got a cool design? We'd love to see it! To add your theme to this collection:

1.  **Fork** this repository.
2.  **Create a new folder** with your theme name (e.g., `My-Cool-Theme`).
3.  **Add your files:**
    * Your HTML/CSS/JS files.
    * Any assets (images, fonts).
    * A `preview.gif` or `screenshot.png` so people can see what it looks like.
    * A concise `README.md` inside your folder explaining how to use/configure it.
4.  **Update the Main README:**
    * Add a row to the [Available Themes](#-available-themes) table above pointing to your folder.
5.  **Submit a Pull Request!**

### Contribution Guidelines
* **License:** By contributing, you agree that your code allows others to use and modify it (MIT License).
* **Clean Code:** Try to keep your code readable.
* **No External Dependencies:** If possible, avoid linking to external CDNs for essential functionality (images/fonts should be local) to ensure the theme works offline.

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files, to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software.
