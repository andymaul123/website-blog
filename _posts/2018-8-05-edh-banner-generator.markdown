---
layout: post
title:  "Node.js Banner Generator"
class: post
overlayTitle: Node.js Banner Generator
date: 2018-08-05
featured: true
imageName: banner-generator
animation: center

icons:
- code

tags:
- dev
---

<span class="dropcap">C</span>ustomization is a large part of the culture surrounding EDH, a format of Magic the Gathering where players build a deck around a legendary creature. People spend thousands of dollars procuring special versions of cards for their deck, getting alterations painted on them, and getting them signed by the card's artist. There's a popular website for housing player's decklists called [Tapped Out](www.tappedout.net). People here go hog-wild customizing their profile pages and deck lists, usually resulting in an experience reminiscient of *Myspace* circa 2005. One user, however, posted some cool images of scattered cards that he took with his camera and used them as banners on his deck page. I thought it was neat, well executed, and then forgot about it for several years.

<div class="fullscreen">
    <img src="{{ site.baseurl }}/image/assets/{{ page.imageName }}.png" class="outline shadows photo">
    <span class="icon-enlarge dark icon"></span>
</div>

What does this have to do with Node.js?

About a week ago I was looking for a small project to sharpen my dev skills when I re-stumbled on that user's page and saw the banner images again. It clicked - here was an opportunity where I could make something tangible and get some good practice too. I decided to make a Node app that would generate banners for my deck pages. The big question here was: could it be done?

About two minutes into googling and I found my answer: [Jimp, the Javascript Image Manipulation Program](https://www.npmjs.com/package/jimp), a node module for doing image manipulation. I bookmarked it and went to bed.

Over the course of the next week I crafted up what is v1.0 of the [EDH Banner Generator](https://github.com/andymaul123/edh-banner-generator). It was a fantastic learning opportunity for me. I got a crash course in promises, had to do some deep dives on things like image compression, and even ran into a math problem that was over my head. Good thing I have a math wizard friend who wrote me up an equation; I'd have never figured this out on my own.

~~~ javascript
function postRotationScale(width,height,rotation) {
    return Math.hypot(width,height)*(Math.sin(Math.atan(height/width)+Math.abs((rotation*(Math.PI/180)))));
}
~~~

Now that you know what this thing creates, here's a deep dive of the process. The app consumes a list of cards from a text file the user provides to create an object of names. Users are able to specify a few things in their lists, like sets of cards with different printings and which card is their "commander". Then, using Jimp, a blank canvas is created. For each card a request is made to [Scryfall's API](https://scryfall.com/docs/api) to pull down an image and saved to the local filesystem. Subsequent requests for the same card will first look at this local store before attempt a GET on the API. 

With an image consumed, it composites it onto the blank canvas following different rules; there are rotations and coordinate mapping that are randomized for a unique output each time. Once the compositing is done the final image is saved to the filesystem and ready to be used!

v1.0 is pretty barebones. It's just the functionality, a readme, and some options via flags. The code is all piled into a single .js file. The cross-section of node.js developers and EDH fanatics is probably miniscule; a web-based deployment would open it up to people who want to use it. All of that said, I'm happy with it as a project and might consider expanding out and fixing these issues in future releases.
