### **Information**

This page solely exists for people with already-modchipped Switch consoles. It's not necessary to follow if your modchip installation is working fine as is and could potentially introduce more issues if your modchip installation is experiencing errors or similar.

That being said, I do recommend updating your modchip's firmware to the latest firmware version to get the best possible performance, reliability and hardware compatibility.

-----

### **Updating your Picofly modchip firmware via `picofly toolbox`:**

1. Download `picofly_toolbox_0.2.bin` and `update.bin` from the links below:

    - [Picofly toolbox](../modchip/firmware/picofly_toolbox_0.2.bin)
    - <a href="https://github.com/DefenderOfHyrule/usk/releases/tag/2.75">Firmware 2.75</a> (download `update.bin`)

2. Place `update.bin` on the root of your SD card.

3. Place `picofly_toolbox_0.2.bin` in `sd:/bootloader/payloads`.

4. Boot into hekate and go to `Payloads` > `picofly_toolbox_0.2.bin`.

5. Press `Info` underneath the `Firmware` section to see the information about the firmware version you're running. Press any key (the Volume or Power buttons) to return to the previous menu.
    - If it's running version `2.75`, you're already up to date and do not need to update.
    - **Note:** *Some* Picofly modchips come pre-flashed with a fork of the spacecraft-nx firmware for hwfly modchips (the `NO SD` screen with the interactive rocket when you turn the Switch on without SD card inserted). You should *not* use this firmware as it is unstable and can cause things like Android/Linux to not boot at all (if relevant to your situation), slow boot times and it can potentially shorten the lifespan of your modchip. *If* you have this firmware version, the `Info` menu will not report a firmware version and will only show `Reading firmware info...` and this means that you should update your modchip's firmware.

6. Select `Update` in the `Firmware` section and wait for it to finish updating the modchip's firmware from `update.bin` located on the root of your SD card. (This shouldn't take more than 1-2 seconds.)

    - **Note:** Updating `sdloader` is not necessary for Picofly modchips as updating its firmware automatically updates `sdloader` as well.

7. Power the console off by pressing any key and selecting `Power off`, then turn it back on.

    - Glitching and training may take a little longer the first time after flashing but should be fast again afterwards.

8. Verifying if the firmware update was successful can be done by booting into `picofly toolbox` (in hekate going to `Payloads` > `picofly_toolbox_0.2.bin`) and selecting `Info` again. It should now display the version number as `2.75`.

-----

### **Updating your Hwfly/SX Series modchip firmware via `hwfly toolbox`:**

!!! note "Note"

    This section assumes that you've previously flashed the SX series modchip with `hwfly-nx`. If you haven't done so yet, see the bottom of [this page](../modchip/flashing_modchip.md#instructions_1) to physically flash your modchip by opening up the console. Only do this if you're comfortable with doing so.

1. Download `hwfly_toolbox.bin` and `release_072.zip` from the link below:

    - <a href="https://github.com/DefenderOfHyrule/hwfly-firmware/releases/tag/0.7.2">https://github.com/DefenderOfHyrule/hwfly-firmware/releases/tag/0.7.2</a>

2. Place `hwfly_toolbox.bin` in `sd:/bootloader/payloads`.

3. Place `sdloader.enc` from the `.zip` file on the root of your SD card.

4. Hold `Volume Up` and boot into hekate, then go to `Payloads` > `hwfly_toolbox.bin`, you can let go of volume up once in `hwfly toolbox`.

    - Holding `Volume Up` while turning on the console "activates" the modchip. This allows `hwfly toolbox` to interact with the modchip and therefore also allow you to update its firmware.

5. Select `Update` underneath the `SD Loader` section once in `hwfly toolbox`.

    - This will update the `sdloader` module that the modchip uses to "inject" (load) any payload named `payload.bin` from the root of your SD card.

6. Power off the console or reboot into hekate (by pressing any key and selecting `Power off` or `Back to hekate`) and delete `sdloader.enc` from the root of your SD.

7. Place `firmware.bin` from the `.zip` file on the root of your SD card.

8. Hold `Volume Up` and boot into hekate, then go to `Payloads` > `hwfly_toolbox.bin`, you can let go of volume up once you're in `hwfly toolbox` once again.

9. Select `Update` underneath the `Firmware` section to update the modchip's firmware.

10. Power the console off by pressing any key and selecting `Power off`, then turn it back on.

    - Glitching and training may take a little longer the first time after flashing but should be fast again afterwards.
