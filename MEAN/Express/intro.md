# Library vs Framework

A library is code someone else wrote that we can include in our application and use. Framework is similar but the way that we use it is different. 

From a stackover flow post: (https://stackoverflow.com/questions/3057526/framework-vs-toolkit-vs-library)

*The most important difference, and in fact the defining difference between a library and a framework is Inversion of Control. What does this mean? Well, it means that when you call a library, you are in control. But with a framework, the control is inverted: the framework calls you. Basically, all the control flow is already in the framework, and there's just a bunch of predefined white spots that you can fill out with your code. A library on the other hand is a collection of functionality that you can call.*

Both frameworks and libraries are external code that you use in your application. But a library is something you're in control of. If you want to use a library you can use 1 method, 10 methods, etc. For example, if you include jQuery it's up to you which parts of it you use. You might use a few methods for animations or 100+ methods. With a framework on the other hand you give up a bit of control. You have decisions that are made for you that you have to abide by to use the framework. The point of a framework isn't to homogenize how all applications work. What frameworks do is that they take all the setup work all basic application needs and prepackages it so we can use it and get started with new apps without doing all the ground work evry single time. 

# What is Express?
*Fast, unopinionated, minimalist web framework for Node.js*

Express is a web development framework. By using with express you're able to focus on writing the application content and not needing to worry about creating a server, dealing with routes, connecting with a database, etc. 

# Why Express? 
Express is by far the most popular node web development framework. It has the most the most downloads on npm and contributors. There is a big community who know express.

to install express use: 
```
npm install express
```

**HTTP Request/Response**: When you go to a URL like Google.com and hit ENTER, you are asking for a web page. You send a HTTP request and that request is either a GET request, POST request, etc. You potentionally send data along with your request. The server that you're requesting from will decide what page to send back to you (e.g Google home page, Google login page, etc). Whatever it is, the server is deciding what to send back and it responds with a response. That is what you're going to use Express to do:

+ Send a request, server side code figures out what you'r asking for and then it sends you back a response. 


**Routes:** The code that is responsible for listening and receving the requests and deciing what to send back. 

--example: Code that is listening for a request to the home page "/".

```
app.get("/", function(request, response) {
response.render("home")
});
```

Inside of routes we have code that is rendering the home page that is going to respond with the content of our home page which is another file somewhre else. 


