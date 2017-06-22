# What is Node?
Node.js is an open source server framework that allows you to run JavaScript on the server. 

# Why Node.js?
Node.js uses asynchronous programming! 

Here is how Node.js handles a file request:

1. Sends the task to the computer's file system.
2. Ready to handle the next request.
3. When the file system has opened and read the file, the server returns the content to the client.

# What Can Node.js Do?
+ Generate dynamic page content
+ Create, open, read, write, delete, and close files on the server
+ Collect form data
+ Add, delete, modify data in your database

# Using Node

Start by using the node comman to run a file 
```Node <file_name>```

--example: ```Node app.js```


# Node version 
To check your current node version type the following in the terminal:
```
node -v
```

# What is a Module in Node.js?
Consider modules to be the same as JavaScript libraries. A set of functions you want to include in your application.

To include a module, use the ```require()``` function with the name of the module:

# Create Your Own Modules
You can create your own modules, and easily include them in your applications.
```
exports.myDateTime = function () {
    return Date();
};
```

Use the ```exports``` keyword to make properties and methods available outside the module file.

# Include Your Own Module
Now you can include and use the module in any of your Node.js files.

use ```./``` to locate the module, that means that the module is located in the same folder as the Node.js file.

# Node's HTTP server