---
title: "Getting (re)started with GitHub Pages and Jekyll"
date: 2025-04-16
---
A few years ago, I set up this website just as a test for using [GitHub Pages](https://pages.github.com/) together 
with the static website generator [Jekyll](https://jekyllrb.com/). GitHub Pages allows you to create a simple 
website either generally for yourself / organisation or specifically for individual GitHub projects. Jekyll is a 
static website generator that is supported by GitHub Pages and, for example, can be used to create a blog from 
markdown (.md) files. This updated first post shares experiences when setting this up and also subsequently with 
Jekyll (also in a different setting).

When setting this up I was already familiar with GitHub, markdown and building websites, but had no familiarity with 
Jekyll and had never even heard of it before. From this starting point, it took me roughly an hour to get it up and 
running. However, the majority of that time was spent passively waiting rather than actively doing anything, so in 
that time I also followed a (now removed) GitHub Pages course and read up on Jekyll.

The nice thing about using Jekyll together with GitHub pages is that it automatically builds and deploys your 
website whenever you push code to the relevant branch of the repo. It is worth nothing that not all jekyll packages 
are supported, so this [list](https://pages.github.com/versions/) is a useful reference to be aware of. Typically 
when working with Jekyll you start with a theme, and it is good to check that the dependencies of that theme are 
compatible with GitHub Pages. I have fallen afoul of this on another project meaning that I have to locally build 
the website and then push the built website to GitHub (with the automatic build step on the server disabled).

In this case I am using the default [minima](https://github.com/jekyll/minima) theme, which allowed me to get this 
basic blog format up and running pretty quickly without prior Jekyll experience. There was only one real tweak that 
I had to make initially, which was referencing the _jekyll-feed_ plugin in the config file to fix a link to a 
non-existent resource that was automatically being generated. 

For this iteration I had to do some manual work to get a working bsky logo in svg format for the footer. When 
investigating this it seemed that the maintenance of this theme was not quite as clean as one would like. I also had 
some _fun_ setting this up with a custom subdomain, although that was largely an unfortunate consequence of making 
an initial mistake with the DNS settings and then having to wait a while for DNS propagation. Removing and reading 
the custom domain in the settings of the repo at a later date immediately solved all issues.

In general I think that GitHub Pages is a nice solution for making a simple website for free without prior knowledge 
of web development. However, I have to say that Jekyll is not my preferred solution, although of course a logical 
choice in this setting due to its integration with the hosting service.
