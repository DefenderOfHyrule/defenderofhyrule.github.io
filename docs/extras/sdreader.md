### **Information**

This page will be about hardmodding the SD card reader of normal V1/V2 Switch consoles to the motherboard of the Switch.
The reason this page exists is because I despise the design of the SD card reader circuitry and hardmodding the SD card is the easier and more fun solution as long as you have the required microsoldering experience.

If you're solely looking for the replacement FPC port, its part number is `5042081610` but it can also be found by the search term "Nintendo Switch SD Card Reader FPC Port". It can be found on AliExpress, TaoBao or similar websites.

### **Overview**

I will be using a schematic for this guide, created by @mattyrog (who is also responsible for the creation and documentation of SAMD21 based modchips for unpatched Switch consoles) on gbatemp. [This thread](https://gbatemp.net/threads/nintendo-switch-sd-card-alternative-points.579623/) contains useful pinouts of the SD card reader's FPC connector and alternative points on the motherboard of the Switch. The other alternative points on the back of the motherboard can also be used but may give you lesser performance or will cause the SD card reader to straight up not work.

**The following schematics are what will be useful for this guide:**

??? note "Schematics"

    ![sdcardreader](../img/extras_img/sd_connection.jpg)

    ![pinout](../img/extras_img/sdmolex.webp)

#### What you need:

- A soldering iron with a small(er) tip (preferably temperature controlled that can reach 350C consistently)
- Good quality flux
- Good quality 30-32 awg wire (such as Kynar wire, other wire can work as long as it's single core)
- Isopropyl Alcohol (preferably 95-99% IPA)
- Soldering tin (leaded is recommended, unleaded will work depending on your skill level)
- A fume extractor (for your own health and safety)
- A microscope (optional but recommended)

#### Instructions:

