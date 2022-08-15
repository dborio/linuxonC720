# linuxonC720
Instructions on how to install your favorite flavor of Linux on an Acer C720 ChromeBook.

Installing Real Linux on the Acer Chromebook C720P:
This is my favorite solution for replacing ChromeOS and installing your favorite flavor of linux on the internal SSD.

Removing the Write-Protect Screw:
Remove all 13 screws from the bottom of the Chromebook. One of them is behind a sticker which you must remove, voiding your warranty.
Then remove the write-protect screw, #7 in this photo: I got that image here: (https://samsclass.info/128/proj/c720-chromebook-annotated-innards.png)

Entering Developer Mode:
Power on your Chromebook. ChromeOS starts.
To enter developer mode press the following key combination:

Esc + Refresh + Power Button

(The refresh button is the 4th button from the left at the top and looks like a curly arrow).

Upon restart, a "scary screen" appears, saying "Chrome OS is missing or damaged".

Press Ctrl+D. From now on you need to press Ctrl+D every time you launch ChromeOS, but soon that won't matter because you'll have Ubuntu instead.

It says "To turn OS verification OFF, press ENTER". Press Enter.

Now it says "OS verification is OFF". After 20 seconds it beeps and says "Your system is transitioning to Developer Mode." After 6 minutes, the "OS Verification is OFF" message appears again, there are three beeps, and the Chromebook restarts.

Now it says "OS verification is OFF". Press Ctrl+D to start ChromeOS.

Enabling Developer BIOS and USB Boot:
Don't log in to ChromeOS.
Press CTRL+ALT+=> (=> is the forward arrow where the F2 key would be on a PC, that is, above the "3" key).

Log in: chronos (No password is needed.)

Execute these commands:

sudo bash

sudo crossystem dev_boot_usb=1

sudo crossystem dev_boot_legacy=1

sudo /usr/share/vboot/bin/set_gbb_flags.sh 0x489

This flashes the BIOS to enable SeaBIOS, which allows you to boot from USB.
Hold down the power button to turn the Chromebook off.

Then install the usb with your flavor of Linux on it (I use Lite Linux https://osdn.net/projects/linuxlite/) and power on the ChromeBook and follow the prompts to install your choice of Linux.

Original instructions by Sam Bowne (https://samsclass.info/128/proj/chromebooks3.htm#:~:text=Installing%20Ubuntu%2015.04&text=The%20prompt%20says%20%22SeaBIOS%22%20and,and%20select%20%22install%20Ubuntu%22).
