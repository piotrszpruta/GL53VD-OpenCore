# Asus GL53VD OpenCore bootloader

Bootloader is tested with Catalina and BigSur, both of systems are working fine. You can install Catalina and update from it to BigSur, without any problem. Just after installation put back EFI from your usb stick to your EFI partition on MacOS drive.

## What's working?
  
  ✅ Intel Wifi card (Intel Dual Band Wireless-AC 7265 [#MoreInfo](#Wifi-Card)) \
  ✅ GPU (1050 vram is added as intel HD 630 vram) \
  ✅ Sound \
  ❎ Touchpad (probably not fixable) \
  ❎ HDMI ([#MoreInfo](#HDMI)) \
  ❎ IMessages and FaceTime ([#MoreInfo](#IMessages-and-FaceTime))
  
  
# MoreInfo

### Wifi Card
  Wifi is working "well" on MacOS because of [itlwm kext](https://github.com/OpenIntelWireless/itlwm). It's working at slower speeds, if you have 100/100Mbps you'll get something around 20/20Mbps. It's not perfect but hey, at least we got something.
  To add your wifi to config, go to ``EFI > OC > Kexts > itlwm.kext > Contents`` and open Info.plist. Find key **WiFiConfig** and below it there will be keys for network. Change one to your SSID and password. If you have installed MacOS you can just download [HelPort](https://github.com/OpenIntelWireless/HeliPort) which is GUI for itlwm.
  
  
### HDMI
  HDMI doesn't show any output, I'll try to fix it in later release. On Catalina it freezes system, on BigSur it just do nothing.
  
### IMessages and FaceTime
  This is fixable by finding good SMBios. I will try to add list with them.
