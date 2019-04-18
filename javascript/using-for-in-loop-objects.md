# Using `for...in` with Objects

Using `for in`, we can easily loop through an object and get it's properties.

```javascript
const person = {
    name: 'Karl Wills',
    birthPlace: 'Warrington',
    age: 31,
    gender: 'male',
    occupation: 'Front-end Developer'
}

for(const prop in person) {
    console.log( `The property name is "${prop}" and the value is ${person[prop]}` );
};
```

### Browser Support

* `for...in` - All modern browsers and IE6+

#### Further Reading

* [MDN - for...in](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in)
