---
layout: page
title:  "Resetting Timeshift correctly and backing files up"
date:   2025-06-07 17:05:00 +0200
categories: jekyll update
author: "Lou Fedora"
permalink: /resetting-timeshift-backing-files
---
Wow. BTRFS on Fedora seems quite a challenge to configure for snapshots. Either you do a lot of subvolumes to make it work with Snapper which has no GUI so far apparently, or you have to rename the volumes in the Ubuntu way since the devs named it a bit strangely on Mint.
{: style="text-align: justify;"}
<br/>
So... I had to reinstall AGAIN, fortunately this [very simple tutorial](https://youtu.be/bN8gGoBaZ5M?si=vh9VTNOa4YYnTOmj) showed me how to do it with simplicity. Must admit that it stressed me a bit when the installation was over, since it was the first time I partitioned my main system (aka not in a VM). But so far, seems great ! It boots normally and the snapshots are taken within seconds.
{: style="text-align: justify;"}
<br/>
I should find a way to backup BTRFS outside of my laptop sdd, but I'm lazy on that right now. I'll focus on saving my home files, it should be alright. With few snaps in case one update messes up something, I can go back to the previous state now. Haven't tested it though. For files, I use the very popular [Pika Backup](https://youtu.be/W30wzKVwCHo?si=O6IfBw6roDRiLLQk) since it's very easy to use.
{: style="text-align: justify;"}
