# SETUP a Linux environment with a bootable USB drive.

## Requirements: 
- A laptop or desktop you aren't using/needing to load Linux onto.
- A thumbdrive you aren't using/needing to install/boot Linux.
- Download latest Ubuntu LTS iso image file (currently version 22.04)
  - https://ubuntu.com/download (Ubuntu Desktop)
  - NOTE if you plan on using an ARM processor download the correct iso image. 
    - This will be for things like Raspberry Pi's. However, specifically if using a raspberry pi, use their supported image: https://ubuntu.com/download/raspberry-pi

## Steps
1. Create a bootable USB drive using the downloaded iso image.
  - There are various tutorials available online to walk you through this process of configuring a USB drive to boot Ubuntu. Below I have my suggestions.
  - Tidwell Recommendation on which software to use:
    - For Mac use Etcher
      - https://ubuntu.com/tutorials/create-a-usb-stick-on-macos#1-overview
    - For Windows use Yumi
    - For Linux use "dd" command (if you're already using Linux)
2. Figure out how to boot up Ubuntu when you have the USB drive plugged in.
  - Usually inolves turning on the computer and before it boots, you press a certain f-key like f9 or f11. Do some research to figure out the proper key. You may also need to to some BIOS configuration. 
  - Depending on USB drive and Computer you may run into issues. Google Away!
    - My favoritate reliable USB drives for this kind of stuff is SANDISK brand.

3. After you boot up, open up the "Terminal" then type in:
  - `expr 1 + 1`
  - Result should be "2" 

Congraulations you have used the terminal and you are running Linux on that old dusty laptop of. Come back to me for another assignment.

## FAQ
- Do you need a large harddrive / HDD/SSD?
  - No, 32GB - 64GB is fine. You can always buy a larger one later if you need it and go through this process again.
- If I want to build a raspberry pi for this assignment should what do I need to buy?
  - You will want to make sure you have periferals such as a mouse, keyboard, sd card, micro hdmi chord. Recommended to look for bundled official hardware combo kits available online.
