# Unofficial repo manifest collections for Xiaomi Mi 6 (sagit)

This branch is for **LineageOS**

## Credits

- Verevka, for [device configuration files](https://github.com/Verevka/android_device_xiaomi_sagit)
- Resurrection Remix OS Team for [their ROMs](https://github.com/ResurrectionRemix)
- Xiaomi, Qualcomm, SONY and Samsung etc. for those proprietary libraries and Linux kernel. But still, **hope you guys can follow GPL licence and release Mi 6's Linux kernel source. Thanks.**

## Usage

**This is the solution I'm currently using. Probably it's wrong but it just works as I expected. Anyone who has some better solution, please tell me in the issue or throw me a pull request.**

1. [Set up your building environment](https://source.android.com/source/initializing?hl=en)
2. Grab the source code, by these commands:

	```
	repo init -u https://github.com/huming2207/sagit_unofficial_repo_manifest.git -b lineage
	repo sync -f --force-sync --no-clone-bundle -j16
	```
	
3. After download finishes, append this: `add_lunch_combo lineage_sagit-userdebug` to the last line of `vendor/cm/vendorsetup.sh`, 
4. Run command: `cp device/xiaomi/sagit/sagit.xml .repo/local_manifest/` 
5. RUN repo sync AGAIN to get Xiaomi's proprietary libraries: `repo sync -f --force-sync --no-clone-bundle -j16`
5. save and compile as an ordinary LineageOS/RROS build process.