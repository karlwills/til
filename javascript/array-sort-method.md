# Sort an array of data using `.sort()`

An array of data can be quickly organised using the built-in `.sort()` method. When you call the `.sort()` method on an array, it looks through each item, comparing it to the one immediately after it.

> The default sort order is built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values.

#### Sorting Items

```javascript
let familyNames = [
    'Joanna',
    'Karl',
    'Gail',
    'Kevin',
    'Helen',
    'Paul',
    'Sally',
    'Robert'
];

familyNames.sort() // ["Gail", "Helen", "Joanna", "Karl", "Kevin", "Paul", "Robert", "Sally"]
```

You can also compare each of the items within the sort, by passing in a function. This will allow you to order the items how you wish, by returing a value from a conditional statement.

For example, this will sort the names by length. Longest first.

```javascript
let familyNames = [
    'Joanna',
    'Karl',
    'Gail',
    'Kevin',
    'Helen',
    'Paul',
    'Sally',
    'Robert'
];

familyNames.sort((person1, person2) => person1.length > person2.length ? -1 : 1); // ["Joanna", "Robert", "Kevin", "Helen", "Sally", "Karl", "Gail", "Paul"]
```

*Note:* The array passed to the function is sorted _in place_. Meaning that the original array has been mutated.


#### Browser Compatibility
Works in all modern browsers, with support in Internet Explorer back to version 5.5


#### More Information
[MDN - Array.prototype.sort()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)
