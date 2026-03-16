---
hide:
  - navigation
  - toc
---

# **Switch Modchip Installation guide**

This guide will guide you through the installation of modchips, there are important things you should know before continuing with this guide.

!!! info "Information"
    If you came here from the NH Server guide, you're here to modchip your Switch. Follow along with this guide if you have the required skills to do so.

-----

The first thing you should know is that this guide is ***NOT*** something you should follow without any prior (micro)soldering experience.  

 - No one involved in this guide or any warnings are in it for money, please listen to them.
 - Watching a youtube video does **NOT** count as experience and is the number one reason outside of iFixit for screwed up installs/broken systems.  
 - Don't just blindly follow anything iFixit says. They have 0 quality control on their guides and you have to fight to get them to make a correction even if the error they make kills the system. Their hardware is also extremely overpriced and in certain cases not even marked properly. 
 - Soldering takes time and patience to learn. It doesn't take a super long time to learn and get to a point you can do the install with little risk, BUT IT SHOULD **NOT** BE YOUR FIRST PROJECT. 


Installing a modchip requires the aforementioned micro-soldering skills and also requires hardware knowledge (knowledge about hardware in general and also the layout of the Switch's motherboard). If you at any point don't know 
what this guide is talking about, you are not ready.

![warning](img/general_img/warning.gif){ width=450 align=center }

The second most important thing is that we *only* support Picofly (the stock `RP2040-Tiny` development board and the premade Picofly OLED "modchip variant") as it's fully open source from its `RP2040` microcontroller to its firmware.
Any modchip containing the `RP2040` microcontroller is a Picofly modchip.

Other `RP2040` based boards *do* work, but the `RP2040-Tiny` development board is the best overall, as it already has 3x 47 Ohm resistors on the `CLK`, `CMD` and `DAT0` lines. If you decide to go with an `RP2040-Zero` for example, you will at least want to buy 2x 47 Ohm (for `CLK` and `CMD`) and 1x 200 Ohm (for `DAT0`) resistors.

More information on where to obtain these modchips can be found on the next page.

- **Note:** Picofly listings with "Hwfly" in the name are not Hwfly modchips but just use the word as keyword so they can be found easier. Picofly modchips have the larger square black chip with the Raspberry Pi logo on them, which is one way of identifying them (this is the `RP2040` microcontroller). They also look much "simpler" in appearance compared to Hwfly modchips.

## Again, this guide is not for beginners and the Switch is not a good first project.

Once you've read this, you may continue to the next page.

???+ warning
      Other modchips, such as Hwfly or Instinct-NX are not assisted with except for the flashing of open source firmware to Hwfly and SX based modchips. The reason for this is because Hwfly and Instinct-NX are derivatives of SX series modchips, also referred to as "clones". SX series modchips were produced by TX (Team Xecuter) and they were part of the reason why Switch modchips have the bad reputation they have. Besides that, TX are also responsible for the creation of Hwfly and Instinct-NX modchips (or continuation of SX series modchips). They also use closed source microcontrollers, board designs and use poor quality board components which in return cause unreliable behavior and quick hardware malfunction over time.

[Continue to Modchip variants :material-arrow-right:](modchip/modchip_choice.md){ .md-button .md-button--primary }
