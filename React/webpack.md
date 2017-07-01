# What is webpack?
Webpack lets us bundle all of our 3rd party dependencies. Webpack has two types of dependencies in its dependency tree: sync and async. Async dependencies act as split points and form a new chunk. After the chunk tree is optimized, a file is emitted for each chunk. 

You can install webpack via npm:
```
npm install webpack -g
```

**Note:** This installs webpack globally for demonstration purposes. When you are building a real application, it’s more advisable to install webpack as a ```devDependency``` of your project.

Using an ES6 class to define a component:
```
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```
