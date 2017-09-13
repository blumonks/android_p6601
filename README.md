# lineageOS 14.1 for BLU R1 HD
What works:
- Boots
- Everything that is not mentioned in "Issues" (see android_device_blu_p6601)

For all bugs, please open a new issue on github with a logcat and/or dmesg of your issue.

To init this repo:

    repo init -u git://github.com/lineageOS/android.git -b cm-14.1
    mkdir -p .repo/local_manifests
    wget https://github.com/blumonks/android_p6601/raw/cm-14.1/local_manifest.xml -O .repo/local_manifests/local_manifest.xml

To sync source:

    repo sync

To build:

    pushd device/blu/p6601 && ./patch.sh && popd
    . build/envsetup.sh && lunch lineage_p6601-userdebug
    mka bacon

Please see the [Lineage Wiki](http://www.lineageosrom.com/2017/01/how-to-build-lineageos-rom-for-any.html) for building instructions.
