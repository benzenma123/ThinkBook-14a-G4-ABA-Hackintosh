# 💻 ThinkBook 14 G4+ | Ryzen 7 5825U Hackintosh
> **Target OS:** macOS Tahoe v26 (Early Alpha/Dev)
> **Status:** Fully Optimized & Cracked 🚀

---

##  OS Info
| Component | Details |
| :--- | :--- |
| **Tested Version** | **macOS Tahoe v26 (26Axxxx)** |
| **Bootloader** | OpenCore 1.0.x |
| **System Model** | MacBookPro16,3 (Recommended) |

---

## ✅ What's Working (The "Goated" Part)
* **Graphics:** Full acceleration (Metal) via `NootedRed`. 144Hz refresh rate is buttery smooth.
* **CPU:** 8 Cores / 16 Threads fully recognized (Cezanne 5825U).
* **Display:** Brightness control & high-resolution HiDPI scaling.
* **Multitasking:** Absolute beast mode. No lag under heavy workloads.
* **Audio:** Internal speakers & Combo Jack (via AppleALC + OCLP Rollback).
* **Thermal:** Ice cold. Stays frosty thanks to proper power management.
* **Touchpad:** Precision tracking with native multi-touch gestures (GPIO Interrupt).

---

## 🛠 Troubleshooting Log (The Battle History)

### 1. GPU Panics & Browser Freezes
* **Issue:** System would hard-freeze or show artifacts when using Chrome/Chromium-based browsers.
* **Cause:** Incompatible hardware acceleration calls in early Tahoe builds for AMD iGPU.
* **Fix:** Switched to **Firefox**. Configured `WebRender` in `about:config` to stabilize rendering.

### 2. The Silent Audio (AppleHDA Rollback)
* **Issue:** Audio was completely dead due to new framework changes in Tahoe.
* **Obstacle:** `AppleALC` alone wasn't enough; required a specific **AppleHDA Rollback**.
* **Solution:** Used **OpenCore Legacy Patcher (OCLP) 3.0.0 Nightly** to perform a Root Patch.
* **Layout ID:** Settled on `alcid=11` for the Realtek ALC257 codec.

### 3. Thermal & Power Issues (Polling vs. Interrupt)
* **Issue:** Laptop was running hot because the touchpad was stuck using `vi2c-force-polling`.
* **Fix:** Removed the `force-polling` boot-arg. Switched to **GPIO Interrupt Mode**. 
* **Result:** CPU overhead dropped significantly; the aluminum chassis is back to being ice cold.

---

## 📸 Screenshots
*(Replace these placeholders with your actual screenshots)*

| Desktop | Audio/Graphics Info | Thermal/CPU Load |
| :---: | :---: | :---: |
| ![Desktop](https://github.com/user-attachments/assets/5dab264b-e432-4698-92b1-c4d4c555895c) | ![About](https://github.com/user-attachments/assets/27b3c99e-20b4-4760-babb-676c2bc7ca34) | ![Activity](https://github.com/user-attachments/assets/a76ff542-75c6-473b-b16f-a150c8a05a3f) |

---

## 🙏 Credits
* [Acidanthera](https://github.com/acidanthera) for OpenCore, Lilu, and AppleALC.
* [NootInc](https://github.com/NootInc) for **NootedRed** (AMD iGPU support).
* [Dortania](https://github.com/dortania) for the OpenCore Legacy Patcher.

---

## 👨‍💻 Author
**Ben**
*Frontend & Backend Developer*
*Currently building **BenOS** from scratch.*
