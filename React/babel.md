# What is babel? 
Babel.js is a wonderful tool for compiling your JavaScript. In terms of React, Babel is going to allow us to transform our JSX (which you'll see soon) into actual JavaScript. You can also opt into "future" versions of JavaScript (ES2015, 2016, etc) and use Babel to transform your future JavaScript to modern day JavaScript so the browser can understand it. 

With Webpack you tell it which transformations to make on your code, while Babel is the specific transformation itself. The overview of implementing Babel is that we npm install a bunch of tools specific to Babel, then we add babel as a loader in our webpack settings. Then whenever webpack bundles our code, it'll transform our code with whatever we specified with Babel.

Get babel along with a few babel presets. In the same directory as the ```package.json```, install our ```babel``` requirements:

```
$ npm install --save-dev babel-core babel-preset-es2015 babel-preset-react babel-preset-react-hmre babel-preset-stage-0
```
