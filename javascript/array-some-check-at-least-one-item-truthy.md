# Check at least one item in an array returns truthy using `Array.some()`

Using the `.some()` method on an array is a good way to test if one or more items passes a condition that you provide.

`.some()` executes the provided conditional function until it finds a truthy value, returning `true` if it does and `false` otherwise.

The method also returns `false` for any condition put on an empty array.

#### Example

```javascript
const ages = [
    31,
    27,
    33,
    25,
    7,
    4
];

ages.some(age => age > 5) // true
ages.some(age => age < 3) // false
```

#### Browser Compatibility
Works in all modern browsers, with support in Internet Explorer 9+. Polyfill also available for older browsers.


#### More Information
[MDN - Array.prototype.some()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)
