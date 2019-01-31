# Looping through objects using `Object.keys()` and `Array.forEach()`

`Object.keys()` will return an array of an object`s own property names.

```javascript
    const cars = {
        fast: 'Ferrari',
        slow: 'Mini Metro',
        big: 'Hummer',
        small: 'Smart Car',
        electric: 'Tesla'
    }

    Object.keys(cars); // ["fast", "slow", "big", "small", "electric"]
```

Using `.forEach()` on the returned array provided from `Object.keys()` will allow us to access both the keys and values from within it.   

```javascript
    const cars = {
        fast: 'Ferrari',
        slow: 'Mini Metro',
        big: 'Hummer',
        small: 'Smart Car',
        electric: 'Tesla'
    }
  
    Object.keys(cars).forEach(function(item) {
        console.log(item); // Key ('fast', 'slow', 'big'...)
        console.log(cars[item]); // Value ('Ferrari', 'Mini Metro', 'Hummer'...)
    });
    
    // and with ES6 ...
    
    Object.keys(cars).forEach(item => console.log(`${item} : ${cars[item]}`));  // 'fast : Ferrari', 'slow : 'Mini Metro'...
```

#### Browser Compatibility
Both are supported in all modern browsers and IE9+. There are Polyfills available for older browser support.

#### More Information
[MDN - Object.keys()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys)
[MDN - Array.forEach](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
