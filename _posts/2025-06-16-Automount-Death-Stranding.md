---
layout: page
title:  "Automounting my drive and playing Death Stranding on my tiny laptop"
date:   2025-06-16 22:06:00 +0200
categories: jekyll update
author: "Lou Fedora"
permalink: /automount-death-stranding

---

What a mess. I wanted to move my Steam files to my new SSD external drive using the options available into the Steam app and cut/paste my Heroic prefixes, but nothing worked. I had to redo it from zero. Since I was recommended to make my drive mounted automatically to have a properly recognised name by Steam (so different that run/media etc), it was the opportunity to do it.There's [this guide](https://smarttech101.com/how-to-mount-disks-and-create-fstab-entries-in-linux) that was recommanded to me but brwosing further, I saw that Ubuntu users had a GUI to do that. I took my bet that Fedora too as I saw aa "Disks" GUI in the available apps. And I was happy to see that it worked like this and in the end updated the fstab entries just like in the guide, so I preferred doing it like that. Archiving the manual technique in here in case I need it in a non GUI situation one day, though.
{: style="text-align: justify;"}

<br/>

<br/>

**<u>So here is what I've done : </u>**

<br/>

- Open the Disks GUI, select my wanted disk and click the little gear below the storage bar : ![mount-options](/assets/images/mount-options.png)
{: style="text-align: justify;"}
<br/>
- On the top options, I unchecked "Default options" so I can have access to the naming options, and clicked "Automatically mount drive" : 
<br/>![automount](/assets/images/automount.png)

- Change the name of my drive, but more importantly, custom my drive mount point (put what you want after mnt/), and select the ID name below the way it's written in fstab : 
<br/>![mount-names](/assets/images/mount-names.png)
{: style="text-align: justify;"}
<br/>
- Of course, saving what I said and input my password so it would also change the fstab entry.
{: style="text-align: justify;"}
<br/>
<br/>
After all of that, I could set up my games properly again... With inputting a special line to activate DirectX12 for Death Stranding, which is `VKD3D_FEATURE_LEVEL=12_1 %command%` so that Vulkan would understand that I need DX12 and do the necessary layering. Then, I put everything at the lowest quality, activated FSR1 and.. It worked properly on my very weak laptop ! I'm very impressed that I can actually run such demanding game without my laptop crashing. It's not the ultimate FPS or resolution granted, but it's playable. FSR1 is crucial though, without it I would've been in lagged pixel land and would've dropped the game unless I got the Steam Deck. 
{: style="text-align: justify;"}
<br/>
I'm so amazed I can run a variety of games, including my beloved Nier Automata and Life is Strange too, with no prior settings than just lowering resolution just a little. On Windows, it didn't even run Genshin properly, no matter the quality I chose. I wouldn't have even tried to launch any other game because it most likely would've frozen/crashed. The fact that I can now and without playing in laggy territory either, just makes me very happy. I can finally use that laptop in other ways than just browsing and Discord. Fedora really gave it a new life. No way I'm coming back now ! I already thought I'd stay because I loved my Linux experience anyway, but here it's just even better than I imagined.
{: style="text-align: justify;"}
