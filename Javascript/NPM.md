# What is NPM (Node Package Manager)
*npm is the package manager for javascript.*


+ npm is the package manager for Node.js. It was created in 2009 as an open source project to help JavaScript developers easily share packaged modules of code.
+ The npm Registry is a public collection of packages of open-source code for Node.js, front-end web apps, mobile apps, robots, routers, and countless other needs of the JavaScript community.
+ npm is the command line client that allows developers to install and publish those packages.

If we want to include something like jQuery or the Bootstrap javascript library or any other javascript libray, we have to use a script tag. But if we're writing node in the server side and we want to include a library or something that someone else wrote we cannot add a script tag because there is no HTML. We are just dealing with Node. 

The way that we get those libraries when we're writing server side jaascript/node is through NPM. Rather that calling them libraries NPM refers to them as packages but it's the same idea. Packages are just code that someone else has written that we can include to our own projects. All the packages are centralized in the NPM website. Awesome! Furthermore, NPM has a command line tool that lets you install things really easily. 

To check your current npm version use the following in your terminal 
```
npm -v
```

**Packages**
+ javascript/node version of libraries
+ let's us install packages easily
+ centralized repository of 200,000 + packages 

All you have to do is type   
```
npm install <name_of_package>
```  
(as long as NPM knows about that package) That's it. You don't have to go find a CDN/link/copy and pasting.   

