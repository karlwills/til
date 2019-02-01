# Use ES6 destructuring to pass in specific `props` to components

Instead of passing in the `props` object as an argument to a function or component in React, you can use ES6 destructuring to pass in the specific property that you would like.

Not only is this a lot cleaner, it also saves the repetitive typing of `props.xxx` in the component.

#### Example

```javascript

// Instead of...
const sayHi = props => {
    return <h1>Hi, {props.name}!</h1>; 
}

// Use destructuring...
const sayHi = ({name}) => {
    return <h1>Hi, {name}!</h1>; 
}

// You can also pass in multiple props
const sayHi = ({ firstName, lastName }) => {
  return <h1>Hi, {firstName} {lastName}</h1>;
}
```
