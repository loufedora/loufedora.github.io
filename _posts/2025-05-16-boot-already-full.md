---
layout: page
title:  "Boot is full : Timeshift to blame"
date:   2025-05-16 21:38:23 +0200
categories: jekyll update
author: "Lou Fedora"
permalink: /boot-already-full
---
When I tried dual booting Fedora, it worked but "/boot is nearly full" then "/boot is full" appared. I wonder what was going on. In the end, after investigating, the answer was quite easy to find : <b>Timeshift auto records the snapshot in /boot !</b>
{: style="text-align: justify;"}
<br/>
![time_default](/assets/images/time_default.jpg)
{: style="text-align: justify;"}
<br/><br/>
So just be careful and click the bigger disk or even plus an external disk instead !
<br/>
![time_good](/assets/images/time_good.jpg)

