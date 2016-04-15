---
layout: default
---

# Use String & List methods together

How do one merge two datasets? Make sure you create 2 sets (or more) of objects with matching keys. Then loop through it using `for in` and use the resulting key on both objects/maps.

Try this out:

```javascript
var prices = {
    "blue" : 9,
    "red" : 5.34,
    "orange" : 9
};

var quantities = {
    "blue" : 2,
    "red" : 4,
    "orange" : 7
};

// calc
for(var color in prices){
    console.log(prices[color]);
    console.log(quantities[color]);
    console.log(prices[color] * quantities[color]);
    console.log("==========================")
}

```
