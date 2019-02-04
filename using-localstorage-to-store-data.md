# Using `localStorage()` to store data in the browser

Read-only data can be set and accessed using `window.localStorage()`.

This is set per domain, and is saved across browser sessions.

Data stored in `localStorage` has no expiration time. Therefore, it is only removed when `localStorage.removeItem(item)` is called, or the user manually removes it in their browser.

*Note:* The keys and values set are always strings.

```javascript
// Set an item
localStorage.setItem('itemName', 'item value');

// get an item
localStorage.getItem('itemName'); // item value

// remove an item
localStorage.removeItem('itemName');

// remove all items
localStorage.clear()
```

#### Browser Support
Supported in all modern browsers, including Internet Explorer 8+

#### Further Reading
[MDN - window.localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage)
