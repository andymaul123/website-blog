---
layout: post
title:  "Adventure.js"
overlayTitle: Adventure.js
date:   2016-02-05
featured: true
imageName: adventure.jpg
gridClass: grid-item-small
tags:
- Development
- javaScript
---

<span class="dropcap">L</span>ately I've found myself with two types of tasks at work: building out forms and writing a lot of javaScript (sometimes both at once). Earlier this week, while I was knee-deep in getting some functionality to work, I ran across *something* that reminded me of the old text-adventure games or MUDs. I can't for the life of me remember what triggered the thought, but the end result was, "I bet I could build a text adventure in javaScript."

Now if you know me, you know that I have this strange affinity toward text-adventure games that cannot be explained. I never played them growing up, but this would be the third text-adventure-related project I've worked on. The first was a [recreation of Zork into The Elder Scrolls: Oblivion as a mod](http://www.nexusmods.com/oblivion/mods/30951/?) and the second was a functional foray into [Inform7, the text-adventure language](http://inform7.com/).

Anyway, I started the little side-project this week and called it Adventure.js. I decided to use it as a learning tool, as I'm still a javaScript novice and haven't had much practical time with object-oriented programming in general. It's definitely a work-in-progress, but so far I have room and item objects, an inventory, and working look and take functions. The language parsing is the hardest part, honestly, and so I've decided to skip that for now. The game only reads the first one or two words put into the input - anything more and it will get confused.

There's only one boring room and two items, but it's a start! Yes, one of the items is a pebble, and there's a good reason for that. While I'm working on adventure.js I'm constantly fuming over memories of playing this old point-and-click game called Shadowgate. You could pick up rocks in that game. I don't know why. 

Man I hated Shadowgate.

I'll be working on this for a bit and will post the "finished" project at some point. Here's an iframe of it in action and the [GitHub repo](https://github.com/andymaul123/adventure.js).

<iframe src="../../../image/assets/adventure.html" style="width: 100%; height: 500px;"></iframe>

