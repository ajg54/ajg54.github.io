---
title: "Getting started with GitHub Pages and Jekyll"
date: 2021-04-01
---
This website is hosted via [GitHub Pages](https://pages.github.com/) and uses [Jekyll](https://jekyllrb.com/).
GitHub Pages allows you to create a simple website either generally for yourself / organisation or specifically for individual GitHub projects. 
Jekyll is a static website generator that is supported by GitHub Pages and, for example, can be used to create a blog from markdown (.md) files.
Somewhat appropriately, this first post is detailing my experiences when setting this up.

This is an example of a personal GitHub Pages site linked to my overall GitHub profile.
I just started out following the instructions on the GitHub Pages landing page, but in parallel also completed the [GitHub Pages course on their Learning Lab](https://lab.github.com/githubtraining/github-pages).
In part, I did this due to some waiting time during the set-up process, more on that later.

It is perhaps useful to know my background when starting this.
I was already in possession of a GitHub user account and was familiar with using both GitHub and git in general.
I had an IDE configured to communicate with GitHub working on my local machine, although admittedly that IDE is one primarily geared towards Python development.
I also have some familiarity with markdown and building websites / webapps in various different ways.
However, I had never used GitHub pages before and had not even heard of Jekyll before.

In total, this site was up and running (excluding this both) in a basic form roughly an hour after deciding to set it up.
The majority of this time was not taken up with actively setting it up, but either waiting for something to happen or being distracted by something else.
In practice, it should only take a few minutes when you know what you are doing.

The quickstart on the landing page provides only enough instruction to display the classic *Hello World* message without styling, but at the bottom of the page does direct you towards further resources.
Perhaps this was bad luck, but it certainly wasn't instantaneous for my site to go live.
The fact there can be a modest delay for pushed changes to go live is mentioned elsewhere, but it would have been nice to have this more explicitly stated.
The work you have to do is very limited to get it up and running, but there is some manual work (e.g. a naming convention that you have to follow, but that is not automatically enforced) and with the delay in going live it was unclear if I'd somehow made a mistake.
I'm guessing that this is in general because Jekyll is a static website generator, so presumably there is a hidden and automatic compile step on the backend.
If you were writing directly in HTML or using a dynamic server-side framework this wouldn't be necessary.
Of course there are benefits to using a framework like Jekyll, such as speed (as pages are not dynamically generated) and automation (compared to doing everything by hand).

Since the site didn't appear immediately I took a diversion to try out the course / tutorial.
This gave an opportunity to learn about making a blog with Jekyll.
The fact that it is automatically supported by GitHub Pages is very convenient, but you then miss *seeing* it in aciton.
However, if that is something you want to see from an education perspective, you can of course install it locally and play around with it there in the *localhost* setting.
Through the tutorial I got to see a bit more how things are working with Jekyll.
One thing I did notice, however, was that in the end result of the tutorial there was a link to a non-existent rss feed.
This was trivially fixed by adjusting the config file to ask for the standard xml file for the rss feed to be generated.

As a first impression, this seems like a very easy way to make a simple website for free that also doesn't require really learning any explicit web development.
Of course there are quite some limitations, for example using a Python web framework is not supported.
However, by using Jekyll and the [minima](https://github.com/jekyll/minima) theme, you get something usable right out of the box.
