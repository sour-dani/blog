---
title: "How we turned his old Mac into something useful - An excuse to hangout with my uncle - Part One"
layout: post
published: true
---

My uncle has graciously donated me Mac Computers in the past since he had no more use for them and through my work at Pre-Fortress 2 we needed Mac compilers. I wanted to return the favor by making him his own NAS! He has used Drive bays before but never had something quite like this. I told him about my Pi OMV NAS using an RPi 2B with a 4TB hard drive living inside of a dollar store jewelry case and he wanted one for himself! I refused to make something as basic and DIY.


For months I have been looking at NASs and saving up money to buy him one of his own. This was a thank you gift after all, it should be damn nice! After talking to him about it for some time he was confused on why it took so long. I told him I wanted only the best parts and wouldn't settle for less.

When I told him about how much hard drives cost for servers he looked at me confused. "Dude I have a bin full of hard drives. Let's just use those!" I asked him what we should do about the NAS and he told me to just use his old iMac Pro he had sitting in the corner of his room. It wasn't going anywhere so might as well use it as a Samba and Jellyfin server. 

As for where the drives would live, some time back he gave me a 4-drive bay that I could use for any project. Thus I brought it back to him in hopes of using it for this project. There was one problem though... *Thunderbolt 2*.

This drive bay used the antiquated Thunderbolt 2 port and cables. We did not have a cable for it at all and any he previously had were long gone. In the meantime, I configured a basic Samba configuration but was stopped short when I tried working with an exFat drive to test. Something I have learned after working on enabling Samba on my own Jellyfin server is that exFat has NO permissions. None! Samba can't do shit with that! So the next time I went back to his house I formatted the drives to APFS. 

Now that we had the Thunderbolt 2 cable after a quick Amazon deliver, the finish line was in sight. I plugged in the cable and...

**nothing**

The drives did not show up at all! I was worried that the drives or the bay itself was broken. But after close inspection, the bay light was on, and no activity lights were on for the drives.

It brought the project to a screeching halt and something my uncle neglected to tell me was the computer had **lost the ability to use Thunderbolt 2 after upgrading to 10.15**. Welp, there's your issue there! He said it's why he gave me the bay to begin with, his machine just refused to use it. 

I took the bay and 4 drives home and sure enough it worked fine on my 10.14 Mojave Mac Mini. Something else I noticed was that the iMac had Thunderbolt firmware of 28.4, I believe it might be too high to support Thunderbolt 2. Any research I've done on this topic was inconclusive so I hope it's as simple as installing Mojave on the iMac. I have read that some people have experienced luck with installing 1.8.9 Mountain Lion and reinstalling Thunderbolt Firmware updates.

All that's left to do is take the bay back over there and give it a try. I will be prepared this time. I have Mojave installed on one of the bay drives so I can quickly boot into Mojave on the iMac. 

In my effort to hopefully bypass some weird Mac shenanigans, I installed Debian on the iMac Pro with no luck. He didn't read the drives. I tried to wipe it when I was there but it just couldn't read the Mojave install USB. I tried burning the USB in multiple ways but all in failure. I'm not to sure how I'll manage that one.

I haven't schedule a hang out session with my Uncle but something tells me this time will actually have progress!