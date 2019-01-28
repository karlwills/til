# Using innerHTML and textContent to get/set content in the DOM

You can use innerHTML and textContent to update the markup and just the text within an element respectively.


#### Using innerHTML to get and set HTML Content

```javascript

// Get the element
const el = document.querySelector('.element');

// Get the HTML
let html = el.innerHTML;

// Set the HTML content
el.innerHTML = 'This would be the new HTML content. You can also add HTML elements, like a <a href="#">Hyperlink</a>';

// Add HTML to an existing elements innerHTML
el.innerHTML = 'This content will be added to the existing content. ' + el.innerHTML;

```


#### Using textContent to manipulate the text within an element

```javascript
// Get the element
let el = document.querySelector('.element');

// Set the text content
el.textContent = 'This would be the new content.';

// Add content to an existing elements textContent
el.textContent += ' This would be added to the existing content in the element.'
```


##### Browser Compatibility
Both work in all modern browsers. Also IE9+
