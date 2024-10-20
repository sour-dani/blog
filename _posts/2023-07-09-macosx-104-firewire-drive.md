---
title: "The Quest for ClassiCube: Mac OS X 10.4 installer booting from FireWire Drive"
layout: post
---

<img width="500" alt="Mac OS X 10.4 Tiger install from FireWire Drive" src="{{site.baseurl}}/assets/images/classicubeg3install/g3tigerinstall1.png">

6 days ago **Action Retro** posted an [IP to his ClassiCube server on twitter](https://twitter.com/ActionRetro1/status/1675976443908505601). In the tweet he stated *"Connecting from old Macs in encouraged, but not required :)"* and I took that personally. I have a 2001 slot loader iMac that I bought for a decent price on Mercari and I pretty much specifically bought it to play [Bugdom](https://github.com/jorio/Bugdom/releases) natively.


With that being said I quickly downloaded the ClassiCube client from [macintoshgarden](https://macintoshgarden.org/games/minecraft-152) only to have it display `Invalid Address`. I was certain I had the correct IP address! It was practically copy and pasted from the tweet! What I realized was that for some reason it *really* wanted a port. After some quick digging and testing from a modern machine I was able to the port for the server. I was able to enter in the full address now, it would start to boot into the server but it would give some `curl` error and then crash when the game window loaded.

<img width="700" alt="curl binary error" src="{{site.baseurl}}/assets/images/classicubeg3install/curlerror.png">

<img width="700" alt="Server IP with Port" src="{{site.baseurl}}/assets/images/classicubeg3install/actionretroserverip.png">

After some light research I had learned that because my iMac was still on `10.3.9` it would be unable to play the funny block game `:disintegrate:`. It was from here, that I knew my quest. Find and assemble a team! A DVD with the 10.4 installer and a USB drive to boot! I was excited and ready to give the machine a much needed upgrade. However, as I soon found out, a G3 cannot boot from USB :(.

My spirit had not dried up yet as I reached out to my uncle who was a graphic designer in the 90s and asked him if he still had any FireWire disc drives. He informed me that any of the drives he once had were long gone. However, he did have a saving grace, a 5GB FireWire hard drive. More then enough for the install disk image. I first attempted to burn the `.iso` to the hard drive by using a FireWire card I have on my PC and Raspberry Pi Imager but it was to no avail. The drive would show up as a disc but when I tried to click on the installer it would give an error `The application "Install Mac OS X" cannot be used from this disk.` I figured that even though I have the disc image, it must be a Windows incompatibility error. So my next step was to use `dd` to burn the iso to the FireWire drive. That took AGES on the G3, in retrospect I *could* have used WSL2 on my PC but I wanted to forego any compatibility issues. Once it was finished it wouldn't mount, for some reason I had managed to fail the easiest imaging command-line tool.

My next attempt was to use Disk Utility by "restoring" the disc image to the FireWire drive. I had to use `dd` to convert the disc image to `.img` but I made sure to run the process on my modern MacBook instead to save time. The process completed and I plugged the USB containing the disc image in the proper format into the G3. I made sure to wipe the drive as a fresh APFS and selected the `Untitled` partition *(disk1s1, I think)* to be the victim of restoration and hit Proceed! It didn't take as long as I thought and before I knew it the drive was proclaiming itself as the `Install Mac OS X` DVD. 

I tried running the application but got the same stupid error as before! `The application "Install Mac OS X" cannot be used from this disk.` Surely I had done all the correct steps... right???? 

But then I remembered the Startup Disk utility in settings! I quickly set the FireWire drive as the boot drive and waited for it to restart.

After much tension the install screen appeared! Finally my work had paid off and We were in 10.4!

<img width="700" alt="BSD MAGIC" src="{{site.baseurl}}/assets/images/classicubeg3install/g3tigerinstall2.png">

The installer ran smoothly and gave me the option to upgrade my system so all my files were saved! **Hooray!!** I really struggled to find a similar solution online and I'm happy to report this works! Let me put it into steps...

## HOW TO INSTALL MAC OS X 10.4 FROM FIREWIRE HARD DRIVE
1. ACQUIRE 5GB+ FIREWIRE HARD DRIVE.
2. PRAY.
3. ACQUIRE MAC OS X 10.4 DVD ISO FROM ARCHIVE.ORG.
4. USE `dd` TO FORMAT IT TO `.img` AND PLACE IT ON A 5GB+ USB.
5. ON THE G3, OPEN DISK UTILITY AND FORMAT THE DRIVE AS APFS (Apple Filesystem Journaled) LEAVE NAMED AS `Untitled`.
6. CLICK RESTORE, SELECT THE `.img` FROM THE USB AND SELECT THE `Untitled` PARTITION.
7. CLICK PROCEED AND BE PATIENT.
8. AFTER IT FINISHES, GO INTO SYSTEM PREFERENCES AND SELECT STARTUP DISK.
9. CHOOSE THE FIREWIRE DRIVE NAMED `Install Mac OS X 10.4...`.
10. PROFIT.

All because I didn't have a FireWire disc drive... did I mention I bought one because I thought this wasn't going to work... I bought it before writing this and while waiting for the drive to restore the disc image.

All I had to do was run ClassicCube again WITH the port and BOOM!

<img width="700" alt="ClassiCube, a Minecraft Clone remade in C++, running on an iMac G3." src="{{site.baseurl}}/assets/images/classicubeg3install/classicubeg3tiger.png">