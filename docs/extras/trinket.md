### **Information**

This page will be about the installation of `SAMD21` based modchips for Unpatched Switch consoles only. These modchips allow you to inject any payload on boot and essentially achieve the same result as voltage glitching based modchips, without the voltage glitching part. As I mentioned before, these *only* work on Unpatched Switch consoles and simply won't work on Patched consoles. These modchips do not rely on voltage glitching and simply allow you to cold boot a payload using `fusee-gelee` in `RCM`.

- Cold booting means being able to boot into a payload from a fully-off state.

-----

### **SAMD21**

`SAMD21` is a series of microcontrollers (like the `RP2040` used in Picofly modchips) that have a *lot* of purposes and many different applications. These applications can range from Switch modchips to factory equipment (as an example) and are very useful.

With this guide, we will be focusing on a `SAMD21` based modchip called `RCM x86`, it's a pretty commonly available `SAMD21` based modchip and is also the most "modchip"-like out of them all (in my opinion).
The documentation for these types of modchips can be found [here](https://gbatemp.net/threads/internal-modchip-samd21-trinket-m0-gemma-m0-itsybitsy-m0-express-guide-files-support.508068/). The soldering for these types of modchips is also *much* easier and straightforward compared to voltage glitching based modchips.

