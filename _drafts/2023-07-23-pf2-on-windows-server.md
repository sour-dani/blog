---
title: "Pre-Fortress 2 on Windows Server Core - [(Don't Fear) The Command Line](https://www.youtube.com/watch?v=Dy4HA3vUv2c)"
layout: post
published: false
---

Pre-Fortress 2 community servers are hosted by a variety of gamers with varying systems. Some of them run the server off a spare PC in their living room, others use full on Container based systems. However, if there's one thing that is prevalent among the popular servers is that they run *[Windows Server](https://www.youtube.com/watch?v=Oc7Cin_87H4)*. As much as I'd like them to get over their fear of Linux, I understand how intimidating CLI is to new server hosts. To tell the truth, it was only 3 years ago that I was hosting discord bots on a copy of Ubuntu Server where I installed Xorg just so I didn't have to use the command line. 

So I came up with a potential fix! I started experimenting with Windows Server 2016 and came up with a guide on how to run PF2 from the Windows CLI. Windows is still a RAM hog but at least few resources will be spent on rending a Desktop Environment


So far none of the server hosts have read the guide but they do have to switch operating systems soon as the [EOL of Windows Server 2012 R2 is on October 10, 2023](https://learn.microsoft.com/en-us/lifecycle/announcements/windows-server-2012-r2-end-of-support). Currently at least two PF2 servers run on Windows Server 2012 R2 to my knowledge. My goal for this tutorial was to ween them off the Desktop Environment and slowly ease them into a better CLI, but for now the familiarity of Windows should be enough.