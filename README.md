# PIForge Sound Alarm Pro — Pro Edition

> One symbol, three thresholds, instant visual and audio escalation

[![Website](https://img.shields.io/badge/Website-piforge.pages.dev-0078d4?style=for-the-badge)](https://piforge.pages.dev)
[![Purchase](https://img.shields.io/badge/Purchase-Buy_Pro_Version-27ae60?style=for-the-badge)](https://piforge.pages.dev/product.html?id=3)

---

## Technical Showcase & Demo

Here is a live demonstration of **PIForge Sound Alarm Pro** running in AVEVA PI Vision:

<p align="center">
  <img src="gif-pf-levels.gif" alt="Sound Alarm Pro Demo" width="100%" style="border-radius: 16px; box-shadow: 0 8px 30px rgba(0,0,0,0.15);" />
</p>

---

## Key Features & Live Demos

Every capability is demonstrated live in AVEVA PI Vision.

### 1. Three-Level Alarm — Critical, Major, Warning
**One symbol, three thresholds, instant visual and audio escalation**

As your process value rises through L1 Warning, L2 Major, and L3 Critical thresholds, the Sound Alarm symbol escalates automatically — changing background color, triggering the corresponding alert sound, and holding the alarm until acknowledged.

- L1 Warning (yellow), L2 Major (orange), L3 Critical (red) — configurable colors
- Background and border change instantly at each threshold crossing
- Each level plays its own sound — 10 built-in options per level
- Priority cascade: L3 always overrides L2, L2 overrides L1

<p align="center">
  <img src="gif-pf-levels.gif" alt="Three-Level Alarm — Critical, Major, Warning" width="100%" style="border-radius: 16px; box-shadow: 0 8px 30px rgba(0,0,0,0.15);" />
</p>

---

### 2. Flexible Alarm Conditions — High, Low, Exact, Range
**Not just 'greater than' — configure the exact condition your process needs**

High-value alarms are the default, but real processes need more. Configure the Sound Alarm for low-value conditions, exact-match states, or any comparison operator. Enable or disable the entire alarm without removing the symbol from your display.

- Operators: > (High), < (Low), =, >=, <= — covers every alarm condition
- Enable/Disable toggle: silence without deleting — perfect for maintenance windows
- Blink effect: pulsing animation draws attention on busy control room displays
- Show/hide label and value independently for clean or detailed layouts

<p align="center">
  <img src="gif-pf-general.gif" alt="Flexible Alarm Conditions — High, Low, Exact, Range" width="100%" style="border-radius: 16px; box-shadow: 0 8px 30px rgba(0,0,0,0.15);" />
</p>

---

### 3. Your Alarm Colors, Your Brand
**Customize every color — normal state, each alarm level, text**

Standard red/yellow/green doesn't fit every control room. Map your plant's color standards to each alarm level. Changes apply instantly on the symbol, no page reload required.

- Per-level alert color: override the default red/orange/yellow to match your standard
- Normal background: transparent, dark, or any solid color for any display theme
- Text color: high contrast on any background
- Live preview: color changes reflect immediately in the symbol

<p align="center">
  <img src="gif-pf-colors.gif" alt="Your Alarm Colors, Your Brand" width="100%" style="border-radius: 16px; box-shadow: 0 8px 30px rgba(0,0,0,0.15);" />
</p>

---


## Installation Guide

Setting up **PIForge Sound Alarm Pro** is quick and straightforward. Follow these steps:

### 1. Deploy Files to PI Vision Server
Extract the downloaded ZIP package. You will find HTML, JS, CSS/SVG, and image files. Copy these files to your PI Vision server's extension folder:
```cmd
%PIHOME%\Scripts\app\editor\symbols\ext
```
*Typically, this path translates to:*
```cmd
C:\Program Files\PIPC\PIVision\Scripts\app\editor\symbols\ext
```

### 2. Unblock Windows Files (Critical)
Windows blocks downloaded files by default. If you skip this step, the symbol will silently fail to load in PI Vision.
1. Right-click the `.js` and `.html` files you copied on the server.
2. Select **Properties** from the context menu.
3. On the **General** tab, look for the security warning at the bottom: *This file came from another computer and might be blocked to help protect this computer.*
4. Check the **Unblock** box, then click **Apply** and **OK**.
5. Repeat this for all files in the package.

### 3. License Key Activation
1. Log in to your PIForge Dashboard and go to **My Licenses** to copy your License Key (format: `XXXX-XXXX-XXXX-XXXX`).
2. Open PI Vision, add the symbol to a display.
3. Click the **Format Symbol (⚙)** configuration panel.
4. Paste your key into the **License Key** field and click **Activate**.

---

## Compatibility Reference

In PI Vision, go to **Help → About** to verify your version number.

| PI Vision Version | Sound Alarm Pro Support | Notes |
| --- | --- | --- |
| **2022+** | Full Support | Recommended |
| **2021** | Full Support | |
| **2020** | Full Support | |
| **2019** | Partial Support | Some features may be limited |
| **2018 or older** | Not Supported | |

---

## Troubleshooting & Support

### Symbol does not appear in the PI Vision palette
* Verify the files are copied to the correct `ext` directory on the **PI Vision server** (not your local machine).
* Perform a hard browser refresh: `Ctrl + Shift + R`.
* Ensure all files are unblocked (see step 2 of the Installation Guide).

### Symbol loads but displays blank or shows error
* Open Browser DevTools (`F12`) and check the **Console** tab for red errors.
* Verify the license key has no extra spaces.
* Try restarting IIS on the PI Vision server. Run this command in an Administrator command prompt:
  ```cmd
  iisreset
  ```

### Need Support?
* If you run into issues, copy your license key and contact us at **contact.piforge@gmail.com** for assistance.

---

👉 **[Purchase and Download the Pro Version at piforge.pages.dev](https://piforge.pages.dev/product.html?id=3)**

*PIForge is not affiliated with AVEVA Group plc or OSIsoft LLC.*
