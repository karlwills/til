# Arrow functions inherit their `this` value from their parent`s context

A common misconception is that arrow functions have no `this` value.

Arrow functions actually inherit their `this` value from the context of their parent. Also known as lexical binding.

#### Examples

In this example, `this` *would not* be the element, it would in fact be the parent's context (the window in this case).

```javascript
element.addEventListener('click', () => {
  console.log(this); 
});

```

However in this example, `this` *would* be the element, because arrow function within the setTimeout's parent is the element itself.

```javascript
element.addEventListener('click', function() {  
   setTimeout(() => {
      console.log(this);
   }, 500);
});
```

#### Further Reading

[MDN - Arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
