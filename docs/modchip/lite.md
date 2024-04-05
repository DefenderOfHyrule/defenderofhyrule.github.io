---
hide:
  - navigation
  - toc
---

### **The Installation**

This page will guide you through the modchip installation process on "Lite" model Switch consoles. Everything you need will be listed and pictures of what your solder joints should look like will be posted by each step.
Specific steps such as photos of the screws you need to unscrew aren't mentioned here as they can be found on guides from iFixit (for example). It's expected for you to know what to unscrew.

#### Diode reading values

These values can differ from console to console. If your modchip installation works fine and doesn't match these exact values, it's not an issue. These values can act as "indicators" about what you might expect.

| Positive to ground        | Negative to ground           |
| ------------------------- | ---------------------------- |
| **SP1** `~0.125`          | **SP1** `~0.125`             |
| **SP2** `~0.12`           | **SP2** `~0.10`              |
| **A** (CMD) `~0.470`      | **A** (CMD) `~0.875`         |
| **B** (RST) `~0.405`      | **B** (RST) `OL`             |
| **C** (DAT0) `~0.435`     | **C** (DAT0) `~0.500-0.850`  |
| **D** (CLK) `~0.440`      | **D** (CLK) `~0.880`         |
| **3.3v** `~0.445`         | **3.3v** `~0.850`            |

#### Requirements:

- A soldering iron with a small(er) tip (preferably temperature controlled that can reach 350C consistently)
- Flux (preferably halogen free flux)
- Good quality 30-32 awg wire (such as Kynar wire, other wire can work as long as it's single core)
- Thermal paste (preferably non-conductive)
- Isopropyl Alcohol (preferably 95-99% IPA)
- Your modchip (including the SoC ribbon cable)
- Kapton tape (optional, but recommended)
- Toothpicks/Q-tips (to remove the thermal paste between the capacitors on the SoC)
- Soldering tin (leaded is recommended, unleaded will work depending on your skill level)
- Double sided tape
- A fume extractor (for your own health and safety)
- A microscope (optional but recommended)
- UV Solder mask (optional but recommended)

??? note "Note for stock RP2040 Zero development board users"
     If you use a stock `RP2040 Zero` development board, you will need to desolder the USB-C port,`BOOT` and `RESET` buttons before continuing. You'll also need to purchase the SoC ribbon cable separately together with 5x `0805 47Ω +-1%` resistors (5x is recommended, 3x is possible in some instances).
     The resistors can be purchased on AliExpress or websites like Digikey or Mouser Electronics. The SoC ribbon cable can be purchased from AliExpress.

#### Instructions:

1. Unscrew the Switch's backplate.

2. Remove the metal shield/cover.

3. Remove the heatpipe/heatsink.

4. Remove the IHS (Internal Heat Spreader) to expose the bare SoC die and RAM chips.

5. Remove and clean up the thermal paste on the SoC die and around/in-between the capacitors on the SoC using IPA.
       - You can also clean off the thermal paste between the IHS and heatpipe/heatsink in the meantime, the red-ish colored thermal goop between the heatpipe/heatsink and metal shield/cover can be left alone.

6. Apply flux and pre-tin the pads labeled `SP1` and `SP2` on the SoC ribbon cable.

7. Place the SoC ribbon cable and align the ribbon cable with the capacitors on the SoC.

8. Tuck the anker points underneath the metal frame below the SoC and the MOSFET section of the ribbon cable underneath the frame between the SoC and RAM, then solder the ribbon cable down once lined up correctly.

9. Apply flux and use your soldering iron to heat up the end of each capacitor together with the respective pad next to both ends of each capacitor of the `SP1` and `SP2` points, ensure the solder flows between the pad on the ribbon cable and end of the capacitor.

10. Your ribbon cable should now be secured in place with both ends of each capacitor soldered to the pads on the ribbon cable.
       - Optional: Place Kapton tape across your solder joints to prevent thermal paste from potentially corroding your solder joints in the future. It also helps in cases where you might have to rework your solder joints.

