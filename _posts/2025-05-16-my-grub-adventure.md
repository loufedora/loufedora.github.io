---
layout: page
title:  "My GRUB adventure"
date:   2025-05-16 19:38:23 +0200
categories: jekyll update
author: "Lou Fedora"
permalink: /my-grub-adventure
---
At some point when I still had windows, I discovered GParted and tried to use it to split my external SDD for doing VMs. That I also discovered and has a bit of trouble setting up the libvirt access to my files but this was solved thanks to youtube tutorials, especially [a tiny but efficient one.](https://www.youtube.com/watch?v=jWySqo6u2l0)
{: style="text-align: justify;"}

But I think I definitely stepped up my VM game too high for a beginner. I may just try simple settings through Gnome Boxes later.
{: style="text-align: justify;"}

When I partitioned, I accidentally unmounted my Mint partition... I was definitely surprised and quite fed up to boot only on Windows while I definitely preferred Windows already. So I went to UEFI settings through the Windows settings panel to boot my Mint USB to remount it back.. And I was so fed up that I chose to erase Windows totally. I didn't yet because I felt I needed it somehow. [This video helped me to de it without compromising my computer boot.](https://youtu.be/QHRrFwEpzPU?si=V6wLisTd1gOGQsRe)
{: style="text-align: justify;"}

And then for the GRUB update to remove boot manager, the same content creator showed [a way that worked for me (going to EFI file and erasing Windows file).](https://youtu.be/VCboZdiztNc?si=DRRZqb9Prfv9HPHG)
{: style="text-align: justify;"}

NB : I'd advise to clean up those folders right away because I thought "I'd do it later" but at some point I had an issue that made me force restart my laptop and... I saw the damned Windows blue screen. I freaked out but could grab the boot settings from the available options and thankfully go back to Mint.. and did the removal because I definitely didn't want to see that screen ever again. It's too dreadful for nothing, even an extra beginner like me could fix that issue.
{: style="text-align: justify;"}

Anyhoo, after all of that I definitely get why Linux Youtubers often talk about ways to recover GRUB menu, since it can disappear easier than you think.. The timeout option is quite nice to edit when having multiple systems, too. It enables to choose. When having one I guess it's better to set the lower value, I should do it.
{: style="text-align: justify;"}
