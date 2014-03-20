static-heroku-nodejs
====================

1) Start new app and "git init" it
2) Go to https://www.heroku.com and sign up there
3) On https://dashboard.heroku.com/apps page click on Create a new app
4) Copy heroku Git URL and add it to your app
5) Create sample index.html file
6) In order to serve html files Heroku needs to start some web server.
It can be nodejs, ruby or whatever language is supported by platform.
In case of this tutorial we will use built-in nodejs "http" package web server.
Sample implementation of web server, that can only serve static html files is app.js file.
It just try to read requested html file and if this file exists write its content to response.
Locally server can be started by "node app.js" command (you need nodejs installed).
7) Heroku doesn't know anything about your app.js file. In order to notify it, you need to create Procfile consisting of only line of code
"web: node app.js"
8) Now commit all changes and push it to heroku using "git push heroku master"