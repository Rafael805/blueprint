# What is Heroku? 
Heroku is a cloud platform as a service supporting several programming languages that is used as a web application deployment model.

To get started sign up or heroku and download the heroku toolbelt. Once installed start by running:
```
heroku
```
Then login in:
```
heroku login
```
This will ask you to enter your heroku email and password. To confirm you're logged in run:
```
heroku autho:whoami
```
To create our heroku app: 
```
heroku create
```
This gives us a custom url and adds a new remote to our git repository. To push our master branch to the heroku remote and start the process of deploying the code run: 
```
git push heroku master
```
To open your heroku app: 
```
heroku open
```
