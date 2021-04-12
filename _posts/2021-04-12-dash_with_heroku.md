---
title: "Deploying a Dash demo app on Heroku"
date: 2021-04-12
---
Having completed the [Python app tutorial on Heroku](https://devcenter.heroku.com/articles/getting-started-with-python), I wanted to deploy a demo Dash app.
There are a couple of differences here compared to the tutorial.
- Dash is built on Flask whereas the tutorial uses a Django app.
- The project will be started with a remote repo hosted on GitHub.

The goal was to get a basic Dash demo app up and running in a straightforward way.
The text below recaps this process, but with the first timer trial and error omitted.

To get going, a repo on GitHub was created with the usual set-up for a Python codebase.
This was then cloned locally as a project in my IDE with a virtual environment set up.
Following the [installation](https://dash.plotly.com/installation) and [demo app code](https://dash.plotly.com/layout) for Dash, a basic app was working locally straightaway.

The next step was to get it also running locally via the Heroku CLI.
Recalling the command *heroku local -f Procfile.windows*, I copied over this file from the demo and modified its one line to refer to the app.py script.
This was all that was needed, although it is unclear whether there is any real benefit of having this command available for a simple app like this (as opposed to just running it locally not using the Heroku CLI).

The final step was to actually launch in on Heroku.
An app was created via the CLI: *heroku create [app-name]*.
The code was then pushed: *git push heroku main*, but this did not lead to a working application (of course).
However, it is worth nothing that this command facilitates working collaboratively with a shared master repo and only deploying new apps explicitly with this command. 
Three further modifications were needed.
- A procfile is needed. 
  Simply copying the one from the tutorial seemed unlikely to work in this setting (by eyeballing the content).
  However, simply searching online for such a file for a Flask app quickly gave a working solution.
- The server needs to be defined in the Dash app simply be adding  the line *server = app.server* to the app.py script.
- Gunicorn is referenced in the procfile (and thus presumably used to serve the app on Heroku), so this needed to be added to the requirements file.

In total, the whole process took around 45 minutes, including some downtime due to some misbehaviour by my laptop.
A large part of this was also due to unfamiliarity with the process.
As usual with a quick and first deployment, some things remain unclear such as whether the server set-up (both in the Procfile and app.py script) is best practice.
