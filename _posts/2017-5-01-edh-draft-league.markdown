---
layout: post
title:  "EDH Draft League Web Site"
class: post
overlayTitle: EDH Draft Site
date: 2017-05-01
featured: true
imageName: draftleague
animation: left

icons:
- code

tags:
- Development
- Javascript
- Firebase
---

<span class="dropcap">I</span> play a lot of Magic the Gathering. I collect the cards, play the game, covet pieces of artwork, and have tattoos of it. Needless to say, I'm unhealthily obsessed with the game, and it's been a part of my life for almost two decades now. I'm fortunate to have a group of friends who I play with regularly. One day, two summers ago, my friend and I decided to run a crazy idea: a special kind of format where a group of eight of us would draft cards from the entire available pool. We were inspired by [Sheldon's Rotisserie Draft League](http://www.starcitygames.com/article/35090_Friends-Setting-Up-The-Commander-Rotisserie-Draft.html), but knew that getting people together to do the whole thing in person wasn't going to happen.

![Draft League]({{ site.baseurl }}/image/assets/draftleague.jpg){: .vertical-image}

Thus, the EDH Draft League web site was conceived.

In secret, the two of us began to work on the first version of the site. The idea was simple: a website that would facilitate us drafting cards, like a fantasy-football site, asynchronously. The first iteration was pretty rough: a bootstrapped front-end using [JSON Blob](https://jsonblob.com/) as a flat-file "back-end". We integrated with [MTG JSON](https://mtgjson.com/) as our data.

The first iteration was cobbled together, but the league was a smashing success. Enough that we did round two in spring 2017, and pushed for a better system. Enter [EDH Draft League v2](https://www.edh-league.com/).

Version 2 had a more stable foundation since we opted to use [Firebase](https://firebase.google.com/) as the platform. Developing on Firebase was a breeze, and we had little issues getting Google authentication and mobile push notifications going. The front-end was dressed up too, opting for a lightweight CSS framework, [Skeleton](getskeleton.com), the same one I use on this site.

Additionally, a major part of the second league season was us developing a custom ELO ranking algorithm. ELO is a ranking system used in chess, but we needed something similar that could function with different critera; namely, multiplayer with three different sub-rankings. After a lot of trial and error we implemented our custom system into the site and used it as an improvement over the static Wins/Losses/Votes system that our first iteration had. You can see the rankings on the "Standings" page.

Version 3 is probably going to happen in the future; I would like to build a decklist and playtesting application that our group can use and add it to the site. Whenever v3 happens, I'll be sure to update with another blog post that goes in more detail!