<div align="center">

# 🎧 Spotify Taskbar Widget

**Control Spotify, display live synchronized lyrics, and Shazam any audio right from your desktop—using only ~8MB of RAM.**

[Overview](#-overview) • [Features](#-features) • [Installation](#-installation) • [Shortcuts & Controls](#%EF%B8%8F-shortcuts--controls) • [FAQ](#-faq)

<br>

</div>

---

## 🌟 Overview

Tired of alt-tabbing out of your game or workflow just to skip a song, check the lyrics, or see what's playing? **Spotify Taskbar Widget** is a native, ultra-lightweight desktop mini-player designed to stay seamlessly visible without cluttering your screen or eating your memory.

| Metric | Standard Desktop Apps (Electron) | **Spotify Taskbar Widget** |
| :--- | :--- | :--- |
| **Memory (RAM)** | ~150 MB – 400 MB | **~8 MB** 🚀 |
| **Controls** | Fixed window, heavy UI | **Instant compact modes (`Alt + N`) & Collapsible buttons** |
| **Physics & Feel** | Static dragging | **60 FPS Momentum throw physics & edge bounce** |
| **Extras** | Playback only | **Live Synced Lyrics, Loopback Shazam & Volume Wheel** |

---

## ✨ Features

- **🪶 Featherlight Memory Footprint (~8 MB RAM):** Built with pure native Python & Qt—zero Chromium or Electron bloat. Unused memory pages are continuously released via Windows kernel working set trimming.
- **🎵 Live Synchronized Lyrics:** Click the **Menu (•••)** button to open the dark obsidian glass lyrics viewer. Features authentic Spotify deep navy aesthetics, smooth auto-scrolling, and glowing active line highlights synchronized to the music.
- **🎯 60 FPS Momentum Physics:** Drag and throw the player across the screen with fluid momentum physics. It gently bounces off display borders and remembers its exact release position.
- **🎛️ Dual-Stage Compact Mode (`Alt + N`):**
  - Press **Alt + N** anywhere (even inside games) to shrink into a compact player with playback buttons on the left and album art on the right.
  - **Collapsible Controls Arrow (❮ / ❯):** Click the subtle chevron arrow to slide the media buttons away into an ultra-discrete `58 × 58` circular album art badge, and click it again to slide them back!
- **🎙️ Zero-Footprint Shazam Recognition:** Hear a song in a YouTube video, game, Twitch stream, or Discord call? Click the blue **Shazam (S)** button. It captures internal loopback audio for 3.5 seconds and scrolls the identified title/artist directly across the widget without opening popups—then frees 100% of its memory.
- **⏱️ Live Timeline Seek & Hover Tooltip:** Hover anywhere along the bottom progress bar to preview exact timestamps (`mm:ss / mm:ss`) in 60 FPS and click to seek playback instantly.
- **🌈 Dynamic Album Accent Colors:** Automatically samples dominant colors from the current album art with 0ms lag, dynamically tinting the seek bar, glow rim, and UI highlights.
- **🔊 Volume Wheel & HUD Feedback:** Scroll your mouse wheel anywhere over the widget or click the `-` / `+` buttons to adjust Spotify volume in 5% increments with an on-screen toast.
- **🎮 Topmost Lock (Over Games & Fullscreen):** Enforced via Win32 `SetWindowPos` to ensure uninterrupted visibility over borderless fullscreen games, browsers, and creative software.
- **👻 Ghost / Transparency Mode:** Toggle semi-transparency with a single click to blend the widget seamlessly into your wallpaper or taskbar.

---

## 📸 Screenshots

<div align="center">
  <table>
    <tr>
      <td align="center"><b>Transparent Mode</b></td>
    </tr>
    <tr>
      <td><img src="png.webp" width="400"/></td>
    </tr>
  </table>
</div>

---

## 🚀 Installation

1. Navigate to the [**Releases**](https://github.com) page and download the latest zip.
2. Extract and run `Setup.bat` (or use `Baslat.vbs` to start silently in the background).
3. Play music on Spotify Desktop and press **`Alt + N`** anytime to shrink or expand the bar!

---

## ⌨️ Shortcuts & Controls

| Shortcut / Button | Action |
| :--- | :--- |
| <kbd>Alt</kbd> + <kbd>N</kbd> | Shrink to Compact Player / Expand Full Bar (Global hotkey) |
| **Left Click + Drag & Throw** | **60 FPS Momentum Physics Glide** |
| **••• (Menu Button)** | Open Live Synchronized Lyrics Viewer |
| **S (Shazam Button)** | Identify Any Music Playing on Your Screen (Loopback) |
| **Progress Bar Hover** | Live Time Preview Tooltip (`mm:ss / mm:ss`) & Seek |
| **Compact ❮ / ❯ Arrow** | Smoothly hide/show media controls in compact mode |
| **Mouse Wheel / `-` `+`** | Adjust Spotify Volume (5% steps) with HUD Toast |
| **◐ Button** | Toggle Ghost / Transparency Mode |
| **– Button** | Collapse / Compact Mode |
| **✕ Button** | Quit Application Completely |

---

## ❓ FAQ

<details>
<summary><b>Does it require Spotify Premium or API tokens?</b></summary>
<br>
<b>No!</b> This widget interacts directly with the native Windows Media Transport Controls (SMTC) session. It requires <b>no logins, no API developer keys, and works with both Spotify Free and Spotify Premium</b> accounts out of the box.
</details>

<details>
<summary><b>How does it use only ~8MB of RAM?</b></summary>
<br>
Unlike Electron-based mini players that bundle entire Chromium web browsers, this widget is built natively using lightweight Qt widgets. Shazam AI libraries run strictly inside a temporary subprocess that is destroyed after 3.5 seconds, and Windows kernel APIs periodically trim idle memory pages.
</details>

<details>
<summary><b>Does it work while playing games in fullscreen?</b></summary>
<br>
Yes! The player uses native Windows <code>SetWindowPos(HWND_TOPMOST)</code> enforcement, allowing it to stay floating smoothly over borderless windowed games, movies, and fullscreen software.
</details>

---

## 🤝 Contributing & Support

If you enjoy this widget, please consider giving it a ⭐ on GitHub!  
Found a bug or have a suggestion? Feel free to open an [**Issue**](https://github.com/issues).

<div align="center">
  <sub>Licensed under the <a href="LICENSE">MIT License</a>.</sub>
</div>
