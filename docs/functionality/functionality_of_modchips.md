### **Information**

This page will cover the functionality of modchips, it will tell you about how they work and why they work.

### **General knowledge**

Unlike "unpatched" consoles (V1 unpatched), modchips enable the ability to run CFW via CPU voltage glitching, which bypasses bootROM firmware verification. This allows payload.bin to be launched in place of `BOOT0` (the first partition on your Switch's internal storage, which contains Nintendo's official bootloader) by a modchip firmware module called `sdloader`. This differs significantly from the RCM exploit fusee-gelee, which is what unpatched consoles use. Modchips allow any Switch console, including all "patched" consoles, to run CFW.

-----

### **The `sdloader` firmware module**

`sdloader` is the module built into the Picofly firmware (and all other modchip firmwares) responsible for loading `payload.bin` from the root of your SD card. It will always run if the modchip installation is successful.

-----

### **Voltage glitching**

Voltage glitching is a type of fault injection attack, a hardware security exploitation technique. It works by briefly and precisely dropping the CPU's supply voltage below its safe operating threshold. This voltage disturbance causes the processor to enter an erroneous state, effectively violating what are known as setup and hold time requirements of the chip's internal logic, which can cause instructions to be skipped or memory operations to be corrupted.

In the context of the Switch modchip, this erroneous state is exploited at a very specific moment during the boot process: when the bootROM performs its signature verification of the next boot stage. If the glitch is timed correctly, that verification check is skipped, allowing the modchip to redirect execution to `payload.bin` on your SD card via `sdloader`.

Voltage glitching is widely used in hardware security research and console hacking. It has previously been used to attack devices such as the Xbox 360, PS Vita, and various microcontrollers. It is considered an attractive attack vector because it is relatively inexpensive to set up and broadly applicable to many chips.

-----

### **Training**

Once successful glitch timings have been found, the modchip performs a process called "training": stress-testing those timings to verify their reliability. The timings, which define the exact delay and duration of the voltage glitch, are then written to the modchip's internal storage and used to achieve fast boot times on subsequent boots.

If a Switch firmware update changes the relevant boot code, some of those stored timings may no longer work. The modchip will cycle through its remaining stored timings and attempt to re-train if needed. If glitching or training fails entirely, resetting the modchip may be required (which involves opening the console and accessing the modchip manually). In practice, Picofly rarely fails glitching or training unless a hardware issue is present.

-----

### **The modchip's payload**

After glitching and training, the modchip writes its payload to an empty sector on the `BOOT0` partition of your Switch's internal storage. This payload is responsible for displaying the Picofly splash screen (the `No SD Card` screen with the Picofly logo) on boot, and prevents the Switch from booting normally unless `sdloader` is bypassed by holding both volume buttons while powering on. This payload does not interfere with any critical part of the Switch's internal storage.

-----

### **Resources on voltage glitching**

Here are some resources that detail voltage glitching in depth, with great explanations on how it works:

!!! note ""

    <a href="https://www.nccgroup.com/research-blog/an-introduction-to-fault-injection-part-13/">NCC Group - An Introduction to Fault Injection (Part 1/3)</a> - accessible, well-structured intro covering voltage, clock, EM, and optical glitching
    
    <a href="https://www.synacktiv.com/en/publications/how-to-voltage-fault-injection">Synacktiv - How to Voltage Fault Injection</a> - practical walkthrough with real IoT device case studies
    
    <a href="https://www.hardbreak.wiki/hardware-hacking/bypassing-security/voltage-glitching">HardBreak Wiki - Voltage Glitching</a> - concise hardware-hacking focused reference
    
    <a href="https://arxiv.org/pdf/1903.08102">Yifan Lu - Injecting Software Vulnerabilities with Voltage Glitching</a> - academic paper, includes a PS Vita boot-time fault injection case study


