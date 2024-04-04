---
hide:
  - navigation
  - toc
---

### **The Installation**

This page will guide you through the modchip installation process on "OLED" model Switch consoles. Everything you need will be listed and pictures of what your solder joints should look like will be posted by each step.
Specific steps such as photos of the screws you need to unscrew aren't mentioned here as they can be found on guides from iFixit (for example). It's expected for you to know what to unscrew.

#### Diode reading values

These values can differ from console to console. If your modchip installation works fine and doesn't match these exact values, it's not an issue. These values can act as "indicators" about what you might expect. Especially the `C` (DAT0) point can have a large range of acceptable values.

| Positive to ground     | Negative to ground     |
| ---------------------- | ---------------------- |
| **SP1**  `~0.420`      | **SP1**  `~0.520`      |
| **SP2**  `~0.25`       | **SP2**  `~0.20`       |
| **A**    `~0.470`      | **A**    `~0.875`      |
| **B**    `~0.405`      | **B**    `OL`          |
| **C**    `~0,435`      | **C**    `~0.500-0.850`|
| **D**    `~0.440`      | **D**    `~0.880`      |
| **3.3v** `~0.445`      | **3.3v** `~0.850`      |

#### Requirements:

- A soldering iron with a small(er) tip (preferably temperature controlled that can reach 350C consistently)
- Flux (preferably halogen free flux)
- Good quality 30-32 awg wire (such as Kynar wire, other wire can work as long as it's single core)
- Thermal paste (preferably non-conductive)
- Isopropyl Alcohol (preferably 95-99% IPA)
- Your modchip (including the SoC ribbon cable and DAT0 adapter)
- Kapton tape (optional, but recommended)
- A dental pick or other thin and sharp tool (to scrape away the top layer of the PCB for the B point)
- Toothpicks/Q-tips (to remove the thermal paste between the capacitors on the SoC)
- Soldering tin (leaded is recommended, unleaded will work depending on your skill level)
- A fume extractor (for your own health and safety)
- A microscope (optional but recommended)

??? note "Note for stock RP2040 Zero development board users"
     If you use a stock `RP2040 Zero` development board, you will need to desolder the USB-C port,`BOOT` and `RESET` buttons before continuing. You'll also need to purchase the SoC ribbon cable separately together with 5x `0805 47Ω +-1%` resistors (5x is recommended, 3x is possible in some instances).
     The resistors can be purchased on AliExpress or websites like Digikey or Mouser Electronics. The SoC ribbon cable can be purchased from AliExpress.

#### Instructions:

1. Unscrew the Switch's backplate.

2. Remove the metal shield/cover (be careful with the antennas that are routed across the metal shield/cover).

3. Remove the Gamecard reader/SD card reader board.

4. Remove the heatpipe/heatsink.

5. Remove the IHS (Internal Heat Spreader) to expose the bare SoC die and RAM chips.

6. Remove and clean up the thermal paste on the SoC die and around/in-between the capacitors on the SoC using IPA.
       - You can also clean off the thermal paste between the IHS and heatpipe/heatsink in the meantime, the red-ish colored thermal goop between the heatpipe/heatsink and metal shield/cover can be left alone.

7. Remove the fan and unplug the fan ribbon cable, joycon rail ribbon cables, screen ribbon cable and speaker connectors.

8. Unscrew and remove the bottom bar of the shell.

9. Remove the motherboard from the Switch casing.

10. Remove the metal plate covering the eMMC chip on the back of the motherboard.

11. Turn the motherboard back around and scrape away the B point on the motherboard using a thin and sharp metal tool.
