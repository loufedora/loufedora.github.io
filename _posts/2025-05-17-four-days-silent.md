---
layout: page
title:  "4 very silent days"
date:   2025-05-17 13:44:00 +0200
categories: jekyll update
author: "Lou Fedora"
permalink: /four-days-silent
---
Everyone, on Fedora 42 be wary of pa-info. It really does mess up your system if you don't take care of what it does. <b>Don't press 'yes' blindly otherwise it does this :</b> 
<br/><br/>
![audio_gone](/assets/images/audio_gone.jpg)
<br/><br/>
As a beginner now I'll definitely be wary. Everything on Fedora runs with Pulseaudio, so without it Pipewire doesn't connect to the sound. Firefox, Videos, rhythmbox don't work either. So be wary and never accept to withdraw that package EVER.
{: style="text-align: justify;"}

Other different debug solutions for sound are available on [this Fedora discussion page](https://discussion.fedoraproject.org/t/missing-codecs-video-playback-not-works-all-the-time/152765/202). It's long but in case your problem isn't linked to the servor going wrong, it may be handy for you.
{: style="text-align: justify;"}

A handy command that was given to me to understand dependencies and removals is --assumeno at the end of the install command. It's so useful, I'm not going without it !
{: style="text-align: justify;"}
