# Using `for...in` with Objects

Using the combination of `for in` and `Object.keys()` we can easily loop through an object and get it's properties.

```javascript
const person = {
    name: 'Karl Wills',
    birthPlace: 'Warrington',
    age: 31,
    gender: 'male',
    occupation: 'Front-end Developer'
}

for(const prop of Object.keys(person)) {
    console.log( `The property name is "${prop}" and the value is ${person[prop]}` );
};
```

### Browser Support

* `for...in` - All modern browsers and IE6+
* `Object.keys()` - All modern browsers and IE9+

#### Further Reading

[MDN - Object.keys()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys)
[MDN- for...in](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in)
