# Use ES6 Destructuring assignment syntax to unpack values into variables

Destruturing assignment syntax allows you to assign the properties of an array or object to variables. 

This allows for much cleaner, leaner and more readable code.

```javascript
const cars = ['Ferrari', 'Aston Martin', 'Audi' ];
const [ferrari, astonMartin, audi] = cars;
```

Using `...rest` syntax also allows you to assign the rest of the values if needed:

```javascript
const cars = ['Ferrari', 'Aston Martin', 'Audi', 'BMW', 'Vauxhall', 'Volkswagen'];
const [ferrari, astonMartin, audi, ...rest] = cars; // ferrari = 'Ferrari', astonMartin = 'Aston Martin', audi = 'Audi', rest = ['BMW', 'Vauxhall', 'Volkswagen']
```

You can also ignore values that you aren't interested:

```javascript
const cars = ['Ferrari', 'Aston Martin', 'Audi', 'BMW', 'Vauxhall', 'Volkswagen'];
const [ferrari, , audi, , vauxhall, ,] = cars; // ferrari = 'Ferrari', audi = 'Audi', vauxhall = 'Vauxhall' 
```

This can be used on objects too:

```javascript
const family = {
    mother: 'Gail',
    father: 'Kevin',
    sibling1: 'Helen',
    sibling2: 'Sally'
}

const { mother, father, sibling1, sibling2 } = family; // mother = 'Gail', father = 'Kevin', sibling1 = 'Helen', sibling2 = 'Sally'
```

#### Further Reading
[MDN - Destructuring assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)
