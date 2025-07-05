---
layout: page
title:  "Setting up remote services : SSH and DWService"
date:   2025-07-05 00:06:00 +0200
categories: jekyll update
author: "Lou Fedora"
permalink: /ssh-dwservice-remote-setup

---

I'm thinking about getting a Raspberry Pi and setting my own instance of Nextcloud and maybe some other stuff. Hence, I had to experiment a bit with SSH and remote desktops beforehand to make sure I find a process that's clear and would work once I am with the Pi. It made me learn about firewall rules too. I spent quite a long time dealing with outdated info about VNC, just for in the end, finding a solution which was much simpler :") Well, at least I could do the research and I'm aware now.
{: style="text-align: justify;"}
<br/>
**<u>So here is what I've done : </u>**
<br/>
<br/>
- Few weeks ago, I've already set up a secure SSH from my laptop to Github, to update my website a bit more securely. To do that, I used both [the official Github tutorial about SSH secure keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) and [this DistroTube video](https://www.youtube.com/watch?v=r4CyUAFMUcY&t=1254s). The video was helpful because it enabled me to double check, especially for the last command `git push git@github.com:(repository link)` because I didn't get the good words the first time. It works flawlessly now, provided I don't mess up the titling or labelling of my documents (but this isn't a Github specificity, even in CLI to do stuff it doesn't work properly if you typo lol).
{: style="text-align: justify;"}
<br/>
- What I did then, is battling with trying to set up a VNC server and getting stuck for around two days because `systemctl` told me that the daemon was dead. After trying different sources, it just happens that there are sharing options into the Gnome settings (in Share, and also in System, Remote Desktop) that set up at least a RDP connection out of the box. It also seems to be Wayland compatible since apparently, one Wayland compositor actually works with RDP. Someone in the Fedora forum also advised me to use FreeRDP, since it's open source and supposedly works well.
{: style="text-align: justify;"}
<br/>
- BUT when I installed FreeRDP, I was quite overwhelmed by the fact that even the Flatpak was a full CLI interface with a plethora of options that I don't know about, since all of this networking/desktop sharing things are very new to me. So I uninstalled it and browsed the internet in hope to find something similar with a bit more GUI... AND I FOUND IT ! It's on [dwservice.net](https://www.dwservice.net/fr/home.html) and it works very well. You download the .sh, run it as executable thanks to `sudo chmod +x` and then `./(.sh file)` and you can choose either to run it as executable only (works without install) or to install the agent and then link the agent to your account on the site. It's not complicated to do at all, the video tutorials are on the site's main page so it's a really easy setup, and the software is free, open-source and made in Europe ! I'm very glad I found it.
{: style="text-align: justify;"}
<br/>
- Then, I wanted to try SSH between my main and secondary laptops to get a hand on how it works before the Pi. [This guide](https://opensource.com/article/20/9/ssh) really gives the good basics. I just had to pick out the good IP address, so in between the different CLI commands available, after some observations, I picked `ip addr show | grep "inet"` because it shows the full address (including the /24 which would be handy later to set up the firewall). And if the connection seems not to work.. then do like me and set up the good firewall rules !
{: style="text-align: justify;"}
<br/>
- So for the firewall, [this article](https://www.tecmint.com/restrict-ssh-access-to-local-network/) really is way sufficient to reach the goal of securing the connection and allowing only the addresses you wish to access your computer through SSH. Just, put the entire address (with the /24) and don't forget the `to any port 22` in the end so that it specifies it's for SSH. I did forget those and of course, the first time, it didn't work. With inputting them correctly, it worked for sure on the Mint Firewall UFW, so it's no reason it wouldn't work on Fedora Firewalld as well (just that I didn't test that one yet).
{: style="text-align: justify;"}
<br/>
It feels very good to have found easy to use yet powerful tools, I really appreciate to learn stuff and make things work. Those remote tools in peculiar are so badass, I feel happy I could make them work too. **Conclusion : usually, something complicated can be paired with something simpler.** It can take slightly more to search, but eventually it can exist. At least, on that case, it did for me :)
{: style="text-align: justify;"}
