---
layout: post
title: "Website Re-launch"
class: post
date: 2015-11-03
---

After a long hiatus from regularly publishing content on my site, I finally felt it was time to leap back in the world of blogging. My previous setup relied on Blogger as the CMS for blogging, and I wanted to move away from it. I looked at some alternatives, but most felt too cumbersome for the type of content I wanted to author (I'm looking at *you*, Wordpress). Too much overhead to deal with. Then I stumbled on a strange and wonderful thing called [Jekyll].

Touted as an authoring platform for tinkerers, my interest was immediately piqued. What is Jekyll? According to their site:

>Jekyll is a simple, blog-aware, static site generator. It takes a template directory containing raw text files in various formats, runs it through a converter (like Markdown) and our Liquid renderer, and spits out a complete, ready-to-publish static website suitable for serving with your favorite web server. Jekyll also happens to be the engine behind GitHub Pages, which means you can use Jekyll to host your project’s page, blog, or website from GitHub’s servers for free.

It only took a few minutes before Jekyll had me hook, line, and sinker. This is exactly what I was looking for! Instead of marrying a third-party blogging platform to my website or converting the website to a new platform, I can instead just write my blog-posts in easy-to-use markdown and let Jekyll rebuild my site for deployment. Everything is simple, static, and completely controlled by me.

Even better, since it uses Liquid I can write variables and small functions inside my .html files to make my code DRY. This is a drawback to maintaining a standard static site, where changes have to be made in fifty-million different locations. Instead, I can create an _include file (header, footer, navigation, etc) and use a command to pull it into my layouts. When I need to update, I just edit the _include file and changes are propagated.

There was a learning curve associated with using Jekyll, and it's not for everyone, but it was a perfect fit for re-launching my site. I also wanted to mention the light-weight framework I'm using, called [Skeleton]. Simple, clean, and it allowed me to focus on Jekyll instead of the framework I was leveraging.

I plan on using my brand-new blogging setup with gusto, so I'll be posting stuff every Friday (or every other Friday; we'll see how quickly I run out of topics to write about). This Friday's inaugural post will be on my foray into digital painting!



[jekyll]:      http://jekyllrb.com
[Skeleton]:		http://getskeleton.com