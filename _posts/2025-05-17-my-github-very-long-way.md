---
layout: page
title:  "My Github very long way"
date:   2025-05-17 14:35:00 +0200
categories: jekyll update
author: "Lou Fedora"
permalink: /my-github-very-long-way
---
Man, while doing a local Jekyll was quite easy, Github was quite circonvoluted for nothing since many of the tutorials didn't correspond to what I saw in my laptop and in the Github personal space. BUT I finally did it after HOURS.
{: style="text-align: justify;"}
<br/>   
After many different sources, I noticed what worked or not. So here is what I've seen working in the end : 
- Add the Jekyll theme I want from forking it to my Github profile.
- Adding an Github Actions workflow and select Jekyll. WAITING UNTIL THE THINGS LOADING IN ACTIONS ARE ALL GREEN BEFORE GOING ANYWHERE ELSE.
- Clone the Github file to my Documents through the git clone terminal command.
- Copy post files if any from the Jekyll trial, adding some info in config.
- Running git add ., then git commit -m 'first commit', then git push -u origin master.
{: style="text-align: justify;"}
<br/>  
It wasn't peculiarly easy to understand that from there, you modify the files LOCALLY (in laptop) and then run terminal commands to get it updated on github. Fortunately, [one video I watched previously](https://www.youtube.com/watch?v=mJ-qvsxPHpY) actually explained it from the very beginning, so I ran those and it seems to work now ! And when I have to update, I just run the 3 commands (with a different name for the git commit -m '') and it's good to go.
{: style="text-align: justify;"}
<br/>  
Also, it seems that the tool is very sensitive if you touch "about" or erase lines in config.yml or in about.md. It destroyed my sync that worked well before, so don't do that ! Just fill the blanks or leave it be.
