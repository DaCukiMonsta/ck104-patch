# README
A firmware patch for Motospeed CK104 keyboards to fix broken software control

# Sources
The original method comes from [this post](https://www.reddit.com/r/MechanicalKeyboards/comments/7sghkk/eelement_z88_104_keys_lighting_and_macro_editor/) by Reddit user [/u/SharXeniX](https://www.reddit.com/u/SharXeniX). This described using the X2000 firmware on an e-element Z-88 keyboard. However, since the Motospeed CK104 is a clone of this keyboard (or maybe the other way around? at least, they are the same inside), I figured it would work for the CK104 too. I tried it and I was correct.

The executable files originally came from [this store page](https://www.lelong.com.my/e-element-x2000-z88-upgrade-version-rgb-waterproof-dustproof-104-tdcgaming-I5597538-2007-01-Sale-I.htm), which is now dead. Both files are reported as clean by my antivirus, but here are the results of a VirusTotal scan:
  - [install_software.exe (0/64)](https://www.virustotal.com/gui/file/23e3498e4bc4a050305b68feb8b897964aa1bb8ce7b845bb3536c3ef58c05be1/detection) (original name "2- E-Element_K870_Driver_Setup_V1.0.5.exe")
  - [update_firmware.exe (1/71, likely false positive from AI antivirus tool)](https://www.virustotal.com/gui/file/b52ce5606fc2b002e227c329c5ac87aef85eb4587e061b97559f9a29c539d9d6/detection) (original name "在线更新工具.exe", chinese for "online update tool", although I don't think it connects to the internet)
