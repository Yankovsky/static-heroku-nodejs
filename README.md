static-heroku-nodejs
====================

#### [Demo](http://static-heroku-nodejs.herokuapp.com/)

#### Step-by-step guide:
1. Start new app and ```git init``` it.
2. Go to [Heroku](https://www.heroku.com) and sign up there.
3. On [your apps page](https://dashboard.heroku.com/apps) click on "Create a new app".
4. Copy Heroku Git URL and add it to your app using ```git remote add heroku your-git-url```.
5. Create sample **index.html** file.
6. In order to serve files Heroku needs to start some web server.
It can be nodejs, ruby or whatever language is supported by the platform.
For this tutorial I will use built-in nodejs [http](http://nodejs.org/api/http.html) package to create simple static web server.
You can find sample implementation in **app.js** file.
Locally server can be started using ```node app.js``` command (you need node.js installed).
7. Heroku doesn't know anything about your **app.js** file. In order to let it know, you need to create **Procfile** with only one line of code
```web: node app.js```.
8. Now you need to create **package.json** file and the easiest way to do it is use ```npm install -y``` command.
9. Now commit all changes and push it to Heroku using ```git push heroku master```.
10. Go to your app page on Heroku website and click on little rectangle with arrow near the name of your application.
It will open your static application. That's it!
