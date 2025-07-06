# KyberStand

WLED Config for D1 Mini – Lightsaber and Kyber Crystal Display Stand

This repository contains the WLED configuration and preset files for the **KyberStand** — a Star Wars-inspired LED lightsaber display stand featuring custom kyber crystal holders and a glowing Jedi Order crest.

It uses a D1 Mini and 32 WS2812B LEDs to bring each crystal to life with individual colors and animations, plus a dynamic Jedi crest effect — perfect for collectors, diorama builders, or any Star Wars fan looking for a glowing centerpiece.

---

## 📁 Included Files

- `wled_KyberStand_presets.json`  
  Custom WLED presets including:
  - 7 individually addressed kyber crystal LEDs with unique color themes
  - A 25-LED Jedi Order diffuser with animated effects
  - Organized into segments for precise control and customization

- `wled_D1Mini_KyberStand_Config`  
  Full WLED configuration including:
  - GPIO settings
  - Segment layout
  - LED count (32)
  - Preset behavior and brightness settings

---

## 💎 Kyber Crystals (3D Printable)

The stand features 7 kyber crystal holders, each backlit by its own LED. If you don’t have official Galaxy’s Edge kybers, you can print your own.

### Print Specs:

- Print **vertically** for best clarity
- Enable **pause at 9mm layer height** for a filament swap:
  - Start with **black filament**
  - Switch to **white or translucent** to simulate a glowing kyber core
- The **Black Kyber** is printed entirely in black
- After printing, apply a **thin brushed coat of clear UV resin** to the outside:
  - Adds a smooth, glossy, glass-like finish
  - Greatly enhances the feel and light diffusion

---

## 💡 LED Layout

The KyberStand uses a single WS2812B LED strip, cut and bridged with ~30mm wires to match physical spacing.

- **7 Kyber Crystal LEDs**:
  - 🔵 Blue
  - 🟢 Green
  - 🟡 Yellow
  - ⚪ White
  - 🟣 Purple
  - 🔴 Red
  - 🟥 "Black" — simulated with pulsing red and flashing white to mimic an unstable crystal

- **25 Jedi Crest LEDs**:
  - Positioned beneath a diffused Jedi Order symbol
  - Animates with a **blue and green alternating chase pattern**

Total LEDs: **32**

---

## ⚙️ Power & Wiring

To avoid overloading the D1 Mini’s regulator, a direct power tap is used from the USB cable.

### 🔌 Wiring Method

1. Use a 2-wire USB power cable (no data lines)
2. Strip and twist:
   - USB **+5V** wire + **LED strip +5V**
   - USB **GND** wire + **LED strip GND**
3. Tin the twisted pairs and solder to:
   - `5V` pin on the D1 Mini
   - `GND` pin on the D1 Mini
4. Connect LED **Data In** to `D4` (GPIO 2) on the D1 Mini

This ensures the LED strip and D1 Mini are powered together without routing current through the onboard regulator.

---

## 🧪 Setup Instructions

1. Flash WLED (v0.14 recommended) to your D1 Mini via [install.wled.me](https://install.wled.me)
2. Connect to the WLED web UI
3. Upload presets:
   - Go to **Presets → Edit JSON**
   - Paste contents of `wled_KyberStand_presets.json`
4. *(Optional)* Restore config:
   - Go to **Config → Security & Updates → Backup & Restore**
   - Upload `wled_D1Mini_KyberStand_Config`

---

## 🛠 Build Tips

- Diffuse the Jedi crest using translucent PLA or a thin diffuser film
- Use frosted filament or clear resin domes over each kyber LED
- Customize preset transitions or segment layouts easily through the WLED web interface

---

## 🌌 Inspired By...

The power of kyber, the legacy of lightsabers, and the artistry of Star Wars collectors. This stand honors the Jedi Order and the Light Side of the Force — and displays your saber collection in style.

---

> **Crafted in Galactic Style ✨**  
> By ASTDrones – [MakerWorld Profile](https://makerworld.com/en/@pumpkin20303) | [GitHub](https://github.com/astdrones) | [eBay Store](https://www.ebay.com.au/usr/astdrones_3d)
