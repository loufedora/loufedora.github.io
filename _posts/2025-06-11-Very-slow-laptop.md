---
layout: page
title:  "Installing Mint on a slow computer"
date:   2025-06-11 20:00:23 +0200
categories: jekyll update
author: "Lou Fedora"
permalink: /mint-very-slow-install

---

Ah, I had a nice combo of everything in an install when my dad asked me to install Mint on one of his old computers... I learnt the hard way that i3 is slowwwwwww !
{: style="text-align: justify;"}
<br/>A compilation of everything I've seen so far :

<br/>

- Deactivating Secure boot in BIOS, and then having a doubt about the USB key being able to to do anything because **something else was plugged in the other port**. It seemed going smoother once it could go fully in.
  {: style="text-align: justify;"}

<br/>

- All was  so slow... **The whole install took 4 times longer** than when I tried on my test old i5. Granted this time I picked Cinnamon over XFCE... Maybe I shoudln't have lol
  
  {: style="text-align: justify;"}
  
  <br/>

- **The mirrors by default for Mint are awful**. More than that, they freeze in place so at the part of the install in which it needs to install extra packages, it loads in the void. Thankfully some part is skippable, but I feared that it coul've impacted the quality of the final install... Fortunately, it didn't. 
  
  {: style="text-align: justify;"}
  
  When I could reach the final install on the laptop, I put some French mirrors and it updated in no time.Those are definitely very important. If someday my Fedora install has some  issues in regards to downloading packages, I'll definitaly **check up if my mirror list is correctly set up**.
  
  {: style="text-align: justify;"}
  
  <br/>

- Dad **wanted to keep a Win10 partition** because he stcoked documents on it. Because of that, even when Mint took most of the disk (1TB), it logged automatically in Windows. Logging into the BIOS again **to change the Boot order** fortunatley functioned.
  
  {: style="text-align: justify;"}
  
  <br/>
  
  So yeah. **Never assume that an install resembles another**, check up if the device handles your distro (fortunately it still does, it works fine). Use lightweight distros if necessary and... **Be patient and have good mirrors haha**
  
  {: style="text-align: justify;"}
