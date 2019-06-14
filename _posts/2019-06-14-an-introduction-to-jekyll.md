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

## Install with RubyGems

So let's take a look at Jekyll in a little more detail. I've lifted some of this information directly from [Jekyll's Quick Start guide](https://jekyllrb.com/docs/quickstart/) — which of course you should browse through too.

The best way to install Jekyll is via RubyGems. Over the last five years or so I've used a Mac, but right now I'm working with a windows laptop (you know, translation software an Mac simply don't mix). Using Jekyll on Windows is not officially supported by the Jekyll team, so Windows users should follow this [step-by-step guide](http://jekyll-windows.juthilo.com/). Luckily for me [@madhur](https://github.com/madhur) has created [Portable Jekyll](https://github.com/madhur/PortableJekyll) containing everything which is required to run Jekyll v3.2.1 on Windows. Just download it and after running the `setpath.cmd` in command line, the setting is ok.

## Create a new project

Once installed, getting a Jekyll project up and running only requires three more commands:

	$ jekyll new yourusername.github.io
	$ cd yourusername.github.io
	$ jekyll serve --watch 
 
Once the server is running, browse to *http://localhost:4000*  and you'll see the content of your project's `_site` folder served as static HTML.
Before we carry on, it's worth noting the [configuration options](https://jekyllrb.com/docs/configuration/) available to you, and which ones to pay attention to from the beginning.
Jekyll allows you to mould your site in any way you want, and it’s thanks to the powerful and flexible configuration options that this is possible. Typically, these options are specified in a `_config.yml` file placed in your site's root directory.

You'll see settings in here for title, decsription etc. You can refence any of these settings in your templates using syntax like {{site.author}}. This is good if you want to repeat values throughout your site, like this site does in the {{site.description}} part of the template.

It's important to note that Jekyll will sometimes do some fairly assumptive things, like copying everything in the root directory to the `_site` folder. There's a good reason for this, and in many cases this is a good thing (e.g. the way I've organised assets into their own folder) but other times you want to exclude specific files or folders from that process. Use the exclude property to define an array of paths that should be omitted.

## Directory Structure

To explain the directroy structure in a little more details (seeing as I've just touched upon it), my project is broken down into 5 folders:

- _includes 
- _layouts
- _posts
- public

## Content

So that's the structure explained, but what about just *normal* web pages. Where do they go?

For the most part, much of my site's content sits in the root. As an example, there is a markdown file in there called `about.md`. Ultimatly, Jekyll will convert this into a HTML file and copy it to the root of the `_site folder`, giving me a [about page](https://aleschreiber.github.io/about/).

At the top of `about.md` is the following Front Matter:

	---
    layout: page
    title: About
    permalink: about-me
    ---

This tells Jekyll to use the "page" layout, to give it a title of "About" and to assign "/about-me/" as it's URL. There's a bunch of extra properties you can assign, but as this site shows, that's all you really need to get going.