# Flashing Jetson with provided image
This section is about how to flash jetson with provided system image. 

## Instructions:
**Creating working directory for device:**
  - in following steps, jetson is unconnected from the host PC
  - download and install NVIDIA SDK manager [official web](https://developer.nvidia.com/nvidia-sdk-manager) 
  - open SDK manager 
  - choose "Target Hardware" and "Linux" according to for which system is image intended. (Jetson Xavier NX modules , JetPack4.6 used in this example)
  - continue through all the steps (with jetson unconnected) 
  - if SDK Manager show flash dialog, click on "Skip".
  - if installation is complete, click on "FINISH AND EXIT".
  - now working directory for target is created in '/nvidia/nvidia_sdk/' folder.(JetPack_4.6_Linux_JETSON_XAVIER_NX_TARGETS in this example)

**Download custom_system.img and copy to working folder:**
  - download `custom_system.img.raw` from storage [KDE BUDU ULOZENE IMAGES ??](link)
  - backup original system.img and system.img.raw in .../Linux_for_Tegra/bootloader/ directory
  - move `custom_system.img.raw` to `/nvidia/nvidia_sdk/$target_working_directory/Linux_for_Tegra/bootloader` as `system.img`
(`sudo mv custom_system.img.raw .../$target_working_directory/Linux_for_Tegra/bootloader/system.img`)

**Run Jetson in Recovery mode**
  - the use of complete DroneCore.Suite is assumed
  - power-off board (pressing button on .Power board to turn off DroneCore is enough)
  - on DroneCore.Pilot interconnect FC_REC with GND pin on CONTROL pin header)
  - connect micro usb cable from host PC to USB_DEV connector on .Pilot board
  - power-on (don't forget to turn on DroneCore with button on .Power board)

**Flash board with flash.sh script:**
  - open terminal window in `.../$target_working_directory/Linux_for_Tegra/` directory
  - execute `sudo ./flash.sh -r jetson-xavier-nx-devkit-emmc mmcblk0p1` (for Xavier NX and internal EMMC)
  - for other options with flash script see [Flashing and Booting the Target Device](https://docs.nvidia.com/jetson/l4t/index.html#page/Tegra%20Linux%20Driver%20Package%20Development%20Guide/flashing.html)
<img src=""  width="750">  