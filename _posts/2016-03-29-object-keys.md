---
layout: default
---

# Object keys

Need to grab all the keys of an object? You can loop over it with a `for` loop, or you can use `Object.keys` to give you an array of all the keys.

```javascript
var human = {
  arms: 2,
  legs: 2,
  heads: 1
};

console.log(Object.keys(human));

// ["arms", "legs", "heads"]
```
