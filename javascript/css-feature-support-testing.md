# Testing CSS support with JavaScript

With CSS, you can check if a feature is supported using the `@supports()` feature query.

```css
@supports(display: flex) {
    .element {
        display: flex;
    }
}
```

This can also be achieved using JavaScript, using the `CSS.supports()` method:

```javascript
if(CSS.supports('display', 'flex')) {
    // Flexbox is supported    
} else {
    // No support for Flexbox
}
```

The above will return a `boolean`, allowing you to apply logic based around the condition.

You _could_ also check that the CSS interface is also supported as part of the condition:

```javascript
if('CSS' in window && CSS.supports('display', 'flex')) {
    // Flexbox is supported    
} else {
    // No support for Flexbox
}
```

A good case for the above would be the ability to write any polyfills/enhancements based around CSS features that may 
or may not be supported.

#### Browser Compatibility
Works in all modern browsers, with no support in Internet Explorer.


#### More Information
[MDN - CSS @supports](https://developer.mozilla.org/en-US/docs/Web/CSS/@supports)
