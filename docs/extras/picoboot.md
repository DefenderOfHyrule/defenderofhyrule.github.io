### **Information**

This page is unrelated to Switch hacking but is still something i'd like to cover when I have the time for it. PicoBoot is a `Raspberry Pi RP2040 Pico` based modchip for the GameCube.
The modchip is fully open source and is *very* cheap compared to all other existing modchips for the GameCube.
Specific steps such as photos of the screws you need to unscrew aren't mentioned here as they can be found on guides from iFixit (for example). It's expected for you to know what to unscrew.

### **Picoboot**

PicoBoot is a modchip that was "created" by [webhdx](https://github.com/webhdx), it uses a stock `RP2040 Pico` development board that was repurposed as GameCube modchip.
Webhdx wrote the Picoboot firmware for the `RP2040 Pico`, wrote great instructions and provided great information about PicoBoot [here](https://github.com/webhdx/PicoBoot).
They're a very talented person and you should definitely check their console modding projects out.

### **Overview**

The GameCube has a *lot* of hardware based mods made for it that will not be covered on this page. PicoBoot is arguably the best and fastest modchip made for the GameCube, it offers the ability to run custom DOL apps on boot and therefore also allows you to run CFW. It can do much more which is also mentioned on webhdx's PicoBoot github repository.

The best CFW (Custom FirmWare) available for the GameCube is called Swiss. It's a fantastic CFW that can interact with- and utilize almost any external storage hardware device that exists for the GameCube.
Swiss is *technically* not a traditional CFW (more of an all-in-one homebrew utility) and is essentially just an environment where you can browse external storage devices/launch any `.dol` file from. Swiss never modifies the GameCube's official system firmware, I call it a CFW because it's the most commonly known/used terminology for it.

I will be writing my own installation page with installation instructions that I recommend/prefer personally. All credits go to webhdx and you should follow webhdx's guide [here](https://github.com/webhdx/PicoBoot/wiki/Installation-guide) if you want to follow the official guide.

#### What you need:

- A Raspberry Pi `RP2040 Pico`
    - **Note:**
- An SD2SP2 expansion card
- A microSD card (32GB is recommended)
- Good quality 28 AWG, single core wire
- Good quality flux
- A microscope (very optional, the solder points are very big and can easily be seen with the naked eye)
- A fume extractor (for your own health and safety)

#### Instructions:
