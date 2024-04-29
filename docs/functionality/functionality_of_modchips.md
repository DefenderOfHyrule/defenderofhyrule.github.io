### **Information**

This page will cover the functionality of modchips, it will tell you about how they work and why they work.

### **General knowledge**

Unlike "unpatched" consoles (V1 unpatched consoles), modchips enable the ability to run CFW via CPU voltage glitching, which bypass bootROM firmware verifications. It allows `payload.bin` to be launched in place of running `BOOT0` (the first partition on your Switch's internal storage that uses Nintendo's official bootloader) normally, loaded via a modchip firmware module named `sdloader`. This is much different from RCM and its exploit, fusee-gelee, which "unpatched" consoles use. Modchips allow any Switch console (like all "patched" consoles) to run CFW.

-----

### **The `sdloader` firmware module**

`sdloader` is the module built into the Picofly firmware (and all other modchip firmwares) which is responsible for "injecting" (loading) `payload.bin` off of the root of your SD card. It will always run if the modchip installation is successful.

-----

### **Voltage glitching**

Voltage glitching essentially "lags out" the Switch's CPU by injecting too much voltage and timing out the CPU for a very short amount of time, allowing you to bypass bootROM firmware verification and the "injection" of a custom payload (in this case, `payload.bin`) from the root of your SD card in the newly created time window by voltage glitching. Voltage glitching is commonly used to interrupt the boot process of several other consoles and computers in general as well and is an effective "attack" in regards to console hacking.

-----

### **Training**

The modchip will do something called "training" once successful glitch timings have been found. Training is the process of "stress testing" the glitch timings the modchip found, glitch timings are the aforementioned time windows the modchip creates to "inject" `payload.bin`. Several glitch timing entries are written to the modchip's "internal storage" and are used for quick boot times. If one of the glitch timings changes or is updated by performing a Switch firmware update, the modchip will attempt to glitch and run `sdloader` with the rest of the remaining glitch timings. If glitching or training fails, resetting the modchip may be necessary (requiring you to open up the console and accessing the modchip manually). Picofly will typically never fail glitching and training unless hardware issues are present.

-----

### **The modchip's payload**

The modchip, after glitching and training, will write its payload to an empty sector on the `BOOT0` partition of your Switch's internal storage. This payload is responsible for making your Switch boot up to the Picofly splash screen (the `No SD Card` splash screen with the Picofly logo) and stops the Switch from booting normally (unless `sdloader` is bypassed by holding both volume buttons and powering on the console). This payload is not dangerous and does not mess with any important aspect of the Switch's internal storage.
