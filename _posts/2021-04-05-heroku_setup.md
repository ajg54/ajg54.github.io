---
title: "Getting started with Heroku for Python app deployment"
date: 2021-04-05
---
To communicate the results of data science projects, it is often useful to make an interactive dashboard.
Many frameworks for making dashboards are effectively making a small web application for you.
This can typically be done natively using the same programming language used for the core analysis and without (much) knowledge of web development.
For example, [R Shiny](https://shiny.rstudio.com/) is one such framework for R.
When run locally, a Shiny app is accessible via your web browser at your localhost URL.
One major plus of creating a dashboard as a web app is the somewhat tautologous point that it is deployable online.
Sticking with the R Shiny example, there is even [shinyapps.io](https://www.shinyapps.io/) providing a very straightforward platform that is perfect for free deployment of demo apps.
However, what about Python deployment? 
This post documents one of ways you can do this.
I was doing everything using a Windows 10 laptop, btw.

I started with the question *is there a shinyapps.io for Python?* 
As far as I can tell, the strict answer is *no*.
With Python being a more generally used programming language than the more data specific R, there are many many ways to build and host a simple Python web app.
This much richer array of options is perhaps a reason for the apparent lack of a direct equivalent.
However, with both a quick search online and asking around giving [Heroku](https://www.heroku.com) as the top suggestion, I decided to give that a go.
As context, I have previously deployed apps built with Flask (a Python web framework) either directly or with Dash.
I've done this on my own server and in AWS, both with and without Docker.
However, the AWS experience was certainly not ideal for a quick and painless demo deployment.
So let's see if Heroku is fitting the bill better.

Having never used Heroku before, I had to first register. 
That was slick and painless, and in no time I was getting going with their [Python tutorial](https://devcenter.heroku.com/articles/getting-started-with-python).
The introduction there gives a short list of dependencies, and in fact the only thing that took any real time was setting up one of those: Postgres.
I did that *on the fly* when it was needed in the tutorial, but it would have been smarter to do it up front.
At the next step there is a further dependency (git), which is needed for the Heroku CLI (command line interface).
In general, the tutorial is very well made and I like that it gets you working with the CLI and also with git straightaway.
Apart from the Postgres set-up, every step was really quick and worked as expected, and the Postgres part was also pretty fine.
It was also nice that it included *config vars* and *provision a database* steps, which are two of things you need to think a little bit more about when shifting from a personal setting on your local machine to a cloud deployment.
To do the plugins part, you need to register a credit/debit card .
Not an unreasonable policy on their part, but it does always feel more comfortable when trying out something at the free tier level if there is literally no way they can bill you.

Timing wise, I went from having no account at Heroku to having their placeholder app deployed in roughly 15 minutes.
There was then a further 20 minutes to follow the steps to replace that with their demo Python (Django framework) app and get to the stage where you can trial a plugin (if happy to register your card details).
After that I spent another 15 minutes on the remaining steps and then had to install Postgres at the end.
All in all, you should be able to easily go from start to finish within one hour if you are familiar with all the dependencies apart from Postgres and have them installed (and install the latter at the very start of the tutorial).
Apart from making life (marginally) more difficult for myself with Postgres, I slightly deviated from the tutorial by doing it via my Python IDE.
However, that pretty much meant that I was just using the command line terminal embedded there rather than standalone.
There were a few places where the response needed in the terminal was not exactly as describe, but in any case trivial and those prompts can be platform / local settings specific.
It was even a good learning / reminder, when I accidentally used the Linux prompt (rather than the Windows one) when trying to run the app locally.
From a personal perspective, I would have preferred the demo to be Flask based and also a little bit more flexible.
By flexible I mean that you work with a more general development setup (e.g. repo on GitHub, using Docker), but it is understandable both from a prioritary and simplicitly perspective why this was not done.
Also for my desired usage (demoing a personal dashboard), the basic development flow from the demo would be sufficient.
In any case, I will find out when I give that a go later on.
