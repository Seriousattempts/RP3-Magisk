# RP3Plus-Magisk & VBMETA files
Retroid Pocket 3+ vbmeta and magisk boot.img for Magisk-v28.1


These files were created from this github repository: https://github.com/skompc/retroid-pocket-3-plus-autoroot

The magisk boot.img and vbmeta_custom.img are to replace the Boot.img and vbmeta-sign.img files in SPD ResearchDownload Tool are under releases. For RP3+ .pac file, refer to https://drive.google.com/drive/folders/1g9m8BlrCsdzXduEUfDERLilVLzxFQxX8


You can also make modifications to the ramdisk and not have to use a different vbmeta-sign.img:

https://github.com/cfig/Android_boot_image_editor
1. Linux only! Windows use WSL/Ubuntu/VirtualBox/whateveruseslinuxcmdline
- Download Android_boot_image_editor to open the stock boot.img that uses the recovery ramdisk using `./gradlew unpack` on your pc
- Copy boot.json and save that somewhere else. boot.img uses avb verification and that allows you to use fastboot and bootloader to flash any boot.img as it now has vbmeta verification
- You can add whatever you want to the ramdisk as long as it will fit when you rerun `./gradlew pack`


In SPD ResearchTool, hit the 2nd botton to the top left to access Download Settings.
*Main Page Tab*
- Change BOOT to the Magisk file
- Change VBMETA to the vbmeta_custom file.
*Flash Operations Tab*
- Select Erase All Flash at the bottom. (Can take 1200 secs when you start flashing to erase all).


If you ever get an NVE error, you can either go to the backup tab in Download settings and uncheck all 3 file backups at the bottom or uncheck NV_LTE under Main Page
