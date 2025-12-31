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

# 📥 How to Download Files from This Repository

This guide walks you through **three simple ways** to download files from this repo — whether you only need one file, the full project, or a stable release.

No GitHub experience required.  
No judgment. Just clear steps.

---

## 🔹 Option 1 — Download a Single File

Use this if you only need **one file**.

1. Click the file you want from the file list.
2. When the file opens, click **“Download raw file”** (usually near the top right).
3. The file will download directly to your computer.

✅ Best for:
- Single configuration files  
- Individual profiles  
- One-off assets  

---

## 🔹 Option 2 — Download the Entire Repository

Use this if you want **everything in one download**.

1. On the main repository page, click the green **`Code`** button.
2. Select **“Download ZIP”**.
3. Once downloaded, unzip the folder anywhere you like.

✅ Best for:
- Full setups  
- Browsing all files  
- Keeping everything organized  

---

## 🔹 Option 3 — Download a Release (Recommended)

Releases are packaged, tested versions of the project.

1. Click **“Releases”** on the right side of the repository page.
2. Select the most recent release.
3. Under **Assets**, download the `.zip` or `.tar.gz` file.
4. Extract the files like any normal archive.

✅ Best for:
- Stable versions  
- Plug-and-play use  
- Avoiding experimental changes  

---

## 🧠 Helpful Notes
- You do **not** need Git or special software to download files.
- If something doesn’t load right away, try refreshing the page.
- You can always return later to download updated versions.

---

## 💬 Need Help?
If something isn’t clear or you get stuck, that’s okay — everyone starts somewhere.  
Check the project notes or documentation for updates and guidance.

You’re good to import. 👍

---

## 🧩 How to Import Profiles into Elegoo Slicer / OrcaSlicer

Elegoo Slicer and OrcaSlicer handle profile imports **the same way**, so these steps apply to both.

You can import **single files** or **entire ZIP packages** — no unpacking required unless you want to.

---

## 🔹 Step-by-Step Import Instructions

1. Open your slicer (Elegoo Slicer or OrcaSlicer).

2. In the top menu, click:
   **File → Import → Configs**

3. Browse to the file you downloaded.

4. Select the file and click **Open**.

That’s it — the profile will now appear in your available presets.

---

## 📦 Supported File Types

You can import any of the following:

- `.json`  
- `.zip`  
- `.elegoo_printer`  
- `.elegoo_filament`  

You can also import an **entire ZIP archive** without extracting it first.  
The slicer will automatically detect and load all supported profiles inside.

---

## ✅ After Importing

Once imported, you can:
- Select the profile from the dropdown menus  
- Adjust values if needed  
- Save changes under your own custom name  

Nothing is overwritten unless you choose to overwrite it.

---

## 🧠 Helpful Tip

If you don’t see the profile immediately:
- Restart the slicer  
- Or switch nozzle sizes and switch back  

Some slicers refresh profile lists only after a UI refresh.

---

## 💬 Need Help?

If something doesn’t load correctly, don’t stress — it’s usually a simple fix.  
Check the repo notes or documentation for updates and clarifications.

You’re good to go. 🚀****

---

## 📜 License

MIT License.  
Use it, modify it, sacrifice it to the filament gods.  
Just don’t blame me if your printer becomes self-aware.  

---

*If this helped you, a star is always appreciated.*

