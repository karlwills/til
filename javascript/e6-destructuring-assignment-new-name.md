# Use ES6 Destructuring assignment syntax to unpack values and assign them into variables with a new name

```javascript
const temperatures = {
  yesterday: 15,
  today: 18,
  tomorrow: 22
};

const  { yesterday: highYesterday, today: highToday, tomorrow: highTomorrow  } = temperatures;
// highYesterday = 15, highToday = 18, highTomorrow = 22
```

*Tip:* Read the assignment syntax as "get the value of `temperatures.yesterday` and assign it to a new variable named `highYesterday`.


#### Further Reading
[MDN - Destructuring assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)
