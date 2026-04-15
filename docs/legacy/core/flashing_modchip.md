# **Flashing the modchip**

### **Information**

Modchips have their own separate firmware version that is separate from the Switch system firmware version, this firmware ultimately determines the functionality and performance of your modchip.
Flashing the firmware to the modchip is not mandatory if your modchip already comes "pre-flashed", but it is recommended to do so.

Any Picofly firmware below version `2.75` is deprecated and is no longer supported, which is why we will be ensuring that the modchip has the latest firmware version (currently `2.82`) flashed to it. This will make sure that you have the best performance and hardware compatibility.

This process is the same for all Picofly modchip models, just use the pictures in the instructions below as reference for your own modchip.

!!! note ""

    **If you're looking to flash your modchip's firmware while it's installed in your Switch console already, see [this page](../../extras/alternate_flashing.md).**

-----

#### Requirements:

- The micro USB / USB-C debug port that comes with a modchip "set" (image shown in the "Instructions" section below)
- Your Picofly modchip
- The latest release of [usk](https://github.com/DefenderOfHyrule/usk/releases/latest) (`firmware.uf2`)
- A computer or Android phone (computer recommended)
- A USB type C to USB type A cable / A micro USB to USB type A cable capable of data transfer
     - The type of cable required depends on the modchip revision you have.
       More recently produced Picofly modchips will come with USB type C debug ports.

#### Instructions:

1. Position your modchip and included USB debug port in the upwards facing position. This means with the side of the RP2040 microcontroller (the square chip with the Raspberry Pi logo) facing you. This is important    because if you don't do this, you can risk frying the USB circuitry of the modchip. The USB debug port additionally also has `UP` text written on it to indicate the orientation of it. <br>
![picofly](../../img/general_img/picofly.JPG){ width="600" }{ loading=lazy }

1. Lift up the locking tab and plug the USB debug port into the connector at the bottom of your modchip, then lock the locking tab to secure the USB debug port in place. <br>
![picofly-with-usb](../../img/general_img/picofly-with-usb.JPG){ width="600" }{ loading=lazy }

    - This step can also be ignored for the stock `RP2040 Zero` development board users as they do not have this port and do not require a separate USB debug port.

1. Hold the `BOOT` button on the modchip and plug the USB debug port into your PC via your data transfer-capable USB cable. <br>
![picofly-with-cable](../../img/general_img/picofly-with-cable.JPG){ width="600" }{ loading=lazy }



1. Your PC should play the "Device connected" sound and a drive should show up on your PC, you should be able to access and open it. <br>
![drive](../../img/general_img/drive.png){ loading=lazy }


1. Drag the `.uf2` file into the root of the drive and wait for the file transfer to finish. The drive will eject itself after it's done. <br>
![flashing](../../img/general_img/flashing.gif){ loading=lazy }



1. Your modchip is now flashed with the latest firmware version, proceed with the modchip installation for your model of Switch console by pressing the relevant button below.

#### Your modchip is now flashed with the latest firmware version, proceed with the modchip installation for your model of Switch console by pressing the relevant button below.

[Continue to Modchip installation Switch :material-arrow-right:](normal.md){ .md-button .md-button--primary }

??? note "About flashing Hwfly/SX series modchips"

    Instructions on how to flash Hwfly/SX series differ a tiny amount from Picofly modchips, they don't have the `BOOT` button and only require you to plug them into your PC to flash them.


    #### Requirements:
    - The micro USB / USB-C debug port that comes with a modchip "set" (image shown in the "Instructions" section below)
    - Your Hwfly/SX series modchip
    - Latest release of [hwfly-firmware](https://github.com/hwfly-nx/firmware/releases/tag/0.7.2) (`release_XXX.zip`)
    - A computer or Android phone (computer recommended)
    - A USB type C to USB type A cable / A micro USB to USB type A cable capable of data transfer


    #### Instructions:

    1. Position your modchip and included USB debug port in the upwards facing position. This means with the side of the microcontroller (the biggest square chip) facing you. This is important because if you don't do this, you can risk frying the USB circuitry of the modchip. The USB debug port additionally also has `UP` text written on it to indicate the orientation. <br>
    ![hwfly](../../img/general_img/hwfly.jpg){ width="600" }{ loading=lazy }

    1. Lift up the locking tab and plug the USB debug port into the connector at the bottom of your modchip, then lock the locking tab to secure the USB debug port in place. <br>
    ![hwfly-with-usb](../../img/general_img/hwfly-with-usb.jpg){ width="600" }{ loading=lazy }

    1. Plug the USB debug port into your PC via your data transfer-capable USB cable.
       your PC should play the "Device connected" sound, which indicates that it's plugged in correctly.<br>
           - **Note:** The modchip will flash blue as soon as it's connected to a power source if the modchip was flashed with spacecraft-nx or hwfly-nx previously. This indicates that it's awaiting USB input.<br>
       ![hwfly-with-cable](../../img/general_img/hwfly-with-cable.jpg){ width="600" }{ loading=lazy }![hwfly-flashing](../../img/general_img/hwfly-flashing.jpg){ width="600" }{ loading=lazy }<br>

    1. Extract the hwfly-firmware zip somewhere, then open the extracted folder and run `flash.bat`.

    1. Wait for the script to finish, it will tell you when it's done and prompt you to press a key to exit the flashing script.
    ![flashing-hwfly](../../img/general_img/flashing-hwfly.gif){ loading=lazy }<br>

        !!! warning "About "Spacecraft-NX `DFU` not found!""
            If the flashing script says that the Spacecraft-NX `DFU` was not found, wait for Windows to finish setting up the device. This can take a minute, so be patient and don't panic. <br>

    1. Your modchip is now flashed with the latest firmware version.
