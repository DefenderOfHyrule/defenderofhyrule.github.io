# **Alternative methods to update your modchip's firmware**

### **Information**

This page solely exists for people with already-modchipped Switch consoles. It's not necessary to follow if your modchip installation is working fine as is and could potentially introduce more issues if your modchip installation is experiencing errors or similar.

That said, I do recommend updating your modchip's firmware to the latest firmware version to get the best possible performance, reliability and hardware compatibility.

-----

### **Updating your Picofly modchip firmware via `Modchip Toolbox`:**

1. Download `modchip_toolbox.bin` and `update.bin` from the links below:

    - [Modchip Toolbox](https://github.com/DefenderOfHyrule/modchip-toolbox/releases) (`modchip_toolbox.bin`)
    - [usk](https://github.com/DefenderOfHyrule/usk/releases) (`update.bin`)

1. Place `update.bin` on the root of your SD card.

1. Place `modchip_toolbox.bin` in `sd:/bootloader/payloads`.

1. Boot into hekate and go to `Payloads` > `modchip_toolbox.bin`.

1. Navigate to `Picofly Options...` underneath the `Picofly` section.

1. Press `Info` underneath the `Firmware` section to see the information about the firmware version you're running. Press any key (the Volume or Power buttons) to return to the previous menu.
    - If it's running version `2.82`, you're already up to date and do not need to update.
    - **Note:** *Some* Picofly modchips come pre-flashed with a fork of the spacecraft-nx firmware for hwfly modchips (the `NO SD` screen with the interactive rocket when you turn the Switch on without SD card inserted). You should *not* use this firmware as it is unstable and can cause things like Android/Linux to not boot at all (if relevant to your situation), slow boot times and it can potentially shorten the lifespan of your modchip. *If* you have this firmware version, the `Info` menu will report `No valid picofly descriptor found. Signature: 0x00000000 (expected 0x9cabe959)` which means that you should update your modchip's firmware.

1. Select `Update (update.bin)` in the `Firmware` section, press A or power and wait for it to finish updating the modchip's firmware from `update.bin` located on the root of your SD card. (This shouldn't take more than 1-2 seconds.)

    - **Note:** Updating `sdloader` is not necessary for Picofly modchips as updating its firmware automatically updates `sdloader` as well.

1. Power the console off by navigating to `Back` under the `Return` section and selecting `Power off`, then turn it back on.

    - Glitching and training may take a little longer the first time after flashing but should be fast again afterwards.

    - **Optional:** Verifying if the firmware update was successful can be done by booting into `modchip_toolbox.bin` (in hekate going to `Payloads` > `modchip_toolbox.bin`) and selecting `Picofly Options...` > `Info` again. It should now display the version number as `2.82`.

-----

### **Updating your Hwfly/SX Series modchip firmware via `Modchip Toolbox`:**

!!! note "Note"

    This section assumes that you've previously flashed the SX series modchip with `hwfly-nx`. If you haven't done so yet, see the bottom of [this page](../modchip/flashing_modchip.md#instructions_1) to physically flash your modchip by opening up the console. Only do this if you're comfortable with doing so.

1. Download `modchip_toolbox.bin` and `release_072.zip` from the links below:

    - [Modchip Toolbox](https://github.com/DefenderOfHyrule/modchip-toolbox/releases) (`modchip_toolbox.bin`)
    - [hwfly-firmware](https://github.com/hwfly-nx/firmware/releases/download/0.7.2/release_072.zip)

1. Extract the downloaded `release_072.zip` file somewhere.
    
1. Place `modchip_toolbox.bin` in `sd:/bootloader/payloads`.

1. Place `sdloader.enc` from the `.zip` file on the root of your SD card.

1. Hold `Volume Up` and boot into hekate, then go to `Payloads` > `modchip_toolbox.bin`. You can let go of volume up once you're in `Modchip Toolbox`.

    - Holding `Volume Up` while turning on the console "activates" the modchip. This allows `Modchip Toolbox` to interact with the modchip and therefore also allow you to update its firmware.

1. Navigate to `HWFLY Options...` underneath the `HWFLY` section.

1. Select `Update` underneath the `SD Loader` section once in `Modchip Toolbox`.

    - This will update the `sdloader` module that the modchip uses to "inject" (load) any payload named `payload.bin` from the root of your SD card.

1. Power the console off by navigating to `Back` under the `Return` section and selecting `Power off`.

    - You can delete `sdloader.enc` from the root of your SD now.

1. Place `firmware.bin` from the `.zip` file on the root of your SD card.

1. Hold `Volume Up` and boot into hekate, then go to `Payloads` > `modchip_toolbox.bin`. You can let go of volume up once you're in `Modchip Toolbox` once again.

1. Select `Update` underneath the `Firmware` section to update the modchip's firmware.

1. Power the console off by pressing any key and selecting `Power off`, then turn it back on.

    - Glitching and training may take a little longer the first time after flashing but should be fast again afterwards.
