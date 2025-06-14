---
layout: page
title:  "Discovering Bottles and setting up my first game on Linux (Genshin Impact)"
date:   2025-06-14 13:06:00 +0200
categories: jekyll update
author: "Lou Fedora"
permalink: /bottles-installing-genshin

---

Everyone talks about Bottles, I finally gave it a try because my dad wanted to use Photofiltre to edit his photos, since he's used to it. Setting up a bottle using the Bottles application is a breeze. However, don't try games with those.. It's better using dedicated softwares like Steam or in my case... Heroic Launcher. 
{: style="text-align: justify;"}
<br/>

Little did I know that compared to Bottles, setting up a game through Heroic Launcher is a massively different process... I could do it a bit but it broke my install anytime I rebooted my laptop ! Aka, the files were downloaded, but Heroic/Proton failed to recognise them correctly. After reinstalling 4 times and getting the same results, I checked the Flathub page of Heroic Launcher and sent a desperate message into their Discord that was indicated there. Fortunately, a Chilian user named F4ngDragon answered me and was patient enough to guide me step by step through it, because it was wayyyy different than I thought. 
{: style="text-align: justify;"}

<br/>

<br/>

**<u>Here is what we did to make it work (in chronological order) : </u>**

<br/>

- Make sure I'm connected to the Epic Store because everything downloads from there, especially Genshin that I wanted. And add the game to the library of Heroic.
{: style="text-align: justify;"}
<br/>

- Then, creating a Game prefix folder in my Documents to use it . It's better to do that than relying on Wine directory by default : ![wine-prefixes](/assets/images/Wine-prefixes.png)
{: style="text-align: justify;"}
<br/>

- Then launch the install to have the game downloaded, accept the path that the Genshin app asks you about. It'll be saved in the directory you setted up before anyway.
{: style="text-align: justify;"}
<br/>

- Then, you need to be able to launch the game using the Wine version called "Proton Experimental". To fetch it, you need to open Steam, download a game with activating overlays and then pick Proton Experimental in the list of Protons that are available.
{: style="text-align: justify;"}
<br/>

- Enter the general settings of Heroic Launcher and browse your files to add the Stream folder in .var as default path for Steam (/home/*username*/.var/app/com.valvesoftware.Steam/data/Steam) : ![steam-default-path](/assets/images/Steam-default-path.png)
{: style="text-align: justify;"}
<br/>

- Restart Heroic Launcher and edit the settings of your game to pick Proton Experimental as your Wine version : ![proton-experimental](/assets/images/Proton-Experimental.png)
{: style="text-align: justify;"}
<br/>

- If your Genshin doesn't switch from the launcher to the game, you need to add an Environment variable into your Advanced Settings to force the opening of the window called `WINEDLLOVERRIDES = lsteamclient=d` and don't forget to click on the + icon to get it saved : ![environmental-variables](/assets/images/Environmental-variable.png)
{: style="text-align: justify;"}

<br/>
<br/>
And now.... It works like a charm ! 
   
I'd still recommend anyone to go into Genshin settings, set up your own quality requirements on the crowds, etc and then click on "Compatibility mode" to be certain that the screen display, quality and everything considers your machine... otherwise you'll be set on maximum screen display, maximum quality and if you have a laptop with 8GB RAM like me... Prepare for a crash lol. With that special mode and playing with resolution of the settings page, it's all smooth for me now.
{: style="text-align: justify;"}
<br/>
So, as I always say : on the Internet, always ask questions ! Don't stay on your own because often many people have lived the same hurdles and are willing to help you. As I've seen on Fedora forum for my 4-day long song issue, and I've seen here too with someone at the other side of the planet helping me for 2-3 hours to have an optimal setting. 
{: style="text-align: justify;"}

Internet people can be amazing, it's not either technical people that speak an alien language or trolls ! Many people are willing to help with speaking at your level if you specify your level in things, are patient and sticking up until the issue is well determined. Just be careful not to launch commands you don't understand, but other than that... Don't stay alone !
{: style="text-align: justify;"}
