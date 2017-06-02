# lineageOS 14.1 for BLU R1 HD
What works:
- ???

What doesn't work:
- ???

For all bugs, please open a new issue on github with a logcat and/or dmesg of your issue.

To init this repo:

    repo init -u git://github.com/lineageOS/android.git -b cm-14.1
    mkdir -p .repo/local_manifests
    wget https://github.com/blumonks/android_p6601/raw/cm-14.1/local_manifest.xml -O .repo/local_manifests/local_manifest.xml

To sync source:

    repo sync

To build:

    . build/envsetup.sh && lunch lineage_p6601-userdebug
    echo "ro.project=lineageOS" > build.ini # Required to build kernel with Ninja
    mka bacon

Please see the [Lineage Wiki](http://www.lineageosrom.com/2017/01/how-to-build-lineageos-rom-for-any.html) for building instructions.
