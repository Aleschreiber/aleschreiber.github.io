---
layout: post
title: An introduction to Jekyll
published: true
---

A little while back, whilst trundling the interwebs researching this-that-or-the-other, my interest in maintaining a personal blog focused on my rudimentary understanding of coding peaked again.

Around a month ago I decided to start working on it. I've been doing a lot translating and writing — which I've enjoyed — and the idea of working on a small side (and useless) project was appealing. But to achieve something I was happy with (learn some new skills) I'd need to tick off each of the following:

- Keep it simple
There's no need to over-engineer. Pick the appropriate tools. For example, is it really necessary to have a content management system? Probably not.

- Keep it concise
In part, the forgotten cousin of point 1. In terms of goals, the site should avoid being a "jack of all trades". Content-driven blog? Image-driven portfolio? Pick a side and do it well.

- Keep it open
By sharing source code I know there's always the possibility of spontaneous peer-review. It's good to be kept on your toes (even if nobody's really looking). It also helps others to learn (which is the point of this particular blog, after all).

It was in the pursuit of point 1 that my interest in [Jekyll](https://jekyllrb.com/) peaked. A simple, blog-aware static site generator, I'd stumbled across Jekyll a while back but never found a use-case for it.
Instead of using a database, Jekyll runs a bunch of raw text files through a [Markdown](https://daringfireball.net/projects/markdown/) converter and [Liquid](https://github.com/Shopify/liquid/wiki) renderer to generate a complete, static website that is platform independent. As a developer you have the opportunity to build a light-weight, modulated system with little-to-no markup duplication, using all the usual CSS/SASS tools, plus the convenience of deploying your work to any architecture.

In addition to this, [GitHub Pages](https://pages.github.com/) is powered by Jekyll. By pushing your source to the world's most popular code repository you can utilise it as a free hosting platform (custom domain name and all) that generates a static Jekyll site. This also means there's no need to commit the generated HTML to the repo (which is a smarter way of working anyway). So that's point 3 checked-off.

Of course point 2 is down to me. Now that I'm more inclined to write, selecting a "blog aware" platform would appear to be a reasonable move. I don't have the assets required of an image-driven site, and much that it might be prettier to look at, it doesn't actually serve the overall purpose. This time around, it's about substance over style.

-----


