# 🐼 Elegoo CC1 — Printer / Filament / Process Profiles

This repo contains my personal, battle-tested configuration profiles for the **Elegoo Centauri Carbon**.  
Nothing here is theoretical. Every profile was printed, tuned, cursed at, and validated on my own machine.

The CC1 ships with hardened steel nozzles in 0.2 / 0.4 / 0.6 / 0.8,  
but only the 0.4mm nozzle currently has fully tuned profiles.  
The other folders are placeholders for future calibration sessions.

---

## 📁 Repo Structure

Printer Profile/  
Filament Profiles/  
Process Profiles/

Each folder is organized by nozzle size, but again:  
**0.4mm is the only one with real, tested data right now.**

Everything else is scaffolding, not lies.

---

## ⚠️ Important Note About Compatibility

All filament profiles in this repository are **tuned specifically for Elegoo-branded filaments**.  
These settings will *not* match other brands like Sunlu, Polymaker, Overture, Hatchbox, generic PLA, etc.

Elegoo filaments have their own:
- melt characteristics  
- pigment load  
- additives  
- cooling behavior  
- flow density  

Using these profiles on non-Elegoo filament may cause poor results.  
If you use another brand, you’ll need to calibrate your own temp, flow, and PA.

These profiles are **Elegoo-only by design**.

---

## 🎯 What’s Tuned Right Now

### ✔ Printer Profile (0.4mm)
My primary CC1 printer profile tuned for PLA on the stock 0.4mm hardened steel nozzle.

### ✔ Filament Profiles (0.4mm)
Includes multiple **Elegoo PLA colors and Elegoo specialty blends**:
- Marble-filled PLA  
- Wood-filled PLA  
- Bronze-filled PLA  
- Elegoo PLA color sets  

Each profile includes tuned:
- Temps  
- Flow (baseline 0.98)  
- Cooling  
- PA  
- Retraction  
- Realistic speed behavior  

### ✔ Process Profiles (0.4mm)
- 0.12mm Fine  
- 0.16mm Optimal  
- 0.20mm Standard  

These are my everyday workhorses — stable, balanced, and reliable.

---

## 🧪 How These Profiles Were Tuned

Calibration was done using:
- High-resolution **microscope inspection** (up to 54× magnification)  
- **AI-assisted surface and defect analysis**  
- Standard calibration tests (temp towers, flow plates, PA tests)

Microscope inspection was used for evaluating:
- Micro-banding  
- Layer fusion  
- Cooling quality  
- Edge sharpness  
- Surface texture consistency  

AI was used for:
- Flow irregularity detection  
- Layer transitions  
- Subtle extrusion shifts  
- Identifying artifacts invisible to the naked eye  

These profiles weren’t tuned by “feel.”  
They were tuned with gear, data, and the patience of someone who prints too damn much.

---

## 🛠 Why This Repo Exists

- Backup for all my CC1 configs  
- Easy synchronization across systems  
- A clean baseline for other CC1 users  
- A central place to upload future nozzle/material/process presets  

No fluff. No bloat. Just real printer settings.

---

## 🚧 Planned Additions

- 0.2mm / 0.6mm / 0.8mm profiles  
- Other Elegoo filament materials  
- More refined profiles based on additional testing  

---

## 📜 License

MIT License.  
Use it, modify it, sacrifice it to the filament gods.  
Just don’t blame me if your printer becomes self-aware.
