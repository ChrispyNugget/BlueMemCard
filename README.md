# BlueMemCard

BlueMemCard is a drop-in replacement PCB for the PSX memory card that combines the existing PicoMemcard and BlueRetro technologies into one board. BlueMemCard allows the use of a Bluetooth controller while also functioning as a regular memory card and also allows the memory card image to be transferred to a PC via USB. Just as important, the board fits right in the stock Sony memory card housing, resulting in a stock and stealth look. 

This is possible as the PSX memory card and controller ports share the same bus, and have nearly identical pinouts. Currently only P1 is supported, and there is no detection if a regular controller is connected. 

<img src="./Images/top.jpeg" alt="Custom PCBs" width="250"> <img src="./Images/bottom.jpeg" alt="Custom PCBs" width="250"> 
<img src="./Images/board.jpeg" alt="Custom PCBs" width="250">

Demo Video: https://youtu.be/jc9e9mESD8Y 

**Note:** These images show the rev1 design. The rev2 design that is included in this repository has slightly improved board dimensions and footprints. As of Nov 10 2022, I have ordered rev2 boards to build and test, and I do not anticipate any issues as the changes from rev1 were very slight. The rev1 Gerbers are also included and have been tested and verified, but the board needs to be filed down a bit in order to fit into the shell.

# Ordering Instructions

The Gerber files have been generated specific to JLCPCB: https://support.jlcpcb.com/article/149-how-to-generate-gerber-and-drill-files-in-kicad

Specify 0.8mm board thickness. 

Specify the following layer sequence:

L1 (Top Layer)     - ps1_memcard_test-F_Cu.gtl

L2 (Inner Layer 1) - ps1_memcard_test-In1_Cu.g2

L3 (Inner Layer 2) - ps1_memcard_test-In2_Cu.g3

L4 (Bottom Layer)  - ps1_memcard_test-B_Cu.gbl

# Assembly Instructions

See BOM folder for parts list and DigiKey / Mouser links.

When dropping in the assembled board into the memory card housing, you may need to use flush cutters to snip off a support under the top half of the housing. Only some memory cards seem to have this support. 

# Software Instructions

The ESP32 can be flashed via darthcloud's instructions: https://github.com/darthcloud/BlueRetro/wiki/BlueRetro-DIY-Build-Instructions

Here are instructions specific to Windows 10: https://github.com/darthcloud/BlueRetro/wiki/Flashing-firmware-Windows-10

To flash modules, a board like this can be used: https://a.co/d/7GO22nZ 

This project does not support PicoMemcard+, only the original PicoMemCard project. Use PicoMemcard.uf2 in v1.0.0 from the PicoMemcard releases: https://github.com/dangiu/PicoMemcard/releases

The memory card image you drop onto the board must be named MEMCARD.MCR

# Credits and Notes

This project is merely a combination of two incredible projects by darthcloud and dangiu. I also must credit PhenomMod as I matched my PCB dimensions to the sd2psx board.

https://github.com/darthcloud/BlueRetro

https://github.com/dangiu/PicoMemcard

https://github.com/sd2psx/pcb 

If you feel so inclined, please support these creators!

https://ko-fi.com/darthcloud

https://www.patreon.com/darthcloud

https://ko-fi.com/dangiu

https://store.phenommod.com/

If anyone is interested in the KiCad project files feel free to reach out. 
