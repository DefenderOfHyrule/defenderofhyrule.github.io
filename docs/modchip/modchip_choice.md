#### Modchip models

There are different modchip models for each model of Switch console, *technically* you can also use modchip models not meant for your specific Switch console but it can introduce complications, which is why it won't be covered here.

The modchip models we will be covering in this guide are:

- Picofly Core (For Normal Switch models | `HAC-001`, `HAC-001(-01)`)
- Picofly Lite (For Lite Switch models   | `HDH-001`)
- Picofly OLED (For OLED Switch models   | `HEG-001`)
- Picofly (Stock development board       | `HAC-001`, `HAC-001(-01)`, `HDH-001`, `HEG-001`)

??? note "Picofly Core"

    Picofly Core is the modchip model for "Normal" Switch consoles, such as regular V1 and V2 consoles. This modchip plugs into the eMMC FPC port on the motherboard and sits on top of the RAM part of the SoC/RAM "IHS" (Internal Heat Spreader) once installed.

    This is what it looks like:

    ![rp2040-core](../img/general_img/core.JPG)

??? info "Picofly Lite"

    Picofly Lite is the modchip model for "Lite" Switch consoles, this modchip is positioned at the top left next to the corner of the SoC "IHS" (Internal Heat Spreader) frame and on top of the metal plate covering the eMMC once installed.

    This is what it looks like:

    ![rp2040-lite](../img/general_img/lite.JPG)

??? success "Picofly OLED"

    Picofly OLED is the modchip model for "OLED" Switch consoles, this modchip is also positioned on the the RAM section of the SoC/RAM "IHS" (Internal Heat Spreader) like the Picofly Core model once installed.

    This is what it looks like:

    ![rp2040-oled](../img/general_img/oled.JPG)

??? warning "Picofly (Stock development board)"

    Picofly was originally based off of the stock `RP2040 Zero` board and is still the most reliable Picofly modchip due to the quality control of these development boards. The installation is a bit more "bare" as you will need to use wire to solder from the development board to the required solder points on the motherboard. Buying an SoC ribbon cable for the solder points on the SoC is recommended if you do decide to go with this method. You will also need to buy the required resistors but there will be more information on this later in the guide. This modchip is compatible with all models of Switch consoles.

    This is what it looks like:

    ![rp2040-zero](../img/general_img/rp2040-zero.jpg)

[Continue to Flashing the modchip :material-arrow-right:](flashing_modchip.md){ .md-button .md-button--primary }
