# 📷 Chip Design of Penta Linear Array Charge Couple Device (CCD)

## Overview

This repository presents the **layout, schematic design, and simulation of a Charge-Coupled Device (CCD) chip**, focusing on the architecture and optimization of a linear five-array CCD using Cadence Virtuoso.

---

## 🏗️ Device Architecture

- **CCD Structure:**  
  - Five linear arrays, each with 6000 pixels and distinct sections: imaging area, bias, storage, transfer, two-phase Horizontal Shift Register (HSR), and output.
  - Each array includes anti-blooming regions to prevent charge spillover, and four readouts per array for robust charge-to-voltage conversion and amplification.
  - The full chip integrates 280 pads and 20 readouts, with metal routing subfields for clock and output signals.

- **Pixel Layout:**  
  - Each pixel: 16 × 16 μm.
  - Pixel block includes photodiode, transfer, storage, bias, anti-blooming, and two-phase HSR (87 μm vertical dimension).
  - Layout designed and optimized in **Cadence Virtuoso**.

- **Routing & Assembly:**  
  - Metal routing for clock and output signals is optimized to minimize crosstalk and resistance.
  - The chip (108,000 × 12,000 μm) is divided into subfields for manufacturability and stitched during lithography.
  - Strategic pad placement ensures efficient interfacing and minimal parasitic effects.

---

## 💻 Tools & Technologies

- **EDA:** Cadence Virtuoso (schematic, layout, simulation)
- **DRC:** Calibre
---

## 🧩 Design Flow

1. **Pixel Schematic & Layout:**  
   - Electrical and physical design of the pixel, ensuring correct resistance and capacitance.
2. **Full Array Schematic:**  
   - Integration of all pixels, considering PCB and packaging effects.
3. **Simulation:**  
   - Analysis of timing (rise/fall, delay), signal integrity, and optimization of RC paths.
4. **Optimization:**  
   - Metal strapping on polysilicon reduces resistance, improving timing and charge transfer.
5. **Design Rule Check (DRC):**  
   - Calibre used to ensure layout compliance with foundry rules; corrections made as needed.
6. **GDS File Generation:**  
   - Final layout exported for fabrication.

---

## 📊 Key Results

- **Optimized RC Paths:**  
  - Metal strapping and layout iterations significantly reduced rise/fall times and delays.
- **Design Compliance:**  
  - All DRC violations resolved, layout ready for fabrication.
- **Full System Integration:**  
  - Complete chip assembly with robust routing and pad placement.

