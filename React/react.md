# Why React? 
React is a JavaScript library

# JSX 
You can embed any JavaScript expression in **JSX** by wrapping it in curly braces.

After compilation, JSX expressions become regular JavaScript objects.

This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions:

```
--example: 
function getGreeting(user) {
  if (user) {
    return <h1>Hello, {formatName(user)}!</h1>;
  }
  return <h1>Hello, Stranger.</h1>;
}
```

Babel compiles JSX down to ```React.createElement()``` calls.

# Hello World
```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

# Container component 
A container component is a component that maintains state and renders child components.

# Presentational components
A presentational component is a component that used props to display information. 
 
# Props
**Props** are used for initializing a component with data.

# State
a react **state** is uesd for keeping track of data that changes in a component. 
