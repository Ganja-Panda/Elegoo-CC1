# Elegoo Centauri Carbon – Start G-Code Guide  
### (Cold Wipe • Optional Heated Mesh • Hot Wipe Workflow)

This README explains the **custom Start G-Code** included in this profile and how to properly run the **one-time heated mesh calibration** so the printer stores a correct mesh for your bed plate and bed temperature.

---

# 🧩 When You MUST Run the One-Time Heated Mesh  
You only need to perform Stage 2 (Heated Mesh) when:

- first time you import the profile,
- you change to a **different build plate**,  
- you change **bed temperature significantly**, or  
- you **reset/clear** the stored mesh.

If you already have a correct Z-offset and the mesh matches your plate & temp, you **do NOT** need to run Stage 2 again.

---

# 🔥 One-Time Heated Mesh Instructions

1. **Remove the leading `;` on the Stage 2 lines** in the Start G-Code block (the 5 lines under “Stage 2”).  
2. **Start any small print** (a throwaway cube is fine).  
   The printer will:
   - heat the bed to your 1st-layer temp,  
   - heat the nozzle to **140°C**,  
   - home, and  
   - run `BED_MESH_CALIBRATE` at print temperature.  
3. After the mesh is saved automatically:
   - **Re-comment the Stage 2 lines** (add `;` back).  
   - You’re done — **you don’t run Stage 2 every print**.

---

# 🧠 Why This Order Matters

### **Stage 1: Cold Wipe @ 140°C**
- Cleans the nozzle without burning filament onto it.

### **Stage 2 (Optional): Mesh at Print Temp**
- Ensures the mesh matches the thermal expansion of your plate.

### **Stage 3: Heat to Full Print Temp**
- Avoids long idle periods at high temps (reduces heat creep).

### **Stage 4: Hot Wipe**
- Final purge & clean right before printing.

Only *after* all of this should the slicer start the fans and the actual print moves.

---

# 🧾 Full Start G-Code Block  
**This is already included in the profile put here for quick reference** 
`Printer Settings → Machine G-code → Start G-code`

```gcode
;===== date: 20240520 =====================
;printer_model:{printer_model}
;initial_filament:{filament_type[initial_extruder]}
;curr_bed_type:{curr_bed_type}

M400 ; wait for buffer to clear
M220 S100 ;Set the feed speed to 100%
M221 S100 ;Set the flow rate to 100%
G90 ;absolute positioning

;===== Stage 1: Cold wipe at ~140°C =====================
M140 S[bed_temperature_initial_layer_single] ;start heating bed (no wait)
M104 S140 ;preheat nozzle to 140°C
G28 ;home XYZ
M729 ;wipe nozzle at 140°C

;===== Stage 2: Get Bed Mesh at Print Temp  =====================
; Remove leading ; to activate these 5 lines for a one-time heated mesh.
;M190 S[bed_temperature_initial_layer_single] ; Wait for bed
;M104 S140 ; Set nozzle temp 140c
;M109 S140 ; Wait for Nozzle 
;G28 ; Home All
;BED_MESH_CALIBRATE ; Get bed mesh at print bed temp

;===== Stage 3: Heat to Full Temperature =====================
M190 S[bed_temperature_initial_layer_single] ;wait for bed
M104 S[nozzle_temperature_initial_layer] ;set nozzle for 1st layer
M109 S[nozzle_temperature_initial_layer] ;wait for nozzle

;===== Stage 4: Hot wipe / purge =====================
M729 ;wipe nozzle at print temp.

;=============turn on fans to prevent PLA jamming=================
