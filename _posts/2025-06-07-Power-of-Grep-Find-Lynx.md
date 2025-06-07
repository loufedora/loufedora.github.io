---
layout: page
title:  "The power of Grep, Find and Lynx"
date:   2025-06-07 18:03:00 +0200
categories: jekyll update
author: "Lou Fedora"
permalink: /power-grep-find-lynx
---
I'm in awe with the power of information that you can get from different CLI commands. There's `grep` that I've seen already because of my audio issues because we did a lot of diagnostic commands, but I truly got to understand its true nature much later, like yesterday. Coupled with `find` and `lynx --dump`, you really can do nice things ! 
{: style="text-align: justify;"}
<br/> 
- `lynx --dump <URL> > (document.extension)` is an AWESOME way to extract web pages in a readable format. I tried other things before like `wget` but their look after the extraction unless in .odt format were awful. Lynx is just perfect, and put the clickable links in the last sections of a document, so the presentation is nice and not bloated with HTML stuff in the middle of the text. I heard later that Lynx is made for blind or people with vision troubles, no wonder. It's really good. It works as CLI web browser too, I have to search how it can display images but it's quite good for a text based CLI application already.
{: style="text-align: justify;"}
<br/>
- `find -iname "*(document or extension)*"` is a killer when you have to find back where something is sorted. `find` in general has a lot of other options but the `-i` enables to search without case sensitivity, which is mega useful. For some reason, `locate` command doesn't show me the same results, but since `find` works well I'm good with that. Can be much useful if I wanna mess with dotfiles or config files later on LOL. For that command, [Distrotube video on "How to find and locate your files"](https://youtu.be/BZ5gsFiIKOQ?si=sQ0oKSmIScjSRzb3) was such a bliss to listen to, it's so clearly worded ! 
{: style="text-align: justify;"}
<br/>
- Lastly, as I said in the beginning, once you've extracted and found your text, `grep` is wonderful to find back some peculiar information, pattern, word without having to open or `cat` the document. It can count occurencies and show lines of context around the occurencies. Can be sooo nice to use when you just need to grab back an info without having to re-read an intire document, as long as you know what you search for. Here also, [Distrotube video about `grep`](https://youtu.be/N05sWPgj-44?si=j4oxgFvPKVRa4yRM) was extra helpful. 
I find this command mind-blowing and extra useful, I hope it can serve me later on. On Linux I'm sure it will, I hope it can work on Windows too like `ls` (since no choice, we use crappy 11 only for now), like that it can be qo much quicker in order to remind oneself of some subject we wrote 3 weeks ago, without having to read all what's around to find the peculiar info.
{: style="text-align: justify;"}
<br/>
I'm sure I'll encounter many more commands that I'll appreciate. Will certainly reference them here !
{: style="text-align: justify;"}
