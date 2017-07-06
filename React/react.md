# Why React? 
React is a JavaScript library. What makes React so convenient for building user interfaces is that data is either received from a component’s parent component, or it’s contained in the component itself. With React, by conceptually re-rendering everything whenever anything changes, not only do you have code that is safe by default, it is also less work as you only need to write the creation path: updates are taken care of for you.

# JSX 
You can embed any JavaScript expression in **JSX** by wrapping it in curly braces. After compilation, JSX expressions become regular JavaScript objects. This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions:

```
--example: 
function getGreeting(user) {
  if (user) {
    return <h1>Hello, {formatName(user)}!</h1>;
  }
  return <h1>Hello, Stranger.</h1>;
}
```
If you decide to use JSX you’ll need some compile stage to convert your JSX to JavaScript. 

Babel compiles JSX down to ```React.createElement()``` calls.

To recap, JSX simply allows us to write HTML like syntax which (eventually) gets transformed to lightweight JavaScript objects. React is then able to take these JavaScript objects and from them form a “virtual DOM” or a JavaScript representation of the actual DOM. 

# Hello World
```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```
# Flow
```
[]app
--[] api
--[]components
--[]styles
----app.css
--app.jsx
[]node_modules
[]public 
.gitignore
package.json
readme.md
server.js
webpack.config.js
```

# Components 
Components are the building blocks of React (they’re essentially widgets or modules). React uses the concept of components which, conceptually are containers for our data and UI . Additionally, a React component can define it's own state using a ```state``` property for handling stateful components. To create a React component, you'll use an ES6 class.

To create a React component: 
```
class <Component> extends React.Component
```
To render a React component to the DOM:
```
ReactDOM.render
```
```
var React = require('react');
var ReactDOM = require('react-dom');
class HelloWorld extends React.Component {
  render() {
    return (
      <div>Hello World!</div>
    )
  }
}
ReactDOM.render(<HelloWorld />, document.getElementById('app'));
```

Every component is required to have a **render** method. **ReactDOM.render** takes in two arguments. The first argument is the *component* you want to render, the second argument is the *DOM node* where you want to render the component. In the example above we’re telling React to take our HelloWorld component and render it to the element with an ID of app. You usually only have to use ReactDOM.render once in your application because by rendering the most parent component, all child components will be rendered as well.

# Container component 
A container component is a component that maintains state and renders child components.

# Presentational components
A presentational component is a component that used props to display information. 

# Stateless functional components

*There are two types of "model" data in React: props and state.*
 
# Props
**Props** are used for initializing a component with data. They are a way of passing data from parent to child.

# State
A react **state** is used for keeping track of data that changes in a component. State is reserved only for interactivity, that is, data that changes over time. When we refer to a component's state, we mean a snapshot of the instance of the component on the page. 

For example, in regular HTML (without React), when we have a text ```<input />``` box on a page, the state of the ```<input />``` element is that the value of the ```<input />``` component is a blank string (i.e. ""). When our user types into the ```<input />``` box, the state changes for the ```<input />``` box to set the value to the keystroke the user made.

# State vs Props
The difference between ```state``` and ```props``` can be a little confusing at first. props are used to pass down data and event handlers from parent components to child components. state on the other hand is used to manipulate the current state of a component.
