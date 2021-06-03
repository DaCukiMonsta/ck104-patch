# Motospeed CK104 Firmware Patch
This is a firmware patch for the Motospeed CK104 and E-Element Z-88 keyboards, to fix a bug where their control software constantly says "Device is disconnected" and refuses to control the keyboard's RGB lighting.

# Risks - you must read!
**There is some level of risk when performing this modification.** While it does not involve modifying the hardware, it does involve modifying the firmware of the keyboard.
  1.  There is no known way to back up the original firmware of the keyboard. This means that if the firmware file does not work, **you will not be able to revert back to a working state**.
  2.  Updating the firmware is risky. Unplugging the keyboard during an update, or any other issue which causes the firmware transfer to fail, could brick the keyboard.
  3.  **The updated firmware is known to ever so slightly reduce the maximum brightness of the LEDs in the keyboard.** This is likely because of the different way it controls the LEDs. My entirely unscientific estimate is that with the updated firmware, the maximum brightness is only around 80-90% of what it was originally. Most users haven't even noticed this, and I doubted it myself until others asked, it is very slight. **Don't perform the modification if you're not happy with this.**
  4.  The firmware you are putting onto your keyboard is that of a different model, which was found to work. This is experimental, nobody has done any work to prove it is safe or reliable, we just tried something and it worked. There is no guarantee that the firmware will work, or that it will not cause problems with your keyboard now or in the future. It is provided for free in the hopes it will help someone, as a result we don't owe you anything if it goes wrong.

Because of these risks, you need to understand and agree to the following points before performing the modification. If English is not your first language, please look at the translated copies and make sure you understand this.
  1.  It is possible that this modification could permenantly brick your keyboard. You accept that you are willing to take this risk, and you have a spare keyboard to use if this breaks your current one. While it has so far had a 100% success rate with users, it cannot be guaranteed that it will work, and that it won't break your keyboard forever.
  2.  It is your keyboard, not someone else's. If you break it, you won't make anyone mad (like a parent).
  3.  You accept it might make your keyboard a little less bright (see above).
  4.  You understand that this resource is provided entirely out of goodwill at no cost, and I nor any future contributors to this repository are responsible if you break your keyboard.
  5.  **It is not possible to revert back to your original firmware at this time. This modification is permenant, it cannot be undone.**

If you understand and agree to all of this, feel free to continue.

# Instructions
Before following the instructions below, you **must** understand and agree to the risks above.

  1.  Download the two exe files, `update_firmware.exe`, and `install_software.exe`. The first is used to perform the firmware update (and it contains the firmware file), the second is used to install slightly different control software which is compatible with the new firmware.
  2.  This is the point of **no return**. With your keyboard plugged into the computer, run `update_firmware.exe`. This will *immediately* update the keyboard firmware, it does not ask you "are you sure" before doing it, so don't click the program until you are ready. Once it succeeds, it should say "PASS". Until then, don't unplug the keyboard or turn your computer off.
  3.  The keyboard lights will turn off entirely, and it will become unresponsive. Don't worry, this is normal. It is because you need to power cycle the keyboard to get it to use the new firmware. To do this, you should unplug the keyboard, wait a few seconds, and then plug it back in. Some users reported that they had to use a different USB port to plug it back in the first time, so try this if it's still not lighting up.
  4.  Uninstall any control software you are already using with your keyboard. This is the software that says "Device is disconnected", this must be uninstalled now.
  5.  Run `install_software.exe` to install the new control software.
  6.  Launch the new control software you just installed, everything should work now.

The picture of the keyboard in the new software will look a little different to your real keyboard, but this is okay please ignore it. If you experience any issues, you can open an issue on GitHub or contact me on Discord DaCukiMonsta#8002, or Reddit [/u/DaCukiMonsta](https://www.reddit.com/u/DaCukiMonsta) and I might be able to try and help you.

# Sources
The original method comes from [this post](https://www.reddit.com/r/MechanicalKeyboards/comments/7sghkk/eelement_z88_104_keys_lighting_and_macro_editor/) by Reddit user [/u/SharXeniX](https://www.reddit.com/u/SharXeniX). This described using the X2000 firmware on an E-Element Z-88 keyboard. However, since the Motospeed CK104 is a clone of this keyboard (or maybe the other way around? at least, they are the same inside), I figured it would work for the CK104 too. I tried it and I was correct.

The executable files originally came from [this store page](https://www.lelong.com.my/e-element-x2000-z88-upgrade-version-rgb-waterproof-dustproof-104-tdcgaming-I5597538-2007-01-Sale-I.htm), which is now dead.

# VirusTotal Scan
Both files are reported as clean by my antivirus, but here are the results of a VirusTotal scan:
  - [install_software.exe (0/64)](https://www.virustotal.com/gui/file/23e3498e4bc4a050305b68feb8b897964aa1bb8ce7b845bb3536c3ef58c05be1/detection) (original name "2- E-Element_K870_Driver_Setup_V1.0.5.exe")
  - [update_firmware.exe (1/71, likely false positive from AI antivirus tool)](https://www.virustotal.com/gui/file/b52ce5606fc2b002e227c329c5ac87aef85eb4587e061b97559f9a29c539d9d6/detection) (original name "在线更新工具.exe", chinese for "online update tool", although I don't think it connects to the internet)
