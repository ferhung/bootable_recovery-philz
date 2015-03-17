__<center><big>Original PhilZ Touch Recovery 6 (ClockworkMod 6 based / Advanced Edition)</big></center>__

__<center><big>Continued by: sudosurootdev</big></center>__

__Philz XDA Home page:__
http://forum.xda-developers.com/showthread.php?t=2201860

#### Building

If you haven't built a recovery ever before, please look up the thread linked above.
If you regularly build ROMs/Recoveries for your device, and have a working CWM setup
on your build machine, then you can quickly set up and build Philz Touch recovery as well

Check that this patch is in your `build` directory:
    https://github.com/CyanogenMod/android_build/commit/fddc5f43

Clone recovery to bootable/recovery-philz folder:

    git clone https://github.com/sudosurootdev/bootable/recovery-philz bootable/recovery-philz -b L5

...or add it to your build manifest:

    <project path="bootable/recovery-philz" name="sudosurootdev/bootable_recovery-philz" remote="github" revision="L5" />

Now build with RECOVERY_VARIANT flag set to philz:

    . build/envsetup.sh && lunch && mka -j3 recoveryimage RECOVERY_VARIANT=philz

or

    export RECOVERY_VARIANT=philz
    . build/envsetup.sh && lunch && mka -j3 recoveryimage

or

    add to device BoardConfig.mk:
        RECOVERY_VARIANT := philz
    and run:
        build/envsetup.sh && lunch && mka -j3 recoveryimage
