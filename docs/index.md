#### Introduction

This guide will guide you through the installation of modchips, there are important things you should know before continuing with this guide.

The first thing you should know is that this guide is **not** something you will want to follow without any (micro)soldering experience whatsoever beforehand. 
Installing a modchip requires the aforementioned microsoldering skills and also requires hardware knowledge (knowledge about hardware in general and also the layout of the Switch's motherboard).

The second most important thing is that we *only* support Picofly (the stock `RP2040 Zero` development board and "modchip" variant of it) as it's fully open source from its `RP2040` microcontroller to its firmware.
Any modchip containing the `RP2040` microcontroller is a Picofly modchip.

Other modchips, such as Hwfly or Instinct-NX are not assisted with except for the flashing of open source firmware to Hwfly and SX based modchips. The reason for this is because Hwfly and Instinct-NX are derivatives of SX series modchips, also referred to as "clones". SX series modchips were produced by TX (Team Xecuter) and they were part of the reason why Switch modchips have the bad reputation they have. Next to that, TX are also responsible for the creation (or continuation of SX series modchips) of Hwfly and Instinct-NX modchips, they also use closed source microcontrollers and board designs + they use poor quality board components.

[Continue to Modchip variants :material-arrow-right:](modchip/modchip_choice.md){ .md-button .md-button--primary }
