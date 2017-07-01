# What is webpack?
Webpack is a code bundler. Basically, it lets us bundle all of our 3rd party dependencies. 

# What problem is this thing solving? 
Many times we have to take our code and change it so it's compliant with what the browser is used to (vanilla HTML, CSS, and JavaScript). For example, if you've ever used a CSS Preprocessor like SASS or LESS you know you need to transform your SASS/LESS code into normal CSS.

Three main things webpack needs to know: 

1) The starting point of your application, or your root JavaScript file.

2) Which transformations to make on your code.

3) Which location it should save the new transformed code.

# Getting started 

You can install webpack via npm:
```
npm install webpack -g
```

**Note:** This installs webpack globally for demonstration purposes. When you are building a real application, it’s more advisable to install webpack as a ```devDependency``` of your project.

The first thing we need to do is create a file which is going to contain our webpack configurations. Conveniently, this file should be named **webpack.config.js** and be located in the root directory of our project.

Now that we have our file made we need to make sure that this file exports an object which is going to represent our configurations for webpack.

```
// In webpack.config.js
module.exports = {}
```

**1.**Tell webpack where the entry point of our application is located. 
```
// In webpack.config.js
module.exports = {
  entry: './app/index.js',
}
```
All we do is give our object a property of **entry** and a value which is a string which points to our root JavaScript file in our app.


