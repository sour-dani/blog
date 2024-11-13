---
title: "DIY Homelab - How I turned stackable jewelry cases and RPi leftovers into a network system"
layout: post
published: false
---

<img width="500" alt="A DIY Homelab featuring a Chromebox that is plugged into a jewelry drawer. The jewelry drawer is housing a raspberry pi and additional drive." src="{{site.baseurl}}/assets/images/homelab/homelab.jpg">

No one expects a jailbroken Chromebox... It's no secret I have religious subscribed to [the teaching of Mr Chromebox](https://docs.mrchromebox.tech/docs/fwscript.html) and at one point I had a homelab to prove it. I have about 4 of these sitting in my closet at this moment. One of which I used as a teaching tool to teach my little brother about the joys of Linux and I have even [managed to get OpenIndiana running on one.]({{site.baseurl}}/openindiana-chromebox/)


***There's almost nothing you can't do with these things!***

# Raspberry Pi Alternative?
Yes, well... no. But, YES!

This is actually a controversial statement. I have been yelled at on the internet for recommending people to recycle ewaste. Yes, really! The reason being is that while performance wise it would be the same, the Chromebox lacks pinout. Honestly my response to that if you're working on a project that needs pinout you don't need a Chromebox. Alternatives don't have to perfectly match each usecase. Even so, you can easily by serial to usb cables easily off your favorite web store.

**List of computers in the above image from top to bottom:**
1. HP Chromebox G1
    - Debian 12
    - Jellyfin
2. 4TB external HDD
3. RPi running Wireguard for remoting into my home network. 
    - Was misconfigured
4. 2TB External HDD
5. RPi 3A+
    - OMV5