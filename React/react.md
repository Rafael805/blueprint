# Why React? 
React is a JavaScript library. What makes React so convenient for building user interfaces is that data is either received from a component’s parent component, or it’s contained in the component itself.

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

# Components 
Components are the building blocks of React (they’re essentially widgets or modules). To create a React component, you'll use an ES6 class.

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
 
# Props
**Props** are used for initializing a component with data.

# State
a react **state** is uesd for keeping track of data that changes in a component. 
