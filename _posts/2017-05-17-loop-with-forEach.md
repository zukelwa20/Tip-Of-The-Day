---
layout: default
---

# Easier loops with forEach


Ever wanted to have an easier way to loop over a JavaScript List aka Array? You are in luck you can use the `forEach` method.

You can loop over this dataset:

```javascript
const fruits = [
    {name : "oranges", day : Monday, qty : 8},
    {name : "apples", day : Tuesday, qty : 5},
    {name : "pears", day : Wednesday, qty : 1},
    {name : "oranges", day : Thursday, qty : 3},
    {name : "apples", day : Friday, qty : 4},
    {name : "oranges", day : Friday, qty : 13}
]
```

Using `forEach` like this:

```javascript
fruits.forEach(function(fruit){
    // print fruit details
    console.log(fruit.name + " " + fruit.day);
});
```

The `forEach` method is an easy way to loop over a list, not needing any counter. The function passed into forEach will be called with each entry in the `fruits` list. How nice is that!

Read more about [forEach](http://devdocs.io/javascript/global_objects/array/foreach).
