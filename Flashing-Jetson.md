# Flashing Jetson with provided image
DroneCore.Suite is basically shipped with jetson flashed with current version of system image. This image evolves over time, so the need to re-flash jetson system image may arise. This section is about how to flash jetson with provided system image. 

## Instructions:
**Creating working directory for device:**
  - in following steps, jetson is unconnected from the host PC
  - download and install NVIDIA SDK manager [official web](https://developer.nvidia.com/nvidia-sdk-manager) 
  - open SDK manager 
  - choose "Target Hardware" and "Linux" according to which system is image intended for. (Jetson Xavier NX modules / JetPack4.6 used in this example)
  - continue through all the steps (with jetson unconnected) 
  - if SDK Manager show flash dialog, click on "Skip".
  - if installation is complete, click on "FINISH AND EXIT".
  - now working directory for target is created in '/nvidia/nvidia_sdk/' folder. 
 (JetPack_4.6_Linux_JETSON_XAVIER_NX_TARGETS in this example)

**Download custom_system.img and copy to working folder:**
  - download `custom_system.img.raw` from storage [KDE BUDU ULOZENE IMAGES ??](link)
  - backup original system.img and system.img.raw in .../Linux_for_Tegra/bootloader/ directory
  - move `custom_system.img.raw` to `/nvidia/nvidia_sdk/$target_working_directory/Linux_for_Tegra/bootloader` as `system.img`
(`sudo mv custom_system.img.raw .../JetPack_4.6_Linux_JETSON_XAVIER_NX_TARGETS/Linux_for_Tegra/bootloader/system.img`)

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


# Compilation and flashing with custom system
If the user needs to customize system image in different way as Airvolute provides, for example custom kernel drivers or other modifications, there are instructions in documentation provided by NVIDIA how to build own system. 

[Kernel Customization](https://docs.nvidia.com/jetson/archives/l4t-archived/l4t-322/index.html#page/Tegra%2520Linux%2520Driver%2520Package%2520Development%2520Guide%2Fkernel_custom.html%23wwpID0E0QD0HA)

[Flashing and Booting the Target Device](https://docs.nvidia.com/jetson/archives/l4t-archived/l4t-322/index.html#page/Tegra%20Linux%20Driver%20Package%20Development%20Guide/flashing.html)

[JetPack Archives](https://developer.nvidia.com/embedded/jetpack-archive)

Following instructions in materials above, the developer is able to obtain kernel sources, make changes in them and flash custom system to jetson.

**WARNING**

Obtained kernel sources do not support all features of DroneCore.Pilot board by default, so the developer must apply some changes in kernel sources to make system working with .Pilot board. Airvolute provides JetPack-specific package with all changed files in default kernel sources, according to which the developer can customize kernel sources to match .Pilot board.
This package contains customized pinmux, kernel drivers, device tree and configs. Choose package according to JetPack version of obtained kernel sources. Package can be downloaded from this link: [LINK NA ULOZISKO ???](blala)


