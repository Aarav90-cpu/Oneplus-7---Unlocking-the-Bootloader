# Oneplus-7---Unlocking-the-Bootloader
This guide shows how to unlock the bootloader while providing the files to do it!

`<WRITTEN BY A HUMAN>`

> Only Support Oneplus 7
>
> Do not use Windows VM... Use Windows To Go instead.

# Introduction

I know... the pain... torture of unlocking a bootloader on a Oneplus 7 since I have been through it 2 times!

See if you have a Oneplus 7 stuck on the Stock OS of ANdroid 12 you cannot unlock it since the unlocker is basically broken!

Also this requires a windows computer linux users! SO get a windows 10 iso file and boot it with Windows To Go on rufus which also requires a windows computer!

# Getting started

 - Clone the repo on your windows machine or if using linux your windoows-to-go machine

 - Go to Settings --> About Phone and tap the build number 7 times!

 - Enable Developer options!

 - Install the Qualcom Drivers Provided for communicating with the phone when it is in edl mode!

Now you phone is in edl mode! (Emergency Download or you can say out time machine to the past)

# MSM Download Tool

First of all we need to degrade the OS Version to Android 10 (Oxygen OS 10)

For that we will use the MSM Download tool on Windows which you will have if you clone the repo which you have to do first!

 - Open MSM Download Tool ( I will call it MSM ).

    - Click on Start!

 - Put your phone into edl mode by running `adb reboot edl`

It will detect your device and start flashing to it!

If it fails get it into edl mode again by pressing down the Volume Up and Down buttons at the same time to force it into edl mode.

 - Once it boots up just set it up.

# Unlocking the Bootloader ( Linux Users you can come back to Linux if you want now )

 - Now just Re-Enable Developer options the same way!

   - Toggle the `Alow the bootloader to be unlocked` and enable usb debugging

 - Run `adb reboot bootloader` on your pc to put it into fastboot!

 - Once it is in fastboot run `fastboot oem unlock` [ Sometimes it will just show a black screen and not the fastboot UI which is normal run it anyway ]

And bam your bootloader is unlocked.

# Going back to Android 12 with a unlocked bootloader

Now that you have unlocked the bootloader but Lineage OS needs Android 12 of the stock os or any other custom rom requires it or you want to be on the latest version?

 - Boot back into fastboot

We will use TWRP! (Image provided)

   - Run `fastboot boot <PROVIDED_TWRP_IMAGE>` to temporarily boot twrp!

 - In TWRP click on Advanced --> ADB Sideload

   - Run `adb sideload Android12.zip`

It will run and say it failled at 47% which means it is sucessful!

 - Now reboot the phone

Say hi to Android 12 with an unlocked Bootloader!

Now root with magisk or install any custom ROM of your choice.
