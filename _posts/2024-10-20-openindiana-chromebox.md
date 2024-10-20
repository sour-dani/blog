---
title: "OpenIndiana on Chromebox: Tomorrow's Solaris on yesterday's machines"
layout: post
published: true
---

<img width="500" alt="OpenIndiana installed on a jailbroken Chromebox" src="{{site.baseurl}}/assets/images/chromebox/openindianachromebox.jpg">

Solaris is an OS we're all somewhat familiar with but consider it some kind of mythical creature. It wasn't something I grew up with and I haven't heard of many folks using it in a professional setting but the fact that [Oracle still supports it](https://www.oracle.com/solaris/solaris11/) shows that somewhere, somehow, some poor sap in IT has to maintain a geriatric mission critical system.

What if I told you that there was... another way... some kind of way to... free... your mind...

Illumos is the kernel inside OpenIndiana. It powers the very soul of the OS. Illumos itself is based on OpenSolaris which was freaking [led by the same guy who made Debian](https://docs.openindiana.org/misc/openindiana/#why-is-it-called-openindiana)! OpenSolaris was kicking around for a few years but the gates were sealed off when Oracle stepped into the picture. They walled off the Solaris garden forever sealing it's fate as just another enterprise Unix OS.

## NOT ALL IS LOST!!
OpenIndiana aims to pick up the pieces and keep pushing onwards. It's goal is to be the premier  OpenSolaris solution for hobbyists and businesses. Personally I think it should aim to replace Oracle Solaris, to keep people in the FOSS ecosystem and encourage maintainence of existing systems but with the benefit of modern technology.

## The actual point of this blog post.
I love messing around with Chromeboxes and for the unitiated; at one point Chromebooks weren't the only way to gain access to the Chrome browser OS. You used to be able to purchase small form factor ChromeOS machines that could sit on your desk and browse the web. The older models now sit at around $20 and are collecting dust on eBay. They're little celeron machines with not much memory but they can perform comparably to a Raspberry Pi. I know that's controversial to say but I don't care! Not every small computer project needs pinout and the benefit of it being an x86 based machine means that it can run a whole host more Operating Systems and software.

At one point I had two Chromeboxes stacked on top of one another. One running a Jellyfin instance and the other was a Minecraft Bedrock Edition server I helped set up for my little brother. They are pitiful in storage but a quick swap of the M.2 drive or plugging in an external storage device fixes that issue. Just be sure to check whether it's a M.2 SATA or NVME drive as I made the mistake of buying the wrong one for mine!

For a good while I was testing the boundaries of just what you could install on a [jailbroken Chromebox](https://docs.mrchromebox.tech/). I would load a Ventoy drive up with a bunch of different older OSs or even silly new ones just seeing what it would boot from. 

So here's where OpenIndiana comes into play... I really badly wanted to run this beautiful feat of engineering on my silly little Chromebox. The traditional route for jailbreaking a Chromebox requires a UEFI only firmware. This means any systems that don't support secure boot will not run. The older your Chrome device [the more likely it is to not support non-UEFI firmware](https://docs.mrchromebox.tech/docs/supported-devices.html).

OpenIndiana is an example of an OS that does not support UEFI and my HP Chromebox G1 is EOL meaning I can only have the UEFI firmware on it. 

But what if I told you it didn't have to be this way... I won't share the link but I took an archived version of [Mr. Chromeboxes's firmware script](https://docs.mrchromebox.tech/docs/fwscript.html) and adjusted it to skip over the EOL checks. Now this is incredibly dangerous and it's plastered everywhere on his website to not do this, but I did it anyway. They only cost $20 and if it breaks I can try my hand at unbricking the machine. By installing the legacy bios, I was able to run and install OpenIndiana to the Chromebox!

## Victory or rather... so I thought..
What a marvelous achievement! I had my Chromebox running the OpenSolaris successor! I could now run whatever software I wanted... right?

<img width="200" alt="Poking a stick at OpenIndiana asking it to do something" src="{{site.baseurl}}/assets/images/chromebox/comeondosomething.jpg">

Well it turns out that the software actually available for OpenIndiana is very limited! Don't expect to start using VSCode and running TuxCart. Not even the installed software would run most of the time. Somewhere, somewhere, some driver was busted. I couldn't do more than try to install or compile software with little hopes of success. I read that [CodeBlock works on OI](https://forums.codeblocks.org/index.php?topic=24033.0) but I didn't have the time or know how to do so. 

So what am I left to do with this machine? Well... sometimes the beauty of computing is getting it to do something at all!